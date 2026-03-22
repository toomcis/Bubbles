# Bubbles — Web UI

This branch hosts the interactive web preview for [Bubbles](https://github.com/toomcis/Bubbles), live at **[bubbles.toomcis.eu](https://bubbles.toomcis.eu)**.

It is deployed via Cloudflare Pages and is separate from the main branch, which contains the plain Lively Wallpaper files.

---

## What's in this branch

```
Bubbles/webUI
├── index.html     # Landing page — live preview, install guide, property reference
└── bubbles.html   # The raw wallpaper, embedded as an iframe in index.html
```

`bubbles.html` is a direct copy of `index.html` from the `main` branch. The landing page calls `livelyPropertyListener()` on it directly through the iframe, so the control panel works without any backend.

---

## Deployment

Hosted on Cloudflare Pages, pointed at this branch. No build step — fully static.

| Setting          | Value                  |
| ---------------- | ---------------------- |
| Branch           | `webUI`              |
| Build command    | *(none)*             |
| Output directory | `/`                  |
| Custom domain    | `bubbles.toomcis.eu` |

---

## Keeping `bubbles.html` up to date

Whenever the wallpaper shader is updated on `main`, copy `index.html` from `main` into this branch as `bubbles.html`.

```bash
git checkout main -- index.html
git mv index.html bubbles.html
git commit -m "sync bubbles.html from main"
```

---

## Looking for the wallpaper itself?

Head to the **[main branch](https://github.com/toomcis/Bubbles)** to download and install the wallpaper for Lively Wallpaper.

---

**Author:** [Toomcis](https://toomcis.eu) — [github.com/toomcis](https://github.com/toomcis)
