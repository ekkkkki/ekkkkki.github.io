# Personal homepage — Yichong (Eric) Zhao

A static, single-page academic homepage. No build step, no framework — just
`index.html` + `assets/`. Edit the files directly and push.

## Live preview locally

```bash
cd personal_hp
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy to GitHub Pages (user site)

Intended to live in a repo named **`ekkkkki.github.io`**, served at
`https://ekkkkki.github.io/`.

```bash
git init -b main
git add -A
git commit -m "Add personal homepage"
gh repo create ekkkkki.github.io --public --source=. --remote=origin --push
```

Then in the repo: **Settings → Pages → Build and deployment → Source: Deploy from a branch**,
branch `main` / `/ (root)`. The site goes live in a minute or two.

## Assets / photo

- The circular avatar is `assets/profile.jpg` (a square crop of the original).
- The uncropped original is kept locally as `assets/profile.jpeg` but is
  **git-ignored**, so it is not published. To re-crop, edit the box in the
  crop snippet and regenerate `profile.jpg`.
- The CV PDF is intentionally **not** included on the site.

## Customize

- **Colors / fonts** — CSS variables at the top of `assets/style.css`
  (`--accent`, `--bg`, fonts, …). Dark mode is automatic via `prefers-color-scheme`.
- **Content** — all text lives in `index.html`, organized into clearly labeled
  `<section>` blocks (About, Publications & Talks, Experience, Education, Projects, Honors).
