# Your academic website — setup

This is a plain static site (no Jekyll, no build step) — GitHub Pages will serve it exactly as-is. It's five separate pages, all sharing the same nav bar (the current page is highlighted in blue in the nav). Contact info (email, X, LinkedIn, GitHub) lives on the About page rather than a separate Contact page.

## 1. Create the repo

Signed in as **danswlee**, create a **new repository** named exactly:

```
danswlee.github.io
```

(It must match that account's username exactly, with `.github.io` at the end — that's what tells GitHub to serve it as a personal site rather than a project page.)

## 2. Add these files

Upload all of these to the **root** of that repo:

- `index.html` — About / home page (includes contact info)
- `research.html`
- `publications.html`
- `code.html`
- `cv.html`
- `style.css`
- `script.js`

Add your CV as `cv.pdf` in the same folder — the "Download full CV" button on `cv.html` (and the quick link in the header of `index.html`) already point to that filename.


