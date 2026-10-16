# Elegant Tern Labs website

Static HTML/CSS landing page for [Elegant Tern Labs](https://github.com/elegant-tern-labs), an independent San Diego R&D studio building experimental games and software tools.

**Status:** a studio introduction with contact links, not a product catalog or application. This repository contains the public website; development repositories may remain private.

## Structure

- `index.html` — page content, studio identity, logo, and GitHub/X/email links.
- `css/style.css` — layout, typography, and colors.
- `logo.png` — studio logo.
- `CNAME` — the custom domain, `elegantternlabs.com`.

There is no application framework or package/build manifest. The page loads the Inter typeface from Google Fonts; external font loading requires network access.

## Local preview

From the repository root, serve the existing files with Python 3:

```bash
python3 -m http.server 8080 --bind 127.0.0.1
```

Open `http://127.0.0.1:8080`. A local preview does not test GitHub Pages publishing, DNS, custom-domain ownership, or HTTPS.

## Publishing and maintenance

The repository follows the GitHub Pages organization-site naming convention. Check **Settings → Pages** for the actual publishing source before assuming that a particular branch or workflow deploys it. Keep `CNAME`, Pages custom-domain settings, and DNS consistent. Do not replace the domain or DNS records as part of a content-only update.

The organization overview lives in [`.github/profile/README.md`](https://github.com/elegant-tern-labs/.github/blob/main/profile/README.md); link to that overview rather than duplicating private project information here.

## Known issues and verification

- On October 15, 2026, a request to `https://elegantternlabs.com` failed certificate hostname verification, and `https://elegant-tern-labs.github.io` redirected to the HTTP custom-domain URL. These observations do not establish the cause. Verify DNS, the Pages custom-domain configuration, certificate provisioning, and HTTPS enforcement before treating the site as HTTPS-ready. Do not work around certificate errors by disabling verification.
- `css/style.css` currently ends with an unfinished `.logo {` rule. Its fixed viewport height and hidden overflow also warrant checking on short/narrow screens. This documentation update does not change the styles.
- Verify the logo, external links, keyboard navigation, and layout on desktop and mobile before publishing visual changes.

No browser, accessibility, or deployment test result is claimed by this README. DNS, TLS settings, and site code were not changed as part of the documentation update.
