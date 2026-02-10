# Air Shipment Swagger Docs (GitHub Pages)

This folder contains a static Swagger UI site that renders `openapi.yaml`.

## Files

- `index.html`: Swagger UI page (includes dark/light toggle + schema auto-expand).
- `openapi.yaml`: OpenAPI 3.0 specification.
- `.nojekyll`: Prevents GitHub Pages from applying Jekyll processing.

## Host on GitHub Pages

1. Create a GitHub repository (example: `air-shipment-docs`).
2. Upload these files to the repository root (or commit/push from your machine).
3. In GitHub go to:
   - **Settings → Pages**
   - **Build and deployment**
   - **Source**: `Deploy from a branch`
   - **Branch**: `main` (or `master`) and **Folder**: `/ (root)`
4. Save. GitHub will show your Pages URL after it builds.

## Local preview

Swagger UI fetches `openapi.yaml` via HTTP, so opening `index.html` directly may not work in some browsers.

If you want a quick local server:

### Option A (Python)

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

### Option B (Node)

```bash
npx serve .
```

## Notes

- If you put the site in a subfolder (not repo root), update `url: "openapi.yaml"` in `index.html` accordingly.

