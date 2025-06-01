---
{"dg-publish":true,"permalink":"/obsidian-digital-garden-plugin/","title":"Obsidian Digital Garden Plugin","tags":["technology","website"],"created":"2024-05-16","updated":"2024-05-16"}
---

Via https://github.com/oleeskild/Obsidian-Digital-Garden)

## Notes on and wishlist for the plugin

- errors
	- `dg-home` is BAD, it adds `gardenEntry` tag each time it uploads, and is always indicated as a modified note. very janky behaviour.
		- troubleshoot: set tag on the `dg-home` note as `gardenEntry` to avoid strange behaviour
	- scrollbar is blocked by navbar. you cannot click on scrollbar at the top right.
	- 404 pages only take the attributes of the theme you used to generate the website. So, if you want to redesign the 404 pages with custom CSS, legit no idea how to make this happen. I've even tried to replicate results from other digital garden examples, to no avail
		- workaround: I am making [[Making my own Obsidian Theme\|my own theme]] LOL
- wishlist
	- `gardenEntry` show title pls :( maybe I can find out how to do this from someone else's repo

To do:

- [ ] [https://wisdump.work/blog-management/digital-garden-management/protecting-your-identity-and-your-domain-with-email-security/](https://wisdump.work/blog-management/digital-garden-management/protecting-your-identity-and-your-domain-with-email-security/)
- [ ] 
- [ ] Open graph?
    - [ ] [https://www.freecodecamp.org/news/what-is-open-graph-and-how-can-i-use-it-for-my-website/](https://www.freecodecamp.org/news/what-is-open-graph-and-how-can-i-use-it-for-my-website/)
- [ ] 

## Useful resources

- [Troubleshooting Digital Gardens](https://wisdump.work/blog-management/digital-garden-management/troubleshooting-digital-gardens/)
- 

## Code snippets

Scrollbar buttons (abandoning bc the html is weird and doesn't let you click on the buttons lol) from [here](https://stackoverflow.com/questions/70879021/how-to-custom-scroll-bar-with-default-arrow-in-css).

```
@media (min-width: 767px) {    
    /* Buttons */
    
    ::-webkit-scrollbar-button:single-button {
      background-color: var(--color-base-30);
      display: block;
      border-style: solid;
      height: 13px;
      width: 16px;
    }
    
    
    /* Up */
    
     ::-webkit-scrollbar-button:single-button:vertical:decrement {
      border-width: 0 8px 8px 8px;
      border-color: transparent transparent var(--color-base-40) transparent;
    }
    
     ::-webkit-scrollbar-button:single-button:vertical:decrement:hover {
      border-color: transparent transparent var(--color-base-50) transparent;
    }
    
    /* Down */
    
     ::-webkit-scrollbar-button:single-button:vertical:increment {
      border-width: 8px 8px 0 8px;
      border-color: var(--color-base-40) transparent transparent transparent;
    }
    
     ::-webkit-scrollbar-button:vertical:single-button:increment:hover {
      border-color: var(--color-base-50) transparent transparent transparent;
    }
    
    
    /* Track */
    
    ::-webkit-scrollbar-track {
        background-color: var(--color-base-10);
    }
    
}

```
