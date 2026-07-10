# pages

HTML snippets to share, hosted via GitHub Pages.

## How to publish a page

1. Drop a self-contained `.html` file (inline `<style>`/`<script>`, no external build tooling) at the repo root.
2. Commit and push to `main`.
3. `.github/workflows/pages.yml` runs a Jekyll build and deploys automatically — no local build/test step.
4. The page goes live at `https://lukezharris.github.io/pages/<filename>.html`.

**Note:** this repo is public — check new pages for sensitive content (real tenant/customer names, internal hostnames, credentials) before pushing.
