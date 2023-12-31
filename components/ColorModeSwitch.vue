<script setup lang="ts">
const colorMode = useColorMode()
const isDark = colorMode.preference === 'dark'

function toggleDark(event: MouseEvent) {
  // @ts-expect-error experimental API
  const isAppearanceTransition = document.startViewTransition
    && !window.matchMedia('(prefers-reduced-motion: reduce)').matches

  if (!isAppearanceTransition) {
    colorMode.value === 'light' ? (colorMode.preference = 'dark') : (colorMode.preference = 'light')
    return
  }

  const x = event.clientX
  const y = event.clientY
  const endRadius = Math.hypot(
    Math.max(x, innerWidth - x),
    Math.max(y, innerHeight - y),
  )
  // @ts-expect-error: Transition API
  const transition = document.startViewTransition(async() => {
    colorMode.value === 'light' ? (colorMode.preference = 'dark') : (colorMode.preference = 'light')
    await nextTick()
  })
  transition.ready
    .then(() => {
      const clipPath = [
        `circle(0px at ${x}px ${y}px)`,
        `circle(${endRadius}px at ${x}px ${y}px)`,
      ]
      document.documentElement.animate(
        {
          clipPath: colorMode.preference === 'dark'
            ? [...clipPath].reverse()
            : clipPath,
        },
        {
          duration: 400,
          easing: 'ease-out',
          pseudoElement: colorMode.preference === 'dark'
            ? '::view-transition-old(root)'
            : '::view-transition-new(root)',
        },
      )
    })
}
</script>

<template>
  <button
    aria-label="Color Mode"
    :title="`Enable ${isDark ? 'Light' : 'Dark'} Mode`"
    class="p-2 link inline-block hover:text-gray-700 dark:hover:text-gray-300 group"
    @click.prevent="toggleDark"
  >
    <div class="icon">
      <ColorScheme>
        <template v-if="colorMode.value === 'dark'">
          <i-line-md-moon class="icon icon--off" />
          <i-line-md-moon-twotone class="icon icon--on" />
        </template>
        <template v-else>
          <i-line-md-sunny-outline class="icon icon--off" />
          <i-line-md-sunny-outline-loop class="icon icon--on" />
        </template>
      </ColorScheme>
    </div>
  </button>
</template>
