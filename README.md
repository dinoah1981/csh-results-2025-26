# Comp Sci High — 2025–26 Results

A single-file, static results dashboard (Regents, course grades by department, student experience).
Everything lives in `index.html` — no build step, no dependencies to install. It only loads Chart.js
from a CDN at runtime, so the published page needs internet access (which any visitor's browser has).

> Note: this will be a **public** GitHub Pages site. The data is school-level and de-identified
> (no student names), but anyone with the link can view it.

## Publish to GitHub Pages (about 1 minute)

1. **Create an empty repo** on GitHub (github.com → New repository). Suggested name: `csh-results-2025-26`.
   Don't add a README/.gitignore — keep it empty so the push is clean.

2. **Push these files.** In a terminal, from this folder:

   ```bash
   git init
   git add .
   git commit -m "CSH 2025-26 results dashboard"
   git branch -M main
   git remote add origin https://github.com/<YOUR-USERNAME>/csh-results-2025-26.git
   git push -u origin main
   ```

   Replace `<YOUR-USERNAME>` with your GitHub username (or org). You'll authenticate in your
   browser or with a personal access token the first time.

3. **Turn on Pages.** In the repo: **Settings → Pages → Build and deployment → Source: "Deploy from a branch"**,
   then **Branch: `main` / `/ (root)` → Save**.

4. Wait ~30–60 seconds. Your site will be live at:

   ```
   https://<YOUR-USERNAME>.github.io/csh-results-2025-26/
   ```

## Updating it later

Edit `index.html` (or have it regenerated), then:

```bash
git add index.html
git commit -m "Update results"
git push
```

Pages redeploys automatically within a minute.

## Files

- `index.html` — the dashboard (the whole site).
- `.nojekyll` — tells GitHub Pages to serve the files as-is (skips Jekyll processing).
- `README.md` — this file.

## Keeping it private instead

If you'd rather it not be on the open web: make the repo **private** and use GitHub Pages on a private
repo (requires GitHub Pro / Team / Enterprise), or just share `index.html` directly / host it on an
internal drive. Open the file locally by double-clicking it — it works with no server.
