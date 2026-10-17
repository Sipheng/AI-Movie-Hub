# TV Hub — Drama Streaming Launcher (GitHub Pages)

A single self-contained `index.html`: a header bar plus **two sections** of
launcher tiles — **chartdrama** (43 sites) and, on a separate line below,
**dramafren** (20 sites). Each tile has its own soft, distinct color (kept at a
constant lightness/saturation so it's easy to read and never over-contrasted),
with the `↗` arrow. Selecting a tile opens that website. The grid re-flows its
rows and columns for phones, tablets and large TV screens, and tiles are
keyboard / TV-remote focusable (arrow keys + Enter).

## Edit the website lists
Open `index.html` and change the `GROUP_CHARTDRAMA` / `GROUP_DRAMAFREN` arrays
near the bottom — add, remove or reorder `{ name: "...", url: "https://..." }`
entries. That's the only thing you need to touch.

## Publish on GitHub Pages

### Option A — web UI (no git needed)
1. Create a new repository on GitHub, e.g. `tvhub`.
2. **Add file ▸ Upload files**, drag in `index.html` (and this README), commit.
3. **Settings ▸ Pages**.
4. Under **Source** choose **Deploy from a branch**, pick `main` / `/ (root)`, **Save**.
5. Wait ~1 minute. Live at: `https://<your-username>.github.io/tvhub/`

### Option B — command line
```bash
cd tvhub-site
git init
git add .
git commit -m "TV Hub drama streaming launcher"
git branch -M main
git remote add origin https://github.com/<your-username>/tvhub.git
git push -u origin main
```
Then enable Pages as in steps 3–5 above.

## Open it on the Smart TV
In the TV browser, go to your Pages URL. Navigate tiles with the remote and
press Enter to launch a site. Tiles open in a new tab.
