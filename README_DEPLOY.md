# Aircon Partner — GitHub Pages deployment

This folder is ready for GitHub Pages.

## Included
- `index.html` — full one-page website
- `styles.css` — site styling
- `CNAME` — sets the custom domain to `airconpartner.co.uk`
- `.nojekyll` — disables Jekyll processing

## Important: quote form
The temporary static-hosting version opens the visitor's email client with the completed project details addressed to:
`hello@airconpartner.co.uk`

This avoids sending customer data to an unapproved third-party form processor.

Before paid advertising, replace this with a proper server-side form endpoint / CRM workflow.

## GitHub Pages
1. Create a repository named `aircon-partner-site`.
2. Upload all files from this folder to the repository root.
3. GitHub → Settings → Pages.
4. Source: Deploy from a branch.
5. Branch: `main`, folder `/ (root)`.
6. Save.
7. In GitHub Pages, set custom domain: `airconpartner.co.uk`.

## GoDaddy DNS
Do not change nameservers and do not delete MX/TXT records for Microsoft 365.

For an apex GitHub Pages domain, GitHub normally requires these A records:
- `@` → `185.199.108.153`
- `@` → `185.199.109.153`
- `@` → `185.199.110.153`
- `@` → `185.199.111.153`

For `www`, add a CNAME to your GitHub Pages hostname, which depends on your GitHub username:
`<YOUR-GITHUB-USERNAME>.github.io`

Remove/replace only conflicting website A/CNAME records. Leave MX, SPF, DKIM and DMARC records alone.

After DNS resolves, enable “Enforce HTTPS” in GitHub Pages.
