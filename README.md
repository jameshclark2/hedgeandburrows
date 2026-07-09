# Hedge & Burrows Limited — Website

Four pages: Home, Services, About, Contact. Built as plain HTML/CSS, no build step, no dependencies beyond Google Fonts.

## Deploying to GitHub Pages

1. Create a new repository on GitHub (e.g. `hedgeandburrows-site`). Keep it **public** — GitHub Pages on the free tier requires a public repo.
2. Upload all files in this folder to the repository root: `index.html`, `services.html`, `about.html`, `contact.html`, `styles.css`, `CNAME`, and the `assets` folder with both logo files inside it.
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`. Save.
5. GitHub will publish the site at `https://[your-username].github.io/hedgeandburrows-site/` within a few minutes. Confirm it works before moving to step 6.

## Connecting hedgesandburrows.com

The `CNAME` file in this folder already contains `hedgesandburrows.com` — GitHub Pages reads this automatically, you don't need to type it in again.

At your domain registrar (wherever you bought hedgesandburrows.com):

1. Add a **CNAME record**:
   - Host: `www`
   - Value: `[your-username].github.io`
2. Add **four A records** for the root domain (so `hedgesandburrows.com` without `www` also works), pointing to GitHub's IP addresses:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
3. Back in GitHub **Settings → Pages**, enter `hedgesandburrows.com` in the custom domain field and save. Tick **Enforce HTTPS** once it becomes available (can take up to 24 hours after DNS propagates).

DNS changes can take anywhere from ten minutes to 24 hours to take effect. If the site doesn't load immediately, wait and try again before troubleshooting.

## Making future edits

Each page is a separate `.html` file with the same header/footer structure. Text can be edited directly in GitHub's web interface (open the file, click the pencil icon, edit, commit) without needing any local tools. Any changes committed to `main` publish automatically within a minute or two.

## Files

```
index.html          Homepage
services.html        Garden maintenance + pest control detail
about.html            Louise's background
contact.html          Contact details, areas covered
styles.css             All styling
CNAME                    Custom domain config for GitHub Pages
assets/
  logo-mark.png       Cropped emblem (wordmark removed), used in header/hero/favicon
  logo-full.jpeg      Full original logo, used on About page
```

## Known open item

The logo emblem (owl, landscape, scales, wreath) is detailed and was designed for large-format use. At favicon and header size (52px) some detail is lost. This was flagged during build — worth showing Louise the live site and asking whether a simplified single-colour mark should be commissioned for small-size use, keeping the full illustration for print and the About page.
