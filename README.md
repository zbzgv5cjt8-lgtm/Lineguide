# LineGuide MVP — beginner setup

## What this prototype includes
- Guided procedure builder with four stages
- Searchable procedure library
- Site → line → asset → task browsing
- Step-by-step instructions, expected results, verification, photos and warnings
- Standard procedure preview with Print / Save PDF
- Draft / In review / Approved document status
- Revision number increment when editing, with prior revisions retained in document history
- Named author, reviewer and approver fields with approval-date record
- JSON backup export and import controls in the library
- Local browser storage and offline app-shell caching after HTTPS hosting
- Export procedure library backup as JSON

## Important limitations
This is a prototype, not a production safety system. Procedures are stored only in the browser/device where entered. There is no account, multi-user syncing, server database, identity verification, or server-enforced approval workflow. Named approvals are recorded in the local app but are not authenticated signatures. Revision snapshots are retained in the local record; export regular backups. A QR code on one device cannot make locally stored data appear on another device. The sample Packing Line 04 procedure is explicitly a draft and must not be used to perform real work.

## Easiest iPhone testing route
The app needs HTTPS hosting for Home Screen installation and service-worker offline caching. One simple route is GitHub Pages:

1. On your iPhone, open Safari and sign in to GitHub at https://github.com. Create a repository named `lineguide`.
2. Upload `index.html`, `app.js`, `manifest.json`, and `sw.js` from this folder into the repository root. Upload `README.md` if useful.
3. Open repository **Settings → Pages**. Under Build and deployment choose **Deploy from a branch**, select `main` and `/(root)`, then Save.
4. Wait for GitHub Pages to publish. The URL will look like `https://YOUR-USERNAME.github.io/lineguide/`.
5. Open that URL in Safari. Tap Share (square with arrow) → **Add to Home Screen** → Add.
6. Open LineGuide from the new Home Screen icon. Create a test procedure, add a photo, save it, and search for it in the Library.
7. After it has loaded once, try Airplane Mode to test whether the app shell opens offline. QR creation itself needs internet.
8. Open a procedure preview and tap **Print / Save PDF**. In the iOS print screen, use the Share button to save or send the PDF.

If uploading files on mobile is awkward, use a computer for the initial upload. Do not publish real sensitive site information in a public repository. For private operational use, the app needs private hosting, access controls and shared storage.
