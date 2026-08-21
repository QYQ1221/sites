# Static Sites — Velorah & Apogee

Two self-contained static websites, deployed together via **GitHub Pages**. No build step required.

## Structure

```
.
├── index.html          # Hub page linking to both sites
├── velorah/index.html   # Velorah® cinematic landing page
├── apogee/index.html    # Apogee data-driven landing page (4 nav sections + contact)
└── .nojekyll            # Disable Jekyll so paths/underscores are preserved
```

Each site is a single self-contained HTML file (Tailwind via CDN, fonts + video via CDN). Open any `index.html` directly in a browser to preview.

## Deploy to GitHub Pages

1. Create a repo on GitHub (e.g. `your-username/sites`).
2. Push this folder:

   ```bash
   git init
   git add -A
   git commit -m "Add Velorah & Apogee static sites"
   git branch -M main
   git remote add origin https://github.com/your-username/sites.git
   git push -u origin main
   ```

3. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → `main` / root** → Save.
4. Wait ~1 minute, then visit:
   - `https://your-username.github.io/sites/`  (hub)
   - `https://your-username.github.io/sites/velorah/`
   - `https://your-username.github.io/sites/apogee/`

## Notes

- Both pages rely on external CDNs (Tailwind Play CDN, Suisse Intl webfont, CloudFront video). They need network access to render fully; the dark background is the fallback if a CDN is blocked.
- To use a custom domain, add a `CNAME` file with your domain and configure it under Settings → Pages.
