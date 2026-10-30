# TheSCREWEDSoftware.github.io

My GitHub Pages site: <https://thescrewedsoftware.github.io/>. A home page (`index.html`) that links to my
projects, plus the web tools that need to be online, each in its own folder.

| Folder | What | Online at |
| --- | --- | --- |
| `world-randomizer/` | Character roller, world map and config update of mod-world-randomizer | `/world-randomizer/` |

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

From the module (`modules/mod-world-randomizer`):

```sh
tools/publish_web.sh "<path to this folder>"
```

It copies the module's `web/` here as `world-randomizer/`. Then commit and push this repository.

The world map shows the zone outlines on a plain background here: the map pictures come from an aowow install,
which GitHub Pages doesn't have.

## Adding another project

1. Copy its web page(s) into a new folder here, e.g. `arma-3-preset-comparator/` (with its own `index.html`).
2. Add a card for it in `index.html`, under "Web tools", linking to `arma-3-preset-comparator/`.
3. Commit and push. It is online at `https://thescrewedsoftware.github.io/arma-3-preset-comparator/`.

A project can also publish its own site from its own repository (Settings > Pages there): it then appears at
`https://thescrewedsoftware.github.io/<repository name>/` without being copied here.
