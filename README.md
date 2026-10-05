# areteapps.hu

Static website for Areté Apps Kft. Plain HTML and CSS, no build step, no cookies, no tracking, fonts self-hosted.

## Files

- `index.html`: home page (English)
- `hu/index.html`: home page (Hungarian)
- `impresszum.html`: legal notice (Hungarian, required for a company website)
- `adatvedelem.html`: privacy notice for this website only
- `styles.css`: all styles
- `fonts/`: Cinzel and Cormorant Garamond (SIL Open Font License)
- `favicon.svg`: browser tab icon
- `CNAME`: custom domain for GitHub Pages
- `.nojekyll`: tells GitHub Pages to serve files as they are

## Before going live

1. Fill in every highlighted `[...]` value in `impresszum.html` once the company is registered (cégjegyzékszám, adószám, közösségi adószám, exact Berger address).
2. Until registration is complete, the company name should carry the "b.a." (bejegyzés alatt) suffix: `Areté Apps Kft. b.a.`
3. Have your ügyvéd check `impresszum.html` and `adatvedelem.html`. Szívem needs its own separate privacy policy before launch.

## Hosting on GitHub Pages

1. Push these files to the root of a repository in the Areté Apps GitHub organization, `areteappshu/areteapps.hu` (public, so GitHub Pages works on the free plan).
2. Repository → Settings → Pages: source "Deploy from a branch", branch `main`, folder `/ (root)`.
3. Custom domain: `areteapps.hu` (the `CNAME` file sets it). Tick "Enforce HTTPS" once the certificate is issued.

## DNS at Rackhost

Replace the two existing A records (91.227.139.235) with GitHub Pages addresses:

| Hosztnév | Típus | Érték |
|---|---|---|
| (empty) | A | 185.199.108.153 |
| (empty) | A | 185.199.109.153 |
| (empty) | A | 185.199.110.153 |
| (empty) | A | 185.199.111.153 |
| www | CNAME | `areteappshu.github.io` |

Do not touch the MX, SPF, DKIM, DMARC or Google verification records. Email keeps working.

## Preview locally

```
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Rights

© 2026 Areté Apps Kft. All rights reserved. Fonts are licensed under the SIL Open Font License; see `fonts/`.
