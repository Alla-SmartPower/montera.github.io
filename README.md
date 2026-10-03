# Montera Landing Page

Public-facing static landing page for **Montera** — a research-driven platform for automated and adaptive penetration testing.

This directory is **independent** from the main Montera application (`pt-frontend` / `pt-backend`). It contains only static files intended for GitHub Pages.

## Expected URL

https://alla-smartpower.github.io/montera_landing/

## Repository setup

Create or use a dedicated repository named:

`montera_landing`

Upload the **contents** of this directory to the repository root (so that `index.html` is at the root).

## GitHub Pages settings

1. Open the repository on GitHub  
2. Go to **Settings → Pages**  
3. Under **Build and deployment**:
   - **Source:** Deploy from a branch  
   - **Branch:** `main`  
   - **Folder:** `/(root)`  
4. Click **Save**

After deployment, the site should be available at:

https://alla-smartpower.github.io/montera_landing/

## Local preview

Open `index.html` directly in a browser, or serve the folder with any static file server:

```bash
# optional
python3 -m http.server 8080 --directory .
```

No backend, API, database, authentication, npm build, or Docker is required.

## Design assets reused from Montera

Copied from the main Montera frontend (public brand assets only):

| Asset | Source |
|-------|--------|
| `assets/montera_logo.png` | `pt-frontend/src/assets/montera_logo.png` |
| `assets/montera-bg.jpg` | `pt-frontend/src/assets/montera-bg.jpg` |
| `assets/montera_favicon.svg` | `pt-frontend/public/montera_favicon.svg` |

Visual tokens (colors, glass cards, gradients, Mulish typography, button styles) follow `pt-frontend/src/theme.ts` and the Login / MainLayout visual language.

## Updating content

- Edit copy and structure in `index.html`
- Adjust styling in `style.css`
- Mobile navigation behavior is in `script.js`
- Keep all asset paths **relative** (`./assets/...`, `./style.css`)

## Deploying changes

1. Commit updates to the `main` branch of `montera_landing`  
2. Push to GitHub  
3. Wait for Pages to rebuild  

Ensure `.nojekyll` remains in the repository root so GitHub Pages serves files without Jekyll processing.
