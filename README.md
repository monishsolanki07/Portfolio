# Monish Solanki — Portfolio

A single-page personal portfolio. Zero build step — it's just static `index.html`
(all CSS/JS inline, fonts loaded from Google Fonts).

## Structure

```
Portfolio/
├── index.html      # the whole site
├── vercel.json     # static-hosting config (clean URLs + headers)
├── .gitignore
└── README.md
```

## Run locally

Just open the file:

```bash
open index.html
```

Or serve it (recommended, matches production):

```bash
python3 -m http.server 3000
# visit http://localhost:3000
```

## Deploy to Vercel

### Option A — Vercel CLI (fastest)

```bash
npm i -g vercel      # once
cd /Users/monish.solanki/Documents/Portfolio
vercel               # first run: log in + answer prompts (accept defaults)
vercel --prod        # deploy to your production URL
```

When asked for settings, accept the defaults — Vercel auto-detects a static site,
so **no build command and no output directory** are needed.

### Option B — GitHub → Vercel (auto-deploy on push)

1. Create a repo and push:
   ```bash
   cd /Users/monish.solanki/Documents/Portfolio
   git add .
   git commit -m "Portfolio site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/portfolio.git
   git push -u origin main
   ```
2. Go to https://vercel.com/new, import the repo.
3. Framework preset: **Other** · Build command: *(empty)* · Output dir: *(empty)*.
4. Click **Deploy**. Every future `git push` redeploys automatically.

## Customize

- Social links (LinkedIn / GitHub / LeetCode) and the project "Live / GitHub"
  links are placeholders in `index.html` — replace the `href="#"` / `https://...`
  values with your real URLs.
