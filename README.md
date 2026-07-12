# Aoufi Labs — GitHub Pages site

Static site (pure HTML + one shared CSS file, no build step) covering all three apps:
VaultCam, Board Vision, and Brain Arena. Built per TASK 3 of `VAULTCAM_TASKS.md`.

```
/index.html             Aoufi Labs portfolio (cards for the 3 apps)
/app-ads.txt            AdMob authorization — MUST stay at the domain root
/style.css              shared stylesheet (dark, mobile-first, system fonts)
/vaultcam/index.html    VaultCam landing (trust-first)
/vaultcam/privacy.html  VaultCam privacy policy (offline, NPA-only ads)
/boardvision/…          Board Vision landing + privacy
/brainarena/…           Brain Arena "coming soon" + privacy
```

## How to deploy (one time)

1. Create a **public** GitHub repo named exactly `<your-username>.github.io`
   (this is the "user site" — files are served from the domain root, which is
   required for `app-ads.txt` to be crawlable).
2. Push the contents of this folder to that repo's `main` branch:
   ```
   cd aoufi-labs-site
   git init
   git add .
   git commit -m "Aoufi Labs site"
   git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
   git push -u origin main
   ```
3. Wait a minute, then verify:
   - `https://<your-username>.github.io/` shows the portfolio
   - `https://<your-username>.github.io/app-ads.txt` shows the AdMob line

## Manual follow-ups after deploy (from VAULTCAM_TASKS.md)

1. In **Play Console**, set each app's *Store settings → website* field:
   - VaultCam    → `https://<your-username>.github.io/vaultcam/`
   - Board Vision → `https://<your-username>.github.io/boardvision/`
   - Brain Arena → `https://<your-username>.github.io/brainarena/`
   (The developer website's **root domain** is what AdMob crawls for app-ads.txt.)
2. Update each listing's **privacy policy URL** to the matching `…/privacy.html`.
3. In **AdMob → Apps → app-ads.txt**, re-check/verify so it crawls the new domain root.
4. Play Console public developer name → **Aoufi Labs** (human checklist item).
