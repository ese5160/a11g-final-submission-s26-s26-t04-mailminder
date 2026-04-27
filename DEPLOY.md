# Publish MailMinder to a public URL

The site is a plain static folder — `index.html` + `styles.css` + `images/`.
Pick one of the three options below.

---

## Option A — Vercel (recommended, clean URL, ~2 min)

1. Push the `website/` folder to GitHub on `main` (it's already in your repo
   if you commit + push it).
2. Go to <https://vercel.com/new> and sign in with GitHub.
3. Click **Import** on `ese5160/final-project-firmware-s26-t04-mailminder`.
4. In the import form:
   - **Framework Preset**: *Other*
   - **Root Directory**: click *Edit* → choose `website`
   - Leave Build Command + Output blank (it's a pure static folder).
5. Click **Deploy**.

You will get a URL like:

```
https://final-project-firmware-s26-t04-mailminder.vercel.app/
```

You can rename the project in Vercel → Settings → General to get something like
`https://mailminder.vercel.app/`.

---

## Option B — Netlify Drop (no account needed, instant)

1. Open <https://app.netlify.com/drop>.
2. Drag the entire `website/` folder onto the page.
3. You instantly get a URL like
   `https://random-name-12345.netlify.app/`.
4. (Optional) Click *Claim this site* to save it under your account and rename.

---

## Option C — GitHub Pages (uses your existing repo)

> Note: this repo is under the `ese5160` organization. If you can't enable Pages
> from the repo settings, ask the instructor to enable it once — after that you
> push as usual.

1. Commit and push the `website/` folder on `main`.
2. In GitHub → repo → **Settings → Pages**:
   - **Source**: *Deploy from a branch*
   - **Branch**: `main`  · **Folder**: `/website`
3. Save. After ~1 minute the URL appears at the top of the Pages page:

```
https://ese5160.github.io/final-project-firmware-s26-t04-mailminder/
```

---

## Local preview (no internet needed)

From the `website/` folder:

```bash
python -m http.server 8000
```

Then open <http://localhost:8000> in your browser.
