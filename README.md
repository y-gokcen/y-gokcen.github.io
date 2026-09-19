# yasemin.gokcen.me

Personal academic site for Yasemin Gokcen. Plain HTML and CSS, no build step, hosted on GitHub Pages.

- `index.html` — the whole site: one page whose sections (About, Research, Publications, Talks & Posters, Code, Experience, Education) are shown one at a time by the tab bar; a small script at the bottom of the file switches them and keeps the URL hash (`#research`, `#presentations`, …) in sync, so section links can be shared
- `favicon.svg` — tab icon
- `style.css` — styles (light/dark via `prefers-color-scheme`)
- `cv/` — current resume PDF
- `posters/` — conference posters and talk slides (PDF)
- `img/` — first-page thumbnails of each poster (`pdftoppm -jpeg -f 1 -l 1 -scale-to 900`)
- `CNAME` — custom domain for GitHub Pages

To update: edit `index.html`, commit, push. Pages redeploys within a minute.

To add a poster: put the PDF in `posters/`, make a 900-px-wide first-page thumbnail in `img/` (wide slides look best letterboxed onto a 4:3 white canvas), and copy one of the `<div class="card">` blocks in the Talks & Posters section.

On phones the header and tab bar stay fixed and only the active section scrolls; that behavior lives in the `@media (max-width: 560px)` block of `style.css`.
