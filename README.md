# Portfolio — Setup & Deploy

## 1. Before you push: your links are already filled in
Your email, LinkedIn, and GitHub are already wired into `index.html` — nothing to edit there.

## 2. Push to GitHub
```bash
git init
git add .
git commit -m "Initial portfolio site"
git branch -M main
git remote add origin https://github.com/pksekharreddychinta/pksekharreddychinta.github.io.git
git push -u origin main
```
This exact repo name (`pksekharreddychinta.github.io`) gives you the cleanest
possible URL: **https://pksekharreddychinta.github.io** — no extra config needed.
Create a repo with this exact name on GitHub first (New repository → name it
`pksekharreddychinta.github.io` → Create, leave it empty, no README) before running
the commands above.

## 3. Turn on GitHub Pages (one-time)
In your repo on GitHub:
1. Go to **Settings → Pages**
2. Under "Build and deployment", set **Source** to **GitHub Actions**

That's it — the workflow in `.github/workflows/deploy.yml` will now run
automatically on every push to `main` and publish the site. Check the
**Actions** tab to watch it deploy; your live URL appears there and under
Settings → Pages once the first run finishes (usually under a minute).

## 4. Making future updates
Just edit `index.html` and push again:
```bash
git add .
git commit -m "Update portfolio"
git push
```
The Action redeploys automatically — no manual build step, no dashboard clicks.
