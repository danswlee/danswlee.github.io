# Your academic website — setup

This is a plain static site (no Jekyll, no build step) — GitHub Pages will serve it exactly as-is. It's five separate pages, all sharing the same nav bar (the current page is highlighted in blue in the nav). Contact info (email, X, LinkedIn, GitHub) lives on the About page rather than a separate Contact page.

**This version is set up for a second, dedicated personal GitHub account — `danswlee`** — used only to host this site, separate from your main `dswlee0519` account. Nothing needed to change in the HTML/CSS for this: the site never hardcodes its own domain anywhere. The only links that still point at `dswlee0519` are the "GitHub" link on the About page and the repo links on the Code and Data page — those are correct as-is, since that's genuinely where your code lives (MASSPRF, Condensate_Size_Distribution_Simulations); don't repoint those at `danswlee`.

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

## Color scheme

The accent color is navy (`#2c4a68`) with a pastel-blue soft tone (`#dbe7f2`) for pills/badges — both set once as CSS custom properties (`--accent`, `--accent-soft`) at the top of `style.css`, so the whole site follows from those two values. This replaced an earlier forest-green scheme.

The *Nature Physics* cover thumbnail on the publications page (`.pub-cover`) is sized larger (150&times;200px desktop, 96&times;128px mobile) so it reads as a real cover image rather than a small icon.

## Publication DOIs

Every publication title is now a link to its DOI. While tracking these down I found three discrepancies worth knowing about (and worth checking against your master CV, not just this site):

- The 2025 Nature Communications paper's actual published title is "Cell surface crowding is a tunable **energetic** barrier to cell-cell fusion" — the site now uses this; your CV may still say "biophysical barrier" (the bioRxiv preprint title).
- The Zhang et al. Physical Review Letters paper is **volume 126**, not 124 (same page 258102).
- The Shin et al. Cell paper was published in **2018**, not 2019 (Cell vol. 175 issue 6, Nov. 2018).

## Still-open items

- **Research section (`#research`) text** — the About page and the "Cell-surface crowding" card are now your own wording. The second card ("Phase separation & the physics of the cell nucleus," Ph.D. work) is still my drafted language from your publication titles — worth a look if you want that in your own voice too.
- **`cv.pdf`** — not included; drop your actual CV PDF into the repo root for the download buttons to work.
- **Lab links** in the About section (Fletcher, Brangwynne, Wingreen lab pages) — worth double-checking they're current before pushing live.
- **Images** — four slots are wired up and waiting for files in an `images/` folder at the repo root:
  - `images/headshot.jpg` — your photo, shown circular in the About page header (roughly square works best, e.g. 400&times;400px).
  - `images/research-crowding.png` — a schematic or microscopy figure for the cell-surface crowding card (~16:10 aspect ratio). PNG rather than JPG here since JPEG compression artifacts show up badly on schematics/diagrams with sharp lines and flat color.
  - `images/research-phase-separation.jpg` — same, for the phase-separation card.
  - `images/natphys-2021-cover.jpg` — the actual *Nature Physics* April 2021 cover image, shown as a thumbnail next to that publication (portrait, e.g. ~300&times;400px).

  Until each file exists, its slot shows a dashed placeholder with the expected path so nothing looks broken in the meantime — just add files with those exact names and they'll appear automatically.

Everything else (bio, publications list with years and DOIs, awards, education, the two GitHub repos in the Code section) is pulled directly from your CV and your GitHub profile.
