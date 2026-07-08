# armory-terminal-web

A gun locker terminal built with zero styling. Stats, specs, and nothing to hide behind.

**ARMORY TERMINAL** is a multi-page, game-style weapon loadout database — a pure-HTML5
structure exercise. There is **no CSS and no JavaScript** anywhere in the project: no
`.css` files, no `<style>` blocks, no `style="..."` attributes, and no `<script>` tags
(the only embedded third-party markup is the YouTube and Google Maps `<iframe>`s). The
pages render with the browser's default look on purpose — the focus is clean, semantic
HTML structure.

## Pages

| File | What it is |
|------|------------|
| `index.html` | Landing page — logo, category index table, and links to every rack |
| `pistol.html` | Pistol rack (4 weapons) |
| `smg.html` | SMG rack (4 weapons) |
| `assault-rifle.html` | Assault Rifle rack (4 weapons) |
| `sniper-rifle.html` | Sniper Rifle rack (4 weapons) |
| `shotgun.html` | Shotgun rack (4 weapons) |
| `lmg.html` | LMG rack (4 weapons) |
| `about.html` | Armory HQ — mission, location map, section directory, references |

Every category page carries an `h1`–`h6` heading structure, a comparison `<table>`, a
local SVG image per weapon, a YouTube showcase embed, external reference links, and
prev / next / home navigation. The category pages are linked in a ring
(Pistol → SMG → Assault Rifle → Sniper Rifle → Shotgun → LMG → back to Pistol).

## Structure

```
armory-terminal-web/
├── index.html
├── pistol.html
├── smg.html
├── assault-rifle.html
├── sniper-rifle.html
├── shotgun.html
├── lmg.html
├── about.html
├── README.md
└── assets/
    └── images/
        ├── armory-logo.svg
        ├── cat-*.svg          # 6 category icons
        └── <weapon>.svg       # 24 weapon silhouettes
```

All images are **local SVG files** referenced with relative paths, so the project works
offline and survives being zipped up and opened on another machine.

## How to open

No build step and no server needed. Just open `index.html` in any web browser
(double-click it, or drag it into a browser window) and follow the links from there.

> The YouTube and Google Maps embeds are the only parts that need an internet connection
> to display; everything else works fully offline.
