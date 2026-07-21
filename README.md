# kasegi-website

Website for [Kasegi](https://github.com/nozokada/kasegi) (Flexible Pay and
Shift Calculator), published via GitHub Pages. Currently just a placeholder
homepage plus the privacy policy page needed for App Store / Google Play
listing requirements; a full marketing/landing site (à la Gappon's
`japanese-lds-quad-website`) is expected to grow here later.

Published at: https://nozokada.github.io/kasegi-website/
Privacy policy: https://nozokada.github.io/kasegi-website/privacypolicy/

## Structure

Static pages, no build step:

- `index.html` — minimal placeholder homepage, linking to the privacy
  policy. Will be replaced by a real landing page later.
- `privacypolicy/index.html` — bilingual (Japanese / English) privacy
  policy with a client-side language toggle. Defaults to the browser's
  language. Kept at a stable `/privacypolicy/` path so the URL registered
  with the app stores doesn't need to change as the rest of the site grows.
- `.nojekyll` — tells GitHub Pages to serve files as-is instead of running
  them through Jekyll.

## Updating the policy

Edit `privacypolicy/index.html` directly (both the `#content-ja` and
`#content-en` sections) and update the "last updated" date in each. Commit
and push to `main` — GitHub Pages redeploys automatically within a minute or
two.

## Hosting setup (one-time)

1. Create an empty GitHub repository named `kasegi-website` under the
   `nozokada` account (no README/license/gitignore, to avoid conflicts with
   this local repo).
2. Push this repo to it.
3. In the repo's **Settings → Pages**, set **Source** to `Deploy from a
   branch`, branch `main`, folder `/ (root)`.
4. Wait a minute, then confirm the pages load at
   https://nozokada.github.io/kasegi-website/ and
   https://nozokada.github.io/kasegi-website/privacypolicy/.
5. Paste the privacy policy URL into App Store Connect (App Privacy →
   Privacy Policy URL) and the Google Play Console (App content → Privacy
   policy).

## Growing this into a full site later

Replace the placeholder `index.html` with a real landing page and link to
`privacypolicy/` from it (as it already does). The privacy policy's path
doesn't need to move, so the URL already registered with the app stores
keeps working.
