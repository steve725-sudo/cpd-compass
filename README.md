# CPD Compass — Your CPD, on course.

Free CPD tracker for Australian nurses and midwives, built around the NMBA CPD and recency-of-practice standards. No server and no accounts: each nurse's data stays on her own device.

## Set up on GitHub Pages (no coding needed)
1. Go to github.com and sign in. Click **+ → New repository**, name it `cpd-compass`, set it to **Public**, then click **Create**.
2. On the new repo page click **uploading an existing file**. Drag in **all** the files from this zip (not the folder itself), then click **Commit changes**.
3. Go to **Settings → Pages**. Under *Source* choose **Deploy from a branch**, select **main** and **/ (root)**, then click **Save**.
4. Wait 1–2 minutes. The app is then live at `https://<username>.github.io/cpd-compass/`.

## Install on a phone
- **iPhone/iPad:** open the link in **Safari** → Share → **Add to Home Screen**. Open the app from the home screen *before* entering anything, because Safari and the home-screen app keep separate storage.
- **Android:** open the link in Chrome → ⋮ → **Install app**.

## Updating
Upload the changed files over the old ones in the repo, and bump `VERSION` in `sw.js` each time. Installed apps show an "Updated — reload" banner.

## Branding
- Colours: Compass Teal `#0E8077`, Harbour Navy `#12355B`, Coral `#F2785C`, Sand `#F6F4EF`
- Mark: `brand-mark.svg`. Icons and `share-card.png` (the link-preview image) are made from it.
- Tagline, credit line and feedback email: edit the `BRAND` block near the top of the script in `index.html`.

## "Say thanks" (Samantha Grosser's books)
- Shown in Settings, and once on Home when a nurse meets her yearly hours. It can be dismissed and never pops up again that year.
- Book details are in `BRAND.support` in `index.html`. Set `enabled: false` to remove the feature.
- **Covers:** create a `books` folder in the repo and upload the covers with exactly these names (JPG, about 400 px wide): `all-that-remains.jpg`, `where-the-light-still-shone.jpg`, `the-last-goodbye.jpg`, `an-officers-affair.jpg`. Until then, styled title cards show instead.

## Maintenance schedule
- **Each June** (new CPD year) and **whenever the NMBA announces the outcome of its 2026 CPD / recency review**: check the NMBA CPD and recency pages. Update `RULES_HTML`, `reqs()` and `RECENCY_REQ` if needed, then set `RULES_CHECKED`.
- **Every 6 months**: tap through every link in Free learning and update `SITES` and `SITES_CHECKED`.
- **When AI providers retire models**: update the defaults in `AI_DEF`. Users can also change them in Settings.
- After any change, bump `VERSION` in `sw.js`.

## Files
`index.html` is the app. `sw.js` provides offline support. `manifest.webmanifest`, the icons and `share-card.png` are branding. `PRIVACY.md` is the privacy statement, `TESTING.md` is the pilot checklist, and `LICENSE` is the free, noncommercial licence.

## Licence
PolyForm Noncommercial 1.0.0: anyone can use and share it free; nobody can sell it. See `LICENSE`.
