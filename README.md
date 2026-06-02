# Neodyad website

Minimal single-page site for GitHub Pages with a custom domain.

## Local preview

```bash
python3 -m http.server 8080
```

Open [http://localhost:8080](http://localhost:8080).

## Deploy to GitHub Pages

1. Create a public GitHub repository and push this folder.
2. In the repo: **Settings → Pages → Build and deployment**
   - Source: **Deploy from a branch**
   - Branch: `main` / **/ (root)**
3. Wait for the first deploy; the default URL will be `https://<user>.github.io/<repo>/` (unless the repo is named `<user>.github.io`, which serves at the root).

## Custom domain

1. Edit `CNAME` if your domain differs from `neodyad.com`.
2. In **Settings → Pages → Custom domain**, enter the same hostname and save.
3. At your DNS provider:

   | Host | Type | Value |
   |------|------|--------|
   | `www` (optional) | `CNAME` | `<user>.github.io` |
   | `@` (apex) | `A` | `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153` |

   Some providers support `ALIAS`/`ANAME` on apex pointing to `<user>.github.io` instead of four `A` records.

4. Enable **Enforce HTTPS** once DNS has propagated (can take up to 24 hours).

## Customize

- Copy and positioning: `index.html`
- Contact email: `mailto:` link in `index.html`
- Domain: `CNAME` and GitHub Pages custom domain setting
