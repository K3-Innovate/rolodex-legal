# K3 Innovate legal site

Public privacy policies and terms for K3 Innovate LLC's apps, served by
GitHub Pages at **https://k3-innovate.github.io/rolodex-legal/**. App source
stays in private repos; this repo is public only because Pages on GitHub's
free plan needs a public repo.

## Rules

- **A published URL never moves.** Store listings and shipped builds point
  at these pages. Rolodex Pro's three URLs are in its App Store and Play
  listings, so they stay at the site root:
  - `/rolodex-legal/` (support URL; this site's index)
  - `/rolodex-legal/privacy-policy.html`
  - `/rolodex-legal/eula.html`
- **Don't rename this repo.** Pages URLs follow the repo name, and the old
  ones would break.
- **The owner and counsel approve every policy before it's merged.**
  Merging to `main` publishes it.

## Adding an app

1. Make a folder named for the app: `<app-slug>/privacy-policy.html` and
   `<app-slug>/terms.html` (or `eula.html`), using `style.css` with
   `href="../style.css"` and a crumb back to `../index.html`.
2. Add the app's section to `index.html`.
3. Put the new URLs in the app's store listings and its build settings.

What each policy has to cover, and the store forms that must match it, are
in the K3 plugin's `store-release` skill (`legal-pages.md`) in
`K3-Innovate/k3-plugin`.

## Where each app's pages are

| App | Pages | Source text |
|---|---|---|
| Rolodex Pro | this site's root | `rolodex_pro/legal/*.md`, mirrored here by hand (no sync; change both the same day) |
| Word of the Day | `https://wordoftheday-api.k3innovate.com/privacy/` and `/terms/`, once counsel approves the text | `Wordofthedayforkids/backend/wordoftheday_backend/legal_pages/` |
