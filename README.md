# SMPL Works Landing Page

A minimal static page: the SMPL Works logo, “When less is more.”, and a GitHub link that opens in a new tab.

- Website: https://smplworks.app/
- Private repository: https://github.com/smpl-works/smpl-works.github.io
- Plain HTML, CSS, and SVG. No JavaScript, dependencies, build process, analytics, or external fonts.
- Palette and type match the Lotus project's dark theme: charcoal `#181817`, warm white `#eee9e1`, rose `#dbab9f`, Segoe UI Variable / Segoe UI, and Georgia headings.

## Edit and preview

Open `index.html` in a browser, or serve this folder with any static HTTP server. Edit the slogan and GitHub URL in `index.html`; edit colors and layout in `styles.css`. Keep the SVG favicon consistent with the logo.

## Publish

Push changes to `main`. GitHub Pages is configured to publish from **main → / (root)**. Keep `.nojekyll` and the `CNAME` file containing `smplworks.app`.

```powershell
git add index.html styles.css favicon.svg README.md
git commit -m "Update SMPL Works landing page"
git push origin main
```

The source repository is private; the published landing page is public. GitHub Pages hosting from private repositories requires an eligible GitHub plan.

## Domain

Squarespace manages the DNS. GitHub has verified ownership of `smplworks.app`. Retain its verification TXT record and unrelated email-security and Domain Connect records.

| Type | Host | Value |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | smpl-works.github.io |

The canonical address is `https://smplworks.app/`; GitHub Pages has HTTPS enforcement enabled. Verify both HTTP and HTTPS redirects from `www` after domain or certificate changes.
