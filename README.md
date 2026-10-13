# DIPRR home-screen launcher (free)

A tiny installable app that gives DIPRR a real icon on phones and computers, and keeps an
**encrypted offline pack** on the device so your projects, links, notes and logins open **without internet**.

It never sees your data unless you load an offline pack, and that pack stays encrypted (AES-256) on the device.
It never runs code from a pack file; it only reads the encrypted data and decrypts it with your passphrase.

## Set up (10 minutes, free)
1. Open `config.js` and paste your DIPRR Web app URL between the quotes.
2. Host this `launcher` folder for free, using **one** of these:
   - **Netlify Drop** (no account needed to try): go to https://app.netlify.com/drop and drag the `launcher` folder onto the page. Claim the site (free account) so it stays online.
   - **GitHub Pages**: create a public repository, upload these files, then Settings → Pages → Deploy from branch → `main` / root.
   - **Cloudflare Pages**: Workers & Pages → Create → Pages → Upload assets.
3. Open the site address on your phone and add it to the home screen:
   - iPhone/iPad (Safari): Share → **Add to Home Screen**
   - Android (Chrome): ⋮ → **Install app**

## Using it offline
1. In DIPRR (online), unlock the vaults you want included, then **Security → Make offline pack**.
2. Open the launcher → **Load offline pack…** → pick the downloaded file. Then delete the downloaded file.
3. Without internet: open the launcher → **Open offline pack** → enter the pack passphrase.
   It locks again after 3 minutes, or as soon as you switch away.

Make a fresh pack whenever you've changed a lot; loading a new one replaces the old one.

## Why this is separate from DIPRR itself
Google Apps Script pages can't set their own home-screen icon or work offline, so this small static site handles
both. Face ID / fingerprint unlock and filling passwords into other apps need the native iOS/Android apps
(see NATIVE-APPS.md).
