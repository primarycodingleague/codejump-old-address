# CodeJump — old address

CodeJump moved from **codejump.primarycodingleague.co.uk** to **https://codejump.co.uk** in October 2026.

This tiny GitHub Pages site keeps the old address working: every page on it (`index.html`, and `404.html` for any other
path) sends visitors to the same page and link on codejump.co.uk, so old bookmarks and share links still work.

On a device's first visit it also carries that browser's CodeJump storage across (saved games, the unsaved draft,
settings and sign-in), because browsers keep each web address's storage separate. It uploads it to the CodeJump cloud
(`POST /move` on codejump-cloud, worker v15) for a one-time code that expires after a day and is deleted once read, and
codejump.co.uk picks it up from `?cjmove=<code>`. After that the device just redirects.

Settings → Pages: deploy from the `main` branch, custom domain `codejump.primarycodingleague.co.uk`, Enforce HTTPS.
