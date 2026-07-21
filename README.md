# kasegi-website

Website for [Kasegi](https://github.com/nozokada/kasegi) (Flexible Pay and
Shift Calculator), published via GitHub Pages. Currently contains just the
privacy policy page needed for App Store / Google Play listing requirements;
a full marketing/landing site (à la Gappon's `japanese-lds-quad-website`) is
expected to grow here later.

Published at: https://nozokada.github.io/kasegi-website/

## Structure

A single static page, no build step:

- `index.html` — bilingual (Japanese / English) privacy policy with a
  client-side language toggle. Defaults to the browser's language.
- `.nojekyll` — tells GitHub Pages to serve the file as-is instead of running
  it through Jekyll.

## Updating the policy

Edit `index.html` directly (both the `#content-ja` and `#content-en`
sections) and update the "last updated" date in each. Commit and push to
`main` — GitHub Pages redeploys automatically within a minute or two.

## Hosting setup (one-time)

1. Create an empty GitHub repository named `kasegi-website` under the
   `nozokada` account (no README/license/gitignore, to avoid conflicts with
   this local repo).
2. Push this repo to it.
3. In the repo's **Settings → Pages**, set **Source** to `Deploy from a
   branch`, branch `main`, folder `/ (root)`.
4. Wait a minute, then confirm the page loads at
   https://nozokada.github.io/kasegi-website/.
5. Paste that URL followed by `privacy` if/when the policy moves to its own
   path (see below), or the root URL as-is, into App Store Connect (App
   Privacy → Privacy Policy URL) and the Google Play Console (App content →
   Privacy policy).

## Growing this into a full site later

Right now `index.html` at the root *is* the privacy policy, since that's the
only page needed today. When a real landing page is added, move this file to
`privacy/index.html` (or similar) and give it its own link from the new
homepage, then update the URL registered with the app stores accordingly.
