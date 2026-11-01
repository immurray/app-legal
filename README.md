# app-legal

Brand-neutral hosting for the legal and support pages of every app, served by GitHub Pages from `main` (root):

**Base URL:** https://immurray.github.io/app-legal/

## Convention (one folder per app)

```
index.html                  # list of all apps — add a section per app
<app-slug>/privacy-policy.html
<app-slug>/terms-of-service.html
<app-slug>/support.html
```

- `<app-slug>` = lowercase app name with no spaces (e.g. `subbill` for SubBill).
- App Store Connect fields:
  - Privacy Policy URL → `https://immurray.github.io/app-legal/<app-slug>/privacy-policy.html`
  - Support URL → `https://immurray.github.io/app-legal/<app-slug>/support.html`
  - Terms (EULA link in the app description / paywall) → `https://immurray.github.io/app-legal/<app-slug>/terms-of-service.html`
- Contact on every page: gridzen@mail.grokbot.com and this repo's Issues (https://github.com/immurray/app-legal/issues). Do not invent other addresses.
- Each page links to its two siblings. Update the "Last updated" date whenever a policy changes.
- Plain static HTML only; `.nojekyll` disables Jekyll processing.

## Adding a new app

1. Copy `subbill/` to `<app-slug>/` and edit the app name, features, data practices, and subscription terms.
2. Add the app to `index.html`.
3. Commit and push to `main`, wait for the Pages build, and check that all three URLs return 200.
4. Put the URLs in App Store Connect.

## Apps

| App | Support | Privacy | Terms |
|---|---|---|---|
| SubBill | [support](https://immurray.github.io/app-legal/subbill/support.html) | [privacy](https://immurray.github.io/app-legal/subbill/privacy-policy.html) | [terms](https://immurray.github.io/app-legal/subbill/terms-of-service.html) |
