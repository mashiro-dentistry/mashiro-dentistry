# 真白牙科 Mashiro Dentistry

Website for Mashiro Dentistry, built with [Hugo](https://gohugo.io/) and a custom light/white/blue theme. Deployed to GitHub Pages via GitHub Actions on every push to `main`.

## Editing content

All visible text lives in markdown under `content/`:

| File | Page |
|------|------|
| `content/about.md` | 關於我們 |
| `content/services/*.md` | 服務項目 (one file per service category) |

Clinic-wide details (name, WhatsApp number, address, opening hours) are set once in `hugo.toml` under `[params]` and reused everywhere.

Each service category file has front matter:

```yaml
title: 基本牙科
weight: 10          # ordering
icon: tooth-check   # icon name from layouts/partials/icons.html
summary: one-line description
items:              # shown as numbered cards on the services page
  - 洗牙
  - 補牙
```

## Local preview

```bash
hugo server
```

## Deploy

Push to `main` — the GitHub Actions workflow builds and publishes automatically.
