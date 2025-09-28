# Seth D. Thorn — CV (GitHub Pages + PDF)

This repo hosts a single-source CV in Markdown and publishes it as:
- **Web**: GitHub Pages (Jekyll). Embed in Squarespace via an `<iframe>`.
- **PDF**: Built automatically via GitHub Actions (Pandoc) and attached as a workflow artifact.

## Quick Start

1. Create a new GitHub repo and upload these files.
2. In `.github/workflows/Build and Deploy GitHub Pages`, GitHub will publish to Pages on push.
3. Enable **Settings → Pages → Build and deployment → GitHub Actions**.
4. After each push, grab the **cv.pdf** artifact from the **Generate CV PDF artifact** workflow.

### Squarespace Embed (Code Block)
Replace `USERNAME` and `REPO`:

```html
<iframe src="https://USERNAME.github.io/REPO/" style="width:100%; height:2200px; border:0;" loading="lazy"></iframe>
```

### Editing
- Edit `index.md` as your single source of truth.
- The site theme/layout is in `_layouts/cv.html`. Print rules are included so printing from the browser yields a clean PDF as well.
