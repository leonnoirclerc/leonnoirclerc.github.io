# leonnoirclerc.github.io

[![Deploy](https://github.com/leonnoirclerc/leonnoirclerc.github.io/actions/workflows/publish.yml/badge.svg)](https://leonnoirclerc.github.io)

> **My personal website is live at → <https://leonnoirclerc.github.io>**

Source code for my personal site — research notes, experiments, and projects. Built with [Quarto](https://quarto.org), deployed to GitHub Pages via Actions.

## Local development

Requires Quarto:

```sh
brew install --cask quarto
```

Then from this directory:

```sh
quarto preview          # live-reload server on http://localhost:4000
quarto render           # one-shot render to _site/
```

## Writing a post

Posts live under `posts/<slug>/index.qmd`. Use a folder per post so figures and notebooks can sit next to the prose. Frontmatter:

```yaml
---
title: "Post title"
description: "One-line summary that shows in listings and OpenGraph."
date: "YYYY-MM-DD"
categories: [tag1, tag2]
---
```

## Adding a project

Projects live under `projects/<slug>/index.qmd`. Same frontmatter, plus an `image:` field for the grid card.

## Deploy

Push to `main`. The workflow at `.github/workflows/publish.yml` renders and pushes `_site/` to the `gh-pages` branch, which GitHub Pages serves at <https://leonnoirclerc.github.io>.
