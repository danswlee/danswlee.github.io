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

Delete `contact.html` from the repo if it's already there from an earlier upload — it's no longer linked from anywhere and the nav no longer points to it.

(Drag-and-drop works fine on github.com, or `git add` + `git push` if you're working locally.)

Add your CV as `cv.pdf` in the same folder — the "Download full CV" button on `cv.html` (and the quick link in the header of `index.html`) already point to that filename.

## 3. Turn on Pages (usually automatic)

Go to the repo's **Settings → Pages**. For a `<username>.github.io` repo, GitHub typically enables Pages automatically from the `main` branch. If it isn't already on, set the source to the `main` branch, root folder.

## 4. Visit your site

It'll be live at:

```
https://danswlee.github.io
```

(Can take a minute or two after the first push.)

## To preview locally before pushing

From this folder, run:

```
python3 -m http.server 8000
```

and open `http://localhost:8000` in a browser — this lets you click between pages the same way visitors will. Double-clicking `index.html` also works for a quick look, but a couple of things (like the CV download link) behave more reliably over a local server.


  Until each file exists, its slot shows a dashed placeholder with the expected path so nothing looks broken in the meantime — just add files with those exact names and they'll appear automatically.

Everything else (bio, publications list with years and DOIs, awards, education, the two GitHub repos in the Code section) is pulled directly from your CV and your GitHub profile.
