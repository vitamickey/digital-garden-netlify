---
{"dg-publish":true,"permalink":"/digital-garden-overhaul-with-obsidian-plugin/","title":"Digital Garden overhaul with Obsidian Plugin","tags":["technology","website","coding"],"created":"2023-10-05","updated":"2024-02-19"}
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
