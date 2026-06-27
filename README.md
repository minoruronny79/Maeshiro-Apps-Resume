# Minoru Maeshiro — Resume Website

Projects-centric personal site. Static HTML, no build step. Hosted on GitHub Pages.

## Structure
```
index.html              ← the whole site
videos/                 ← project videos (.mp4)
docs/1_Maeshiro_Resume.pdf
```

## Publish on GitHub Pages
1. Create a repo (e.g. `minorumaeshiro.github.io` for a root site, or any name).
2. Upload everything in this folder (keep the folders intact).
3. Repo → Settings → Pages → Source: `main` branch, `/root`. Save.
4. Your site goes live at the URL GitHub shows (give it ~1 min).

## Add a new video later (no coding)
1. Drop the `.mp4` into the `videos/` folder.
2. Open `index.html`, find the `PROJECTS` array near the bottom.
3. Add one line to that project's `videos: [...]`:
   ```js
   { type:"guide", title:"My new guide", src:"videos/FILENAME.mp4", note:"short caption" }
   ```
   - `type:"overview"` → amber "Overview" badge (use one per tool)
   - `type:"guide"`    → grey "User Guide" badge

## Add a whole new project
Copy a `{ ... }` block in the `PROJECTS` array, change the fields, and set
`tag` to `"risk"`, `"invest"`, or `"ai"` for the color. Leave `videos:[]` empty
and it shows a "coming soon" placeholder until you upload.

## Tips
- Keep video files reasonably small (GitHub has a 100 MB/file limit; aim < 50 MB).
- Filenames: no spaces is safest (use underscores).
