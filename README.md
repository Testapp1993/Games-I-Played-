# My Game Year — iPhone web app

A static, installable Progressive Web App (PWA) for tracking games played by year. It works without a server-side database: records are saved in local browser storage on the device where you use it.

## Features
- Year-by-year game log and monthly started chart
- Status, platform, genre, start/completion dates, hours, rating, optional cover URL and notes
- Search, filters, sorting, edit and delete
- JSON backup export and restore/merge
- Offline app shell through a service worker after first load
- iPhone Home Screen web-app metadata and icon

## Publish using GitHub Pages (free)
1. On GitHub, create a **new public repository** named `my-game-year`.
2. Upload the contents of this folder to the repository root (the files should appear directly in the repository: `index.html`, `manifest.webmanifest`, `sw.js`, `icon.svg`, `apple-touch-icon.png`).
3. Open repository **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/(root)`, then Save.
5. Wait for deployment. Your address will look like `https://YOUR-USERNAME.github.io/my-game-year/`.
6. Open that address in Safari on your iPhone and test adding a game and exporting a backup.
7. In Safari, tap **Share → Add to Home Screen**, enable **Open as Web App** if offered, then tap **Add**.

GitHub Pages sites are publicly reachable. This app's game data is not uploaded to GitHub or to the site; it is stored in browser storage on each device. Do not put personal gaming backup JSON files in the public repository. Export a backup periodically and keep it somewhere private. To move records between devices, export JSON on one device and use Restore on the other.

## Important data notes
- Browser storage is not cloud sync. Clearing Safari website data or removing site storage can delete records; keep backups.
- Each browser/device has its own library. Export/restore is the transfer mechanism.
- Offline support works after the app has successfully loaded online at least once. A new version can require an online visit to update the cached app shell.
- Cover images load from the URL you enter and require internet; external image hosts may block them. Cover images are optional.
- If using a GitHub project URL, keep all app asset links relative (this package does so) so the subfolder path works.
