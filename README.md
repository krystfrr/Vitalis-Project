# Vitalis Demo

Vitalis is a static, front-end-only demo of a personal health archive. The root `index.html` is the dashboard; the three section folders contain the exported Health Records, Medications, and Medical ID screens.

The content is sample data. There is no backend, authentication, network data submission, or persistent storage. The medication log is an in-browser demo interaction and resets when the page is reloaded.

## Preview

From the repository root, run:

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000>. Serving over HTTP also lets the exported screens load their local runtime scripts in browsers that restrict scripts opened with `file://`.

## Publish With GitHub Pages

1. Push this repository to GitHub.
2. Open the repository's **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the branch containing the site and the `/(root)` folder, then save.

No build step or package installation is required. The site entry point and all assets are in the repository root and its subfolders. Keep links relative so the same files work under a GitHub Pages project URL.

## Screens

- `Health Records-html/Records.dc.html`
- `Medications-html/Medications.dc.html`
- `Medical ID-html/MedicalID.dc.html`

These `.dc.html` exports are design-reference screens rendered by the bundled `support.js` and `vendor/` runtime files. Preserve the reference styling when changing them; avoid editing the generated runtime files.