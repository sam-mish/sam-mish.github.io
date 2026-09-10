# Portfolio site

A minimal Jekyll site, hosted free on GitHub Pages. No build tooling required —
GitHub builds it for you on every push.

## One-time setup

1. Create a GitHub repo named exactly `yourusername.github.io`.
2. Push everything in this folder to that repo (see commands below).
3. In the repo's **Settings → Pages**, set the source to the `main` branch,
   root folder. Save. Your site goes live at `https://yourusername.github.io`
   within a minute or two.
4. Edit `_config.yml`: set `title`, `url`, `email`, `github_username`.
5. Add a profile photo at `assets/img/profile.jpg`.
6. Add your resume as `assets/resume.pdf`.
7. Edit `index.md` (About) and `resume.md` (Experience/Education/Skills) with your own text.
8. Delete the example project in `_projects/` once you've added your own.

```bash
cd site
git init
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git add .
git commit -m "Initial site"
git branch -M main
git push -u origin main
```

## Adding a new AI project (the whole point)

Create a new file in `_projects/`, named `YYYY-MM-DD-short-title.md`:

```markdown
---
title: "Project Title"
date: 2026-03-01
tags: [Python, LLMs]
image: /assets/img/your-thumbnail.jpg
description: "One-line summary for the project card."
links:
  - label: "View on GitHub"
    url: "https://github.com/yourusername/repo"
---

Write the project writeup here in Markdown.
```

Commit and push. The project appears on `/projects/` automatically, newest first,
and gets its own page at `/projects/short-title/`. Nothing else to edit.

## Adding photos to the gallery

Drop an image file (`.jpg`, `.jpeg`, `.png`, or `.webp`) into `assets/gallery/`,
commit, push. It appears on `/gallery/` automatically — no file needs editing.

## Previewing locally (optional)

Requires Ruby installed.

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`.
