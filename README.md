# kasegi-privacy

Privacy policy page for [Kasegi](https://github.com/nozokada/kasegi) (Flexible
Pay and Shift Calculator), published via GitHub Pages for App Store / Google
Play listing requirements.

Published at: https://nozokada.github.io/kasegi-privacy/

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

1. Create an empty GitHub repository named `kasegi-privacy` under the
   `nozokada` account (no README/license/gitignore, to avoid conflicts with
   this local repo).
2. Push this repo to it.
3. In the repo's **Settings → Pages**, set **Source** to `Deploy from a
   branch`, branch `main`, folder `/ (root)`.
4. Wait a minute, then confirm the page loads at
   https://nozokada.github.io/kasegi-privacy/.
5. Paste that URL into App Store Connect (App Privacy → Privacy Policy URL)
   and the Google Play Console (App content → Privacy policy).
