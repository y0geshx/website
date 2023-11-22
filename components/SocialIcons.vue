<template>
  <div>
    <NuxtLink target="_blank" href="https://twitter.com/yogeshx95" title="Visit my Twitter" class="group">
      <i-line-md-twitter class="icon icon--off" alt="Twitter Logo" />
      <i-line-md-twitter-twotone class="icon icon--on" alt="Twitter Logo" />
    </NuxtLink>
    <NuxtLink target="_blank" href="https://github.com/y0geshx" title="Visit my GitHub" class="group">
      <i-line-md-github class="icon icon--off" alt="Github Logo" />
      <i-line-md-github-loop class="icon icon--on" alt="Github Logo" />
    </NuxtLink>
    <NuxtLink target="_blank" href="mailto:y0geshx@proton.me" title="Visit my Email" class="group">
      <i-carbon-email class="icon icon--off" alt="Email Logo" />
      <i-carbon-email class="icon icon--on" alt="Email Logo" />
    </NuxtLink>
  </div>
</template>

<style scoped>
a {
  @apply hover: text-gray-700 dark:hover:text-gray-300 p-2;
}
</style>
