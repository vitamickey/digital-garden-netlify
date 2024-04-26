---
{"dg-publish":true,"permalink":"/digital-garden-overhaul-with-obsidian-plugin/","title":"Digital Garden overhaul with Obsidian Plugin","tags":["technology","website","coding"],"created":"2023-10-05","updated":"2024-04-25"}
---

2024-04-25

I figured out that it was quite easy to duplicate my Hugo website repo into a new one with a more suitable/descriptive name, freeing up my digital garden repo for something new. I just had to make sure I didn't mess up the submodules into the GitHub pages repo, but I figured it all out and my website isn't broken so that's good.

In terms of the actual overhaul on my digital garden, I'm pretty close to just [[Making my own Obsidian Theme\|Making my own Obsidian Theme]] in order for the website to work exactly how I want it, but for now, I am relatively satisfied with all the tweaking I've done to the [[CSS\|CSS]]. I really want to learn how to make [[Nunjucks\|Nunjucks]] scripts, so I can add different things to each note, but I have a small problem in that I don't uhhhh even know how to write [[JavaScript\|JavaScript]].

It currently runs with [[Minimal (Obsidian Theme)\|Minimal (Obsidian Theme)]], using colours taken from [[Primary (Obsidian Theme)\|Primary (Obsidian Theme)]]. The main issue is that I can't figure, based on the website set-up, how to make the 404 pages take on my custom CSS attributes, as it just takes them from the Obsidian theme you've decided to use, and the 404 page doesn't even load up the custom CSS.

## A weird workaround

There seems to be some error where the `dg-home` property thinks that your homepage note is updated every time you open the publication centre. Additionally, every time you update the note and republish it, a script adds the `gardenEntry` tag, in order to signal to the website to give the note the home contents appearance. To fix this, I simply changed the note to have the `gardenEntry` tag and removed the `dg-home` property.

---

Okay so, Apparently, the [Obsidian Digital Garden](https://github.com/oleeskild/Obsidian-Digital-Garden) plugin exists. Which means I'm gonna change my Hugo website to be more like a personal website and see if I can run the the [[Digital garden\|Digital garden]] website off a sub-link from the main website. So, the base URL for the digital garden being `michaelacheong.com/notes`, or something like that.

However, a couple of issues.

1. My current `digital-garden` repo contains the Hugo site and its code, as well as the subfolder `public` which links to my `vitamickey.github.io` Github pages repo.
  1. I would like to replace the `digital-garden` repo with an actual digital garden.
  2. I would like to move the Hugo code onto a repo called `hugo-site` or something to that effect. This includes the fact that...
    1. Everything from `digital-garden` needs to move to the new repo
    2. The submodule connected to `public` needs to move cleanly as well.
      1. https://stackoverflow.com/questions/4604486/how-do-i-move-an-existing-git-submodule-within-a-git-repository
2. My current existing Obsidian vault needs to be force pushed onto my now renamed digital-garden repo for my private notes
  1. https://stackoverflow.com/questions/51275223/how-to-overwrite-remote-git-repository-with-a-new-local-project
    1. "In case some other git noob comes around, these are the exact steps I took: In the new local repository: `git init` , `git add --all`, `git remote add origin <remote url>`, `git commit -m "some comment"`, `git push -f origin main"

To do:

- [ ] Open graph?
  - [ ] https://www.freecodecamp.org/news/what-is-open-graph-and-how-can-i-use-it-for-my-website/
