# Workspace Instructions

## Project Shape

This workspace contains three standalone Vitalis design-reference exports:

- `Health Records-html/Records.dc.html`
- `Medical ID-html/MedicalID.dc.html`
- `Medications-html/Medications.dc.html`

Each folder also contains a README, a `support.js` rendering runtime, and local React runtime files in `vendor/`.

## Working With the Mockups

- Treat the `.dc.html` files as visual reference mockups, not production application code. Their inline styles and `<helmet><style>` blocks encode the design values to reproduce in a separate implementation.
- Preserve the mockups' existing layout, colors, typography, spacing, and component details unless the user explicitly asks to change the reference itself.
- Keep changes scoped to the relevant section folder and mockup.
- Do not hand-edit `support.js` or `vendor/react*.js`; these are bundled runtime files, not the design source.
- The HTML uses an `<x-dc>` template and may contain design-tool interpolation tokens such as `{{accent}}`. Do not assume these are ordinary app templates or replace them without a specific request.

## Preview

Serve the relevant folder over HTTP, then open its `.dc.html` file. For example, from `Health Records-html/` run:

```sh
python3 -m http.server 8000
```

Open `http://localhost:8000/Records.dc.html`. Serving over HTTP avoids browser restrictions that can affect scripts opened through `file://`.