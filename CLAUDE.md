# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose

Personal scratch repo for sharing standalone HTML snippets/pages via GitHub Pages (public repo `LukeZHarris/pages`). Each `.html` file at the root is an independent, self-contained page — there is no shared build, framework, or dependency between them.

## Deployment

Pushing to `main` triggers `.github/workflows/pages.yml`, which runs a Jekyll build (`actions/jekyll-build-pages`) and deploys the result via GitHub Pages. There is no `Gemfile` — the workflow uses the default Jekyll build with `theme: jekyll-theme-minimal` (`_config.yml`).

- Any `.html` file added at the repo root is picked up automatically and copied through as-is (no Liquid front matter is used in existing pages), landing at `https://lukezharris.github.io/pages/<filename>.html` after deploy.
- There's no local build/test/lint step — verify a page by opening the `.html` file directly in a browser before pushing.
- Workflow actions are pinned to commit SHAs (not tags) — preserve that pattern if updating `.github/workflows/pages.yml`.

## Working conventions

- Pages are self-contained: inline `<style>`/`<script>`, no external build tooling, no shared assets directory.
- Because the repo is **public**, check any new page for sensitive content (real tenant/customer names, internal hostnames, credentials) before pushing.
- `index.html` is a minimal placeholder landing page, not a real index of contents — don't assume it needs to link every page added here.
