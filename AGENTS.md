# Repository Guidelines

## Project Structure & Organization
- Source pages: `index.qmd` (home), `publications.qmd`, posts in `posts/<slug>/index.qmd`.
- Assets: `images/` for media; bibliographic data in `publications.bib`.
- Config: `_quarto.yml` controls site metadata, nav, and formats.
- Build output: `_site/` (published site). Build cache: `_freeze/`.

## Build, Preview, Publish
- `quarto preview`: Run a local server with live reload at a local port.
- `quarto render`: Build the full site into `_site/`.
- `quarto check`: Verify required tooling and reveal missing dependencies.
- Tip: Commit source (`*.qmd`, `images/`, `_quarto.yml`), not `_site/` unless your deploy strategy requires it.

## Coding Style & Naming
- Content: Write in `.qmd` with YAML front matter (`title`, `date`, `categories`).
- Indentation: 2 spaces for YAML and nested Markdown lists/code.
- Slugs: Hyphenated lowercase (e.g., `posts/hello-world/index.qmd`).
- Media: Place under `images/`, use descriptive names, add alt text.
- Headings: Use sentence case; keep levels consistent (`#`, `##`, `###`).

## Testing & Validation
- Build cleanly: `quarto render` should complete without errors/warnings.
- Link/content sanity: Use `quarto preview` to manually verify navigation, code blocks, and citations.
- Environment: Run `quarto check` after upgrades or on new machines.

## Commit & Pull Request Guidelines
- Commits: Prefer Conventional Commits (e.g., `docs: add post on X`, `fix: correct broken link`).
- PRs: Include a concise description, screenshots for visual changes, and link related issues.
- Verification: Show that `quarto render` succeeds locally; note any config changes in `_quarto.yml`.

## Security & Configuration Tips
- Do not commit secrets or API keys; this site should be static.
- Keep `_quarto.yml` minimal and documented; add comments near non-obvious options.
- Large assets: optimize images before adding to keep builds fast.

