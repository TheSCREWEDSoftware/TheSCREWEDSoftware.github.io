# TheSCREWEDSoftware.github.io

My GitHub Pages site: <https://thescrewedsoftware.github.io/>. A home page (`index.html`) that links to my
projects, plus the web tools that need to be online, each in its own folder.

Projects with their own repository publish their own pages (Settings > Pages in that repository) and appear under
this address without being copied here:

| Project | Repository | Online at |
| --- | --- | --- |
| World Randomizer pages | `mod-world-randomizer-website` | `/mod-world-randomizer-website/` |

## Putting it online (once)

1. On GitHub, create a **public** repository named exactly `TheSCREWEDSoftware.github.io` (no README, it is here).
2. In this folder:

   ```sh
   git remote add origin https://github.com/TheSCREWEDSoftware/TheSCREWEDSoftware.github.io.git
   git push -u origin main
   ```

3. Repository **Settings > Pages**: Source "Deploy from a branch", branch `main`, folder `/ (root)`. The site is
   up a minute or two later.

`.nojekyll` makes GitHub serve the files as they are (no Jekyll build).

## Updating the World Randomizer pages

Nothing to do here: push `mod-world-randomizer-website` (the module's `web/` submodule) and GitHub Pages updates
`/mod-world-randomizer-website/` by itself. The cards in `index.html` link there.

## Adding another project

1. Copy its web page(s) into a new folder here, e.g. `arma-3-preset-comparator/` (with its own `index.html`).
2. Add a card for it in `index.html`, under "Web tools", linking to `arma-3-preset-comparator/`.
3. Commit and push. It is online at `https://thescrewedsoftware.github.io/arma-3-preset-comparator/`.

A project can also publish its own site from its own repository (Settings > Pages there): it then appears at
`https://thescrewedsoftware.github.io/<repository name>/` without being copied here.
