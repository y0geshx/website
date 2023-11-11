---
title: "How I Organise My Life"
description: "In this post, I share the apps and the simplistic approach I use to organise my life."
publishedAt: '2023-11-1'
status: published
tags: 
  - obsidian
  - Todoist
  - Cron
---
::Toc
::

::primary
This article is a work in progress. Feel free to read it, but some sections are incomplete.
::

::tip
Note: Visit [Obsidian](https://obsidian.md), [Cron](https://cron.com), [Todoist](https://todoist.com/).
::

Over the last few months, I've set out to really get my life sorted and organised so I can manage my time and thoughts better. I have explored numerous apps, and "productivity setups", searching for that seamless integration that could bring a sense of order to my chaotic mind and life. But nothing quite hit the mark until recently.

This is not going to be one of complex setups that you often see productivity influencers making videos and courses about. I actually rejected Obsidian once because I found it really overwhelming after watching a YouTube video setting it up so extensively, reminiscent to configuring [Emacs](https://www.gnu.org/software/emacs/). In my opinion, people watch these second brain and personal knowledge management setup videos and think it's the holy grail of productivity. They fall into the trap of constantly looking for the perfect app and the perfect setup, always trying to optimise their workflow when they're actually just wasting their time without actually focusing on what's important: getting stuff done.

My setup embraces simplicity. Here's what I wanted from my workflow.

- Note taking app: Has to have [backlinks](https://help.obsidian.md/Plugins/Backlinks) and a simple way to organise notes by topics. Should sync across all devices 
- Calendar app: Creating and editing events should be fast. Also needs to have good NLP for dates and sync with my phone's calendar widget.
- Tasks app: Should be easy to quickly add tasks. Has to have good NLP (Natural Language Processing) for dates Also should sync across all devices

So here are my apps of choice and how I use them.

## Note Taking App: Obsidian

[Obsidian](https://obsidian.md) is my choice of app for note taking. As I mentioned in the intro, I had used it previously in a very complex and overwhelming setup for a week which just didn't feel right. Almost all videos of Obsidian on YouTube were like that. So I had rejected the app back then.

Fast forward a few months and I saw Obsidian gaining popularity again on Twitter and Discord, so I decided to give it another try, only this time, I read the docs instead of videos. I soon realised the simplicity of Obsidian. It's just notes in Markdown, stored in a folder, called "Vault" in Obsidian. You can link to other notes using standard Markdown syntax and also group notes by topic using sub-folders or tags.

### Why I Like Obsidian

Obsidian has an elegant user interface with an one of the best if not **the** best Markdown editors out there which make the note-taking experience smooth and natural. My favourite part is that it supports vim keybindings in the editor! It also features a nice command palette in which all the commands can be triggered by hotkeys as well. With thousands of plugins available, it gives you tools to do pretty much anything.

But where Obsidian really won me over is privacy. Notes are saved in a local folder and never go to a database. It also doesn't store notes in a weird Obsidian specific format, it's just standard Markdown! It allows you to own and control your data.

### How I Take Notes

All notes live in the root of my Obsidian vault. I don't use sub-directories. Whenever I need to make a new note, I just create the file in the root. To group notes by particular topics, I use tags. For example, recently I had a very cool idea to sell canned carbonated sugarcane juice, which I'm not sure will taste good by the way. So I created a note for it and put the appropriate tags for it in the frontmatter.

![A demo of tags](/tags-demo.png)

It's a topic which is interesting to me and also a cool idea that I might revisit and explore in the future.

I also really like links in Obsidian. A few days ago, I had been diving deep into purple coloured stones because they look really cool. So I created a note titled "Purple Stones" to keep track of my research. In the "Purple Stones" note, I made a list of all the purple stones that caught my eye with a short description of each of them. But instead of cramming detailed information for each of the stones, I created a separate note dedicated to each stone with all the information I got from my research. 

So now, when I click on any stone's name in the "Purple Stones" note, it takes me to its dedicated note where I can immerse myself in all the information about that particular stone.

I was also on the hunt for cool desk decorations and created a note for it. As I was researching common desk decorations I came across the idea of using beautiful rocks as decorations. So I instantly linked my note on amethyst because raw amethyst looks stunning. Obsidian also has a really cool backlinks feature, whenever I visit my amethyst note, I can also see a list of all the other notes where amethyst was mentioned. It's like having a web of interconnected knowledge!

Links have become a huge part of my Obsidian workflow. Each note leads to even more pathways of things I've researched, ideas I've had, or cool things I've discovered. It's as if my notes have formed a collection of interconnected nodes, guiding me through my exploration of different topics and keeping everything neatly organised.

### What I Take Notes Of

I take notes of pretty much everything.

- Any idea that comes to mind
- Anything interesting I come across
- Videos or blog posts that make me think, I break down the key points
- Cool thoughts and random musings
- Research on various topics
- Planning blog posts and events

Also Obsidian is simply the best Markdown editor I have ever used so I just use it for writing anything.

### How I Navigate Notes

As I had written in the previous section, links really help in exploring and guiding you through your notes. It's like having interconnected nodes of knowledge I had said. Well Obsidian has this really feature called "Graph View" which lets you visualise your entire vault. Each note becomes a node and these nodes are connected to each other using the links you create.

![A look at the Graph View](/graph-view.png)

In the Graph View you can easily search for everything, including notes, tags, and also visualise how your notes are linked.

![A screenshot of my blog graph](/blog-graph.png)

I have heard some people saying that the Graph View is not useful, but I find it to be a natural and intuitive way to navigate my notes. It's much better than the regular search experience for me.

To make note navigation even faster and more efficient, I use a plugin called [Omnisearch](https://github.com/scambier/obsidian-omnisearch). It enhances the search functionality in Obsidian with OCR and a smart weighting algorithm. Plus, it supports vim keybindings, which I love. It reminds me of the [Telescope](https://github.com/nvim-telescope/telescope.nvim) plugin in Neovim. 

### Syncing Notes

Syncing notes across in Obsidian can be done in different ways. While Obsidian offers a paid [Sync](https://obsidian.md/sync) service for seamless synchronisation across devices, I personally use a different approach since I cannot afford it at the moment.

Since Obsidian stores notes as local files in a folder, you can easily sync them using cloud storage services like [Google Drive](https://google.com/drive) or [Dropbox](https://dropbox.com). Another option is using [Syncthing](https://syncthing.net/) which is what I use. It's an open-source, encrypted file synchronisation program. I find Syncthing convenient because it allows me to sync my files locally between my Mac and Android phone without sending data over the internet. It's a simple and secure solution for keeping my notes in sync across devices. I really like it.

### Publishing Notes

When I used to use [Notion](https://notion.so), I loved the publish feature that allowed me to share notes easily with a link. Obsidian also offers a similar feature through its paid [Publish](https://obsidian.md/publish) service, but it's not within my budget. So, I decided to create my own Obsidian publish solution using [Rust](https://rust-lang.org). It's a command-line tool that scans my Obsidian vault for notes with `publish: true` in the metadata (similar to the official Publish plugin). It then converts the Markdown notes to HTML and deploys them to the internet. While I'm still refining the static site generator, my plan is to open-source it once it's ready for broader use. This way, others can benefit from it as well.

### Plugins

I use just three plugins:

- Minimal Theme Settings, which is the plugin to configure the [Minimal Theme](https://minimal.guide) for a clean and minimalistic UI.
- [OmniSearch](https://github.com/scambier/obsidian-omnisearch), which is a better and quicker search.
- [FuzzyTag](https://github.com/adriandersen/obsidian-fuzzytag), which provides autocomplete for tags while writing them in the frontmatter.

Hopefully this shows that you don't need ten different plugins to make Obsidian functional. It's already enough for whatever you want to do.

## Tasks App: Todoist

When it comes to managing tasks, I prefer to keep my notes and tasks separate. While some people might use Obsidian for todo-lists, I find it more comfortable to use a dedicated task app.

My go-to task app is [Todoist](https://todoist.com/). [Despite todo apps being broken](https://frantic.im/todo-for-robots/), Todoist *works fine*. It has a nice UI which allows for adding tasks quickly, even when on the go, thanks to its convenient widget. It has excellent natural language processing, it understands dates and times in whatever broken english I use.

![A demo of Todoist's excellent NLP](/todoist-nlp.png)

I particularly enjoy the satisfying sound it plays when I complete a task. Todoist's sub-tasks feature is incredibly useful for breaking down complex tasks into smaller, more manageable steps, which also happens to be perfect for shopping lists and check lists.

I also use Todoist as a reminders app. A few days ago, I needed to wish a friend a safe journey for their upcoming long-distance travel, so I added a reminder in Todoist a week in advance, ensuring that I won't forget to send my well-wishes on the day.

## Calendar App: Cron

[Cron](https://cron.com) is my preferred Calendar app. It syncs with [Google Calendar](https://calendar.google.com/calendar/u/0/r) and features a clean and intuitive UI to for quickly creating and organising events. It offers all the features you'd expect from a standard calendar app but with the added benefits of being keyboard-friendly, visually appealing, and it feels *fast*.

While Cron doesn't have an official Android app yet, I find that the Google Calendar app works fine. I really like the widget it provides and use it to stay updated with my schedule at a glance.


Thank you!