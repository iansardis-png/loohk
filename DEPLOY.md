# Deploy LooHK to GitHub Pages

The site is static. Root must contain `index.html` (this folder already does).

## Fastest: GitHub website

1. Go to https://github.com/new
2. Name the repo `loohk` (or any name). Public.
3. Do **not** add a README.
4. Upload these files into the repo root (not a subfolder):
   - `index.html`
   - `app.js`
   - `styles.css`
   - `manifest.json`
   - `icon.svg`
   - `.nojekyll`
   - `data/toilets-v1.geojson` (keep the `data/` folder)
5. Repo → **Settings** → **Pages**
6. Source: **Deploy from a branch**
7. Branch: `main` / folder: `/ (root)` → Save
8. After a minute the map is at:

`https://YOUR_USERNAME.github.io/loohk/`

## Command line

```bash
cd hk-toilet-app
git init
git add .
git commit -m "LooHK map v1"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/loohk.git
git push -u origin main
```

Then enable Pages as above.

If the map is blank, you put the files in a subfolder. They must be at the repo root.
