# TSPF — The Supa Paper Frogs

Handmade origami paper frogs that actually jump. Folded by hand, one sheet at a time — no glue, no scissors.

**Live site:** https://jivanshdaru.github.io/the-supa-paper-frogs/

## About this repo

The whole site is a single self-contained page: `index.html`. All CSS and JavaScript are inline, so there is no build step, no bundler, and no dependencies to install. Google Fonts is the only external resource.

| File | Purpose |
| --- | --- |
| `index.html` | The entire site — markup, styles, scripts |
| `404.html` | Custom "page not found" page served by GitHub Pages |
| `favicon.svg` | Browser tab icon |
| `og-image.png` | Preview image shown when the link is shared |
| `.nojekyll` | Tells GitHub Pages to publish files as-is, skipping Jekyll |

## Running it locally

Open `index.html` in a browser — that is enough for most changes.

To test it the way GitHub Pages serves it (useful for checking the 404 page and absolute paths), run a local web server from the project folder:

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000/.

## Publishing changes

Every push to the `main` branch republishes the site automatically. GitHub usually takes under a minute.

```bash
git add .
git commit -m "Describe what changed"
git push
```

## Hosting settings

GitHub Pages is configured to deploy from the `main` branch, root folder (`/`), under repository **Settings → Pages**.

## Leaderboard (optional)

The frog game keeps high scores in the browser's local storage by default, so scores stay on the device that set them. To share a leaderboard across devices, set `LEADERBOARD_API_URL` near the top of the script section in `index.html` to a backend endpoint (for example a Google Apps Script web app URL). Leave it as an empty string to keep scores local.
