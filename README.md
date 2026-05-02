# PerformanceNet.ai Landing Page

Production landing page for PerformanceNet — federal-grade AI integration for commercial enterprise.

Single-file static site. No build step required.

## Local preview

Open `index.html` directly in any browser, or serve locally:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to Vercel

1. Push this repo to GitHub.
2. At https://vercel.com/new, import the repo.
3. Framework preset: **Other** (no build command, no output directory override).
4. Click Deploy.

## Connect performancenet.ai (GoDaddy → Vercel)

After the first deploy:

1. **Vercel** → Project → Settings → Domains → add `performancenet.ai` and `www.performancenet.ai`.
2. **GoDaddy** → My Products → DNS → Manage DNS → `performancenet.ai`:
   - **A record**: name `@`, value `76.76.21.21`
   - **CNAME**: name `www`, value `cname.vercel-dns.com`
   - Remove any conflicting default `@` A or `www` CNAME records (e.g. GoDaddy's parking page).
3. Wait 5–60 minutes for DNS propagation. Vercel auto-issues the SSL certificate.

## File structure

```
.
├─ index.html              # Entire site (inline CSS, single file)
├─ vercel.json             # Caching + security headers
├─ assets/
│   ├─ performancenet-mark.png             (used in header)
│   ├─ performancenet-logo.png             (brand asset)
│   ├─ performancenet-logo-transparent.png (brand asset)
│   └─ one-pager.jpg                       (brand asset)
└─ README.md
```

## Editing content

All copy, layout, and styling lives in `index.html`. Open in any text editor.
