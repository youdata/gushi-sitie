# 古詩四帖 · Four Ancient Poems — a scroll atlas

张旭（传）《古诗四帖》 — a narrated deep-zoom reading, as a static page (in Chinese).

Four Ancient Poems, the cursive handscroll attributed to Zhang Xu, with its colophons: three photographs of the scroll joined on one canvas, the four poems and the colophons' own words.

Live: https://youdata.github.io/gushi-sitie/

The image pyramids are tile folders (`gushi-sitie-1/`, `gushi-sitie-2/`, `gushi-sitie-3/`: `header.idx` + `{z}/{x}/{y}.png`), so any static host serves them.
Its fonts are in `fonts/`, trimmed to the page's characters. The narrated video is not included.

## How it is made

From `infographic-examples/gushi-sitie-atlas/build.mjs` (the page) with rx (`~/rx-cli`):

```sh
node build.mjs                                                     # → gushi-sitie-atlas.json
rx export gushi-sitie-atlas.json --out site --app /rx-graphic-editor/web/index.html --canvas --theme dark --lock-layers --tiles dir
rx publish site --to github:youdata/gushi-sitie --yes
```
