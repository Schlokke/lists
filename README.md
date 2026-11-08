# Lists as an installable web app (PWA)

Chrome only offers "Install app" for pages served over https, so the files in this folder
need to be hosted once. After the first visit the app works fully offline.

## Host it for free on GitHub Pages

1. Create a free account at github.com and make a new public repository, for example `lists`.
2. Click "Add file" > "Upload files" and drag in everything from this folder:
   `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`.
   Commit the upload.
3. Open the repository's Settings > Pages. Under "Build and deployment", choose
   "Deploy from a branch", pick `main` and `/ (root)`, and save.
4. After a minute your app is live at `https://YOUR-NAME.github.io/lists/`.

## Install it on your phone

1. Open that address in Chrome on Android.
2. Open the three-dot menu and tap "Install app" (or "Add to Home screen").
3. Open it once with internet so it can cache itself. From then on it works offline.

## Turn it into an APK with PWABuilder

1. Go to pwabuilder.com and paste your GitHub Pages address.
2. Tap "Package for stores" > Android and download the package.
3. The zip contains an installable `.apk` plus the signing key. Keep the key if you ever
   want to publish updates.

## Updating

Edit `index.html`, upload it again, and change `var V = 'lists-v1'` in `sw.js` to
`lists-v2` so installed copies pick up the new version.

Your data is stored on each device. Use "Export" in the labels and backup screen to
keep a copy.
