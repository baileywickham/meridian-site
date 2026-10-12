# meridian-site

Public pages for Meridian, served by GitHub Pages: the home page, privacy policy and terms that
Google's OAuth consent screen links to.

- `index.html`: home page
- `privacy.html`: privacy policy
- `terms.html`: terms of service

Keep the privacy policy in step with the app: if Meridian starts sending data somewhere new, update
`privacy.html` and its date.
- `appcast.xml`: the Sparkle update feed the Mac app polls
  (`https://baileywickham.com/meridian-site/appcast.xml`)

Mac releases are published by `scripts/release.sh` in the (private) meridian repo: it uploads the
notarized `.dmg` as a GitHub Release asset of this repo, adds the item to `appcast.xml` and points
the Download button in `index.html` (`data-release-link`) at it. Don't edit those by hand; keep the
`data-release-link` / `data-release-requires` attributes, the script looks for them.
