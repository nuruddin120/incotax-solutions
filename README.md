# IncoTax Solutions — Website

A single-file, production-ready marketing website for **IncoTax Solutions** (cloud accounting + income tax services). Built with Tailwind CSS (compiled and inlined) and inline SVG icons — no build step, no external CDN dependency. It works by simply opening `index.html`.

## Files

| File | Purpose | Required? |
|------|---------|-----------|
| `index.html` | The entire website (HTML + CSS + JS, self-contained) | Yes |
| `vercel.json` | Clean URLs + a few sensible security headers | Optional |
| `README.md` | This file | No (just docs) |

> The only thing loaded from the internet at runtime is the **Inter** web font (Google Fonts). If it's ever blocked, the site automatically falls back to the system sans-serif font, so nothing breaks.

---

## Deploy with GitHub + Vercel

You can do this entirely from a browser — no terminal needed.

### Step 1 — Put the files on GitHub

**Option A: GitHub website (easiest, mobile-friendly)**
1. Go to <https://github.com/new> and create a new repository, e.g. `incotax-website`. Keep it Public or Private — both work with Vercel.
2. On the new repo page, click **uploading an existing file**.
3. Upload `index.html` (and optionally `vercel.json`). Make sure `index.html` is at the **root** of the repo, not inside a folder.
4. Click **Commit changes**.

**Option B: Git command line**
```bash
git init
git add index.html vercel.json
git commit -m "Initial IncoTax Solutions website"
git branch -M main
git remote add origin https://github.com/<your-username>/incotax-website.git
git push -u origin main
```

### Step 2 — Connect Vercel

1. Go to <https://vercel.com> and sign in with your GitHub account.
2. Click **Add New… → Project**.
3. Find your `incotax-website` repo and click **Import**.
4. Leave all settings as default:
   - **Framework Preset:** `Other` (Vercel auto-detects a static site)
   - **Build Command:** leave empty
   - **Output Directory:** leave empty (it serves the repo root)
5. Click **Deploy**.

After ~20–30 seconds you'll get a live URL like:
```
https://incotax-website.vercel.app
```

### Step 3 — (Optional) Add your own domain

1. In your Vercel project, open **Settings → Domains**.
2. Add your domain (e.g. `incotaxsolutions.com`).
3. Update the DNS records at your domain registrar as Vercel instructs (usually an `A` record or a `CNAME`).

---

## Updating the site later

Any time you change `index.html` and push the change to GitHub (or re-upload it on the GitHub website), Vercel automatically rebuilds and redeploys within seconds. No extra steps.

---

## Quick reference: what's wired up in the site

- **Schedule Free Call** → dials `+880 1346 808902` (shows a confirmation first)
- **Start with a free consultation** & **Book My Free Consultation** → open a WhatsApp chat to `+880 1346 808902` (the form fields are passed along as a prefilled message)
- **Email:** incotaxsolutions@gmail.com
- **Social:** Facebook (`/IncoTaxBD`) and LinkedIn (`/company/incotax-solutions`)

> **Note:** The contact form opens WhatsApp rather than sending email server-side (a static site can't run a backend). If you later want submissions delivered to your inbox, you can connect a free form service like [Formspree](https://formspree.io) or [Web3Forms](https://web3forms.com) — just ask and it can be added.
