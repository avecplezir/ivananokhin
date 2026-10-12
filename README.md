# Quarto Personal Site Starter (Ivan)

## Quick start
1. Install Quarto: https://quarto.org/docs/get-started/
2. In this folder:
   ```bash
   quarto render
   quarto preview
   ```
3. Initialize a repo and push to GitHub:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo>.git
   git push -u origin main
   ```
4. Enable GitHub Pages in repo Settings → Pages → "Deploy from a branch" → `gh-pages` (after first publish)

### Publish options
- **Option A (CLI):**
  ```bash
  quarto publish gh-pages
  ```
- **Option B (GitHub Actions):** keep `.github/workflows/quarto-publish.yml` and enable Pages to serve from the `gh-pages` branch created by the workflow.

The workflow builds from source on each push to `main`. Commit source pages, configuration, and assets; `_site/`, `.quarto/`, and `.DS_Store` files stay local and are ignored by Git. Only `.qmd` pages are rendered, so repository documentation is not published.

The `website.site-url` setting in `_quarto.yml` controls the public base URL. Quarto uses it to generate `sitemap.xml` and `robots.txt` on every full build; update that setting if the site moves.

## Customize
- Replace `images/me.jpg` with your photo (keep same name).
- Edit `_quarto.yml` for navbar, theme, social links.
- Put your BibTeX entries into `publications.bib`.
- Add posts under `posts/` (each post gets its own folder with `index.qmd`).

## Netlify (optional)
If you prefer Netlify, add a site with build command `quarto render` and publish directory `_site`.
