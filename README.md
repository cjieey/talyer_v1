# Talyer Tally website

Landing page plus the live demo app for Talyer Tally. It is a plain static
site with no build step, so it runs on Vercel, Netlify or GitHub Pages as is.

```
index.html          the landing page
favicon.svg         browser tab icon
og-image.png        preview image when the link is shared on Facebook / Messenger
vercel.json         small Vercel settings for the demo app
app/                the live demo (installable PWA)
  index.html
  manifest.webmanifest
  sw.js
  icon.svg
```

## 1. Put it on GitHub (no Git needed)

1. Sign in at https://github.com and click **New** to create a repository,
   for example `talyer-tally-site`. Leave it empty (no README).
2. On the new repository page, click **uploading an existing file**.
3. Open the extracted `talyer-tally-site` folder on your computer, select
   **everything inside it** (index.html, app, vercel.json and the rest) and
   drag it into the browser. Upload what is inside the folder, not the
   folder itself, so `index.html` ends up at the top of the repository.
4. Click **Commit changes**.

If you use Git on the command line instead:

```
cd talyer-tally-site
git init
git add .
git commit -m "Talyer Tally website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/talyer-tally-site.git
git push -u origin main
```

## 2. Deploy on Vercel

1. Go to https://vercel.com and sign in with your GitHub account.
2. Click **Add New → Project**, then **Import** next to `talyer-tally-site`.
3. Set **Framework Preset** to **Other**. Leave Build Command and Output
   Directory empty.
4. Click **Deploy**. After about a minute you get a link like
   `talyer-tally-site.vercel.app`.

Every time you change a file on GitHub, Vercel publishes the new version
by itself.

## 3. Optional: your own domain

In Vercel open the project, go to **Settings → Domains**, add your domain
(for example `talyertally.ph`) and follow the DNS steps it shows.

## Editing

- Text, colors and sections are all in `index.html`. Colors are at the top
  of the `<style>` block (`--accent` is the orange).
- The demo app is `app/index.html`. To update it, replace the files in
  `app/` with a new build of the app.
- After you deploy, open your real link in https://www.opengraph.xyz to check
  the share preview. If Facebook shows an old image, paste the link into
  https://developers.facebook.com/tools/debug and click **Scrape Again**.
