# Seth D. Thorn — CV Site

This repository hosts my **academic/creative CV**, published via GitHub Pages.  
The site and a downloadable PDF are generated automatically using GitHub Actions.

---

## Live Links

- **Web version:** https://seth-thorn.github.io/cv/  
- **PDF version:** https://seth-thorn.github.io/cv/cv.pdf  

---

## Build & Deployment Pipeline

Each push to `main` triggers this workflow:

1. **Jekyll build** — the site is compiled into `_site/`  
2. **Puppeteer PDF render** — the HTML version is converted to `cv.pdf`  
3. **Assembly** — `_site/` contents and `cv.pdf` are copied into a writable folder  
4. **Publish** — the folder is uploaded and deployed via GitHub Pages  

Because of this, you only ever need to edit one file:

- `index.md` — the master CV source in Markdown  
- Supporting CSS or layout tweaks live in `assets/` or `_layouts/cv.html`

---

## Editing Instructions

- Update **only** `index.md` when you change appointments, publications, etc.  
- Create / edit CSS under `assets/css/print.css` or override in `_layouts/cv.html` for styling.  
- If you ever tweak the layout/design, do so in `_layouts/cv.html` — the PDF render mirrors that HTML.

To trigger a rebuild:
```bash
git add .
git commit -m "Update CV content"
git push origin main
