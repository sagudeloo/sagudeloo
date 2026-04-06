# OpenCode Instructions

## Project Overview
The repository is intended to host a portfolio website that will be published via **GitHub Pages**.

- The site will live in a dedicated folder (e.g. `website/` or `docs/`).
- All static assets should reside inside this folder – no code outside of it will be served.

## Key Commands
These commands are the minimal set that an agent would otherwise guess incorrectly:

1. **Create site folder** (if not already present)
   ```bash
   mkdir website
   cd website
   # Add your index.html, CSS, images, etc.
   ```
2. **Add and commit changes/**
   ```bash
   git add website/
   git commit -m "Add portfolio site"
   ```
3. **Publish to GitHub Pages (default branch)** – If you prefer the default `main`‑branch flow:
   ```bash
   # Ensure the repo settings have “GitHub Pages → Source: main” enabled.
   git push origin main
   ```
4. **Publish to a dedicated `gh-pages` branch** – if you want the site isolated from source code:
   ```bash
   git checkout -b gh-pages
   # (Optional) Copy or symlink your website files into this branch
   git add .
   git commit -m "Deploy portfolio"
   git push -u origin gh-pages
   ```
5. **Local preview** – if you use a static site generator, run its dev server (e.g., `hugo serve`, `jekyll serve`).

## GitHub Settings Checklist
- In the repo settings → *Pages*, set the source to the folder that contains your site (`/website` or `/docs`) or to the `gh-pages` branch.
- Ensure **Enforce HTTPS** is enabled for security.

## Common Gotchas
- **Branch name mismatch:** The GitHub Pages UI may still point to an old branch; double‑check the selected source after pushing.
- **Missing index file:** Without an `index.html`, GitHub Pages will return a 404.
- **Cache issues:** If changes are not visible immediately, clear browser cache or use incognito mode.

---

> *This file is meant to be read quickly by an OpenCode agent. Keep it concise and only include commands that are non‑obvious.*