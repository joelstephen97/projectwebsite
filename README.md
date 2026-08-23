# projectwebsite

My first personal website: a single static HTML page with a hero, an About Me section, an experience list and a CV download, styled with one CSS file and Bootstrap from a CDN.

![HTML](https://img.shields.io/badge/html-static-orange) ![License](https://img.shields.io/badge/license-GPL--3.0-blue)

## Why

I started this repo in early 2020 (it was originally named `joelstephen97.github.io`) as a place to have a web presence while looking for my first jobs, and kept editing it until July 2023. It went through a few rewrites: the 2020 `home.html` draft, a 2022 Bootstrap layout with a nav and CV button, and a 2023 pass that added the low-poly SVG background, a footer and a mobile breakpoint. After that I moved to a React site at https://joelstephen.vercel.app and stopped touching this one.

It stays public as a snapshot of what my CV and front-end skills looked like at the time, and because a zero-build HTML/CSS page is still the quickest way to put a one-page profile online.

## Quickstart

There is no build step.

```bash
git clone https://github.com/joelstephen97/projectwebsite.git
cd projectwebsite
python -m http.server 8000
# open http://localhost:8000
```

Opening `index.html` directly in a browser also works (the CSS and background use relative paths). Bootstrap, the Font Awesome kit and the Poppins font load from CDNs, so icons and fonts need internet access.

## Usage

To reuse it as your own one-pager:

1. Edit the text in `index.html` (hero, About Me, Experience, footer links).
2. Replace `CV.pdf` with your own; the "Download CV" button points at it.
3. Tweak colours and spacing in `CSS/style.css`. The mobile layout is the `@media (max-width: 1050px)` block at the bottom.
4. Push to any static host (GitHub Pages, Netlify, Vercel).

## How it works

`index.html` is one page with anchor links (`#about-me`, `#experience`) in the nav. Layout uses Bootstrap 5 grid classes; everything else (typography, hero, nav, footer, breakpoint) is in `CSS/style.css`. `poly.svg` is the tiled page background. `CV.pdf` is the 2023 CV as linked from the hero. `me.jfif` is a profile photo from an earlier layout that is no longer referenced.

## Status and limitations

- Frozen since July 2023. The experience section is a snapshot from then and is out of date; the live CV and site are at https://joelstephen.vercel.app.
- Single page, no JavaScript, no dark mode, no analytics.
- Depends on three CDNs (jsDelivr for Bootstrap, kit.fontawesome.com, Google Fonts).
- `.hintrc` is a webhint config from when I ran the VS Code webhint extension; it is not needed to view the site.

## License

GPL-3.0, see [LICENSE.md](LICENSE.md).
