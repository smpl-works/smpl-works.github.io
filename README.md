# SMPL Works Landing Page

A quiet, static home for SMPL Works. Plain HTML and CSS, with no JavaScript, dependencies, analytics, external fonts, or build step.

- Website: https://smplworks.app/
- Intended repository: https://github.com/smpl-works/smpl-works.github.io
- Source: `index.html`, `styles.css`, and `favicon.svg`.

## Preview and edit

Open `index.html` in a browser, or serve this folder using any static HTTP server. Edit text in `index.html` and colors, spacing, or layout in `styles.css`.

## Add an application

When the first application is ready, replace the entire `collection-empty` div in the Applications section with the following. Replace the sample title, description, and URL with real details before publishing. Additional `article` elements go inside the same `application-list` div. Existing CSS provides a two-column desktop layout and a single-column mobile layout.

```html
<div class="application-list">
  <article class="application-card">
    <h3>Your application name</h3>
    <p>A short, specific description of what the application helps you do.</p>
    <a class="text-link" href="https://your-application.example/">
      Open application <span aria-hidden="true">↗</span>
    </a>
  </article>
</div>
```

## Publish

Push changes to `main`. GitHub Pages should publish from **Deploy from a branch → main → / (root)**. The `.nojekyll` file keeps publishing static. The `CNAME` file contains the custom domain; keep it when editing the site.

```powershell
git add index.html styles.css favicon.svg README.md CNAME .nojekyll .gitignore
git commit -m "Update SMPL Works landing page"
git push origin main
```

## Domain setup

Configure `smplworks.app` in GitHub Pages settings **before changing DNS**. The domain's DNS is currently managed by Squarespace.

1. In the `smpl-works` account's **Settings → Pages**, add and verify `smplworks.app`. GitHub supplies a unique TXT record name and value. Add exactly those values in Squarespace DNS and retain the record after verification.
2. In the repository's **Settings → Pages**, set the custom domain to `smplworks.app`.
3. Replace the Squarespace website A records for `@` with these four GitHub Pages records. Replace the existing `www` CNAME with the value below. Leave unrelated MX, TXT, and other records unchanged.

| Type | Host | Value |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | smpl-works.github.io |

4. Once GitHub's DNS check and certificate provisioning succeed, enable **Enforce HTTPS**. GitHub redirects `www.smplworks.app` to the apex domain when both are correctly configured. DNS and certificate provisioning can take up to 24 hours.

See [GitHub's custom-domain documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).

## Verification

Check desktop and mobile layouts, keyboard navigation and focus, all links, and the page with JavaScript disabled. The page deliberately requests only its local stylesheet and favicon. Verify that DNS, HTTPS, and the `www` redirect work after changing domain settings.
