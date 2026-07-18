# Apex Training

A single-page workout, bodyweight, and calorie tracker.

## Contents

- `index.html` — the full app (self-contained styling and scripts; the
  brand wordmark shown inside the app is inline SVG)
- `manifest.json` — web app manifest so it can be installed as a PWA
- `icons/` — app icons used for the browser tab favicon, Apple/iOS home
  screen icon, Windows pinned-tile icon, and PWA install icon
  (`icon-192.png`, `icon-512.png`, `icon-512-maskable.png`)

## Installing as an app

Because of the manifest and icons, most browsers (Chrome, Edge) will offer
an "Install" option in the address bar. Installing gives it its own window
and Start Menu / taskbar icon on Windows, and a home-screen icon on
Android/iOS — no separate build step needed.

## Data persistence

This app saves your workouts, bodyweight, and calorie logs using the
browser's `localStorage`, under keys prefixed `apex-training:`. Data lives
on whichever device/browser you use the app in and survives refreshes and
closing the tab. It's cleared if you clear that site's browsing data, and
it does **not** sync across devices — it's per-browser only.

## Running locally

Just open `index.html` in a browser, or serve the folder with any static
file server, e.g.:

```
npx serve .
```

## Deploying with GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under "Build and deployment", set **Source** to `Deploy from a branch`,
   pick the `main` branch and `/ (root)` folder.
4. Save — your site will be live at
   `https://<your-username>.github.io/<repo-name>/`.
