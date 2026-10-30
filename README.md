# Camiguin trip app 🌋

Trip app for the Laagan Squad, Camiguin, Nov 5–8, 2026: itinerary, flights, stay, costs, payment status, and the shared photo album.

## How it works

Every push to `main` runs two GitHub Actions:

- **Deploy web app to GitHub Pages** publishes `www/` as a web app at `https://<your-username>.github.io/<repo-name>/`. iPhone and Android users can install it from the browser.
- **Build Android APK** builds `camiguin.apk` and attaches it to a new release on the repo's **Releases** page.

## One-time setup

1. **Settings › Pages › Build and deployment › Source:** choose **GitHub Actions**.
2. **Actions** tab: if asked, click **I understand my workflows, go ahead and enable them**.
3. Run both workflows once from the **Actions** tab (**Run workflow**), or push any change.

## Installing

- **Android (APK):** open the latest release under **Releases**, download `camiguin.apk`, open it, and allow installing from your browser or file app when asked.
- **Android (no APK):** open the GitHub Pages link in Chrome, then menu ⋮ › **Install app**.
- **iPhone:** open the GitHub Pages link in Safari, then **Share › Add to Home Screen**.

## Updating the app

Edit `www/index.html` (or replace it with a new version) and commit to `main`. The web app updates on the next open; Android APK users install the new APK from the latest release.

## Files

- `www/`: the app (HTML, manifest, service worker for offline use, icons)
- `assets/`: source icon and splash for the Android build
- `capacitor.config.json`, `package.json`: Android wrapper settings (Capacitor)
- `.github/workflows/`: the two automated builds
