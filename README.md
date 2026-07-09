# pushkarbhuse.com

Personal website for Pushkar Bhuse — a single self-contained `index.html`
(all fonts, runtime, and the animated background are inlined; no build step).

## Deploy with GitHub Pages

1. Create a new GitHub repository (e.g. `pushkarbhuse-site`).
2. Upload the contents of this `site/` folder to the repo root:
   - `index.html`
   - `CNAME`  (contains `pushkarbhuse.com` — tells Pages your custom domain)
3. In the repo: **Settings → Pages → Build and deployment**
   - Source: **Deploy from a branch**
   - Branch: **main** / **/(root)** → Save
4. Still under Settings → Pages, confirm the **Custom domain** shows
   `pushkarbhuse.com`, then tick **Enforce HTTPS** (available once DNS resolves).

## Point GoDaddy at GitHub Pages

In **GoDaddy → My Products → DNS** for pushkarbhuse.com:

- Four **A records** for host `@` pointing to GitHub Pages:
  - `185.199.108.153`
  - `185.199.109.153`
  - `185.199.110.153`
  - `185.199.111.153`
- One **CNAME record**: host `www` → `<your-github-username>.github.io`

DNS can take 10 minutes to a few hours to propagate. Once it does, GitHub
issues a free SSL certificate automatically.

## Updating the site later

Replace `index.html` with a newer build and commit — Pages redeploys on push.
