# clickwiseowl.com

The Click Wise Owl website. One static page, no build step, no framework.

## Files

| File | What it is |
|---|---|
| `index.html` | The entire site — HTML, CSS and JS in one file |
| `clickwiseowl-logo.png` | Owl logo, 600×600, used in the "Sobre mí" section |
| `clickwiseowl-logo-horizontal.png` | Header logo, 451×138, used in the nav bar |

## How it is published

Push to `main` → the connected host rebuilds automatically. **Never deploy by dragging a
folder.** A drag replaces the whole site and deletes anything not in the folder; a push
changes only what changed.

## Where everything lives

- **Code:** this repository
- **Host:** Netlify, project `clickwiseowl` (site id `0a81493b-df15-48ae-9bbc-3293e6035941`)
- **Domain:** clickwiseowl.com, DNS managed by Netlify (NS1 nameservers)
- **Contact number on the site:** +502 5377 1248 (WhatsApp)

## Known issue — logos are borrowed

The two `<img src="...">` tags currently point at a **frozen Netlify deploy**:

    https://6a7d42bcadcaf6f0622a927e--clickwiseowl.netlify.app/clickwiseowl-logo.png
    https://6a7d42bcadcaf6f0622a927e--clickwiseowl.netlify.app/clickwiseowl-logo-horizontal.png

This was a workaround from 26 Aug 2026 — the PNG files could not be moved into the deploy
folder, and a Netlify drag-drop would have deleted the originals. It works and is stable
(Netlify keeps historical deploys), but it is not the end state.

**To fix:** put the two PNG files in this folder, change both `src` attributes back to plain
filenames (`clickwiseowl-logo.png` and `clickwiseowl-logo-horizontal.png`), commit and push.

## Language toggle

The page is bilingual in one file. Every translated string is a pair:

    <span data-es>Texto</span><span data-en>Text</span>

CSS hides `[data-en]` by default; the `toggleLang()` function adds an `en` class to `<html>`
which flips which half shows. The choice is remembered in localStorage. If you add new copy,
add BOTH spans or that text vanishes in one language.

## Pricing shown on the page (as of 26 Aug 2026)

- Sitio profesional — Q5,500 one-time
- Sitio + agenda — Q9,500 one-time (marked "Más solicitado")
- Bot de WhatsApp — Q3,500 one-time
- All with Q250/mes hosting and support; custom work "desde Q25,000"
