# Gooji — Public Pages

Hosting repo for Gooji's App Store support, privacy, and terms pages.
Served via GitHub Pages so the URLs can be used in App Store Connect.

## Pages

| File | App Store Connect field |
|------|-------------------------|
| `support.html` | Support URL (required) |
| `privacy-policy.html` | Privacy Policy URL (required) |
| `terms-of-service.html` | (linked from app / privacy) |
| `index.html` | Landing page |

## Before publishing

Fill in every `[BRACKETED]` placeholder across all HTML files:

- `[COMPANY]` — your name or LLC
- `[SUPPORT_EMAIL]` — e.g. support@gooji.app
- `[EFFECTIVE_DATE]` — publish date
- `[JURISDICTION]` — e.g. "the State of California, USA"
- `[RESPONSE_TIME]` — e.g. "1–2 business days"
- `[MAILING_ADDRESS]` — optional; delete the bracketed clause if unused
- Pricing line in `support.html`

> These are starter templates, not legal advice. Have them reviewed by
> a qualified attorney before relying on them.

## Publish to GitHub Pages (free, public repo)

```bash
# 1. Create a new PUBLIC repo on github.com (e.g. "gooji-pages"), then:
git init
git add -A
git commit -m "Gooji public pages"
git branch -M main
git remote add origin https://github.com/<your-username>/gooji-pages.git
git push -u origin main
```

Then on GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `/ (root)` → Save.**

After a minute your URLs will be live at:

```
https://<your-username>.github.io/gooji-pages/support.html
https://<your-username>.github.io/gooji-pages/privacy-policy.html
https://<your-username>.github.io/gooji-pages/terms-of-service.html
```

The `.nojekyll` file tells GitHub Pages to serve the HTML as-is.

## Custom domain (optional, later)

If you buy `gooji.app`, add a `CNAME` file containing the domain and
configure it under Settings → Pages → Custom domain. Your URLs become
`https://gooji.app/privacy-policy.html`, etc.
