# YOU MUST RUN

A first-person nightmare runner. One static page, no build step.

## Run it locally
Browsers block `fetch` from `file://`, so serve the folder:

    python3 -m http.server 8000

then open http://localhost:8000

## Deploy to GitHub Pages
1. Push this folder to a repo (`index.html`, `music/`, `.nojekyll` at the repo root).
2. Settings > Pages > Deploy from a branch > `main` / root.
3. Open `https://<you>.github.io/<repo>/`.

## Music
Add audio files to `music/` and list them in `music/tracks.json`
(see `music/README.txt`). With no tracks the built-in synth plays.
Audio streams from the folder, so keep files a sensible size.

## Notes
- three.js loads from cdnjs. To work offline, download `three.min.js` (r128)
  next to `index.html` and change the `<script src>` near the bottom.
- Settings and records are stored in `localStorage`.
