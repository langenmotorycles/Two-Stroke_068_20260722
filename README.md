# Langen Two-Stroke 024 — Certified Pre-Owned Flipbook

A static, browser-based flipbook for **LANGEN TWO-STROKE 024, CERTIFIED PRE-OWNED**.

The source PDF is embedded directly in `index.html`. No server, database, package installation, or build command is required.

## Publish with GitHub Pages

### 1. Create the repository

1. Sign in to GitHub.
2. Create a new repository, for example `langen-two-stroke-024`.
3. Choose **Public** if your GitHub plan requires a public repository for Pages.
4. Do not initialise it with another README, `.gitignore`, or licence.

### 2. Upload these files

Upload the entire contents of this folder, preserving the `.github/workflows/deploy-pages.yml` path.

You can upload through GitHub's web interface, or use Git:

```bash
git init
git add .
git commit -m "Publish Langen Two-Stroke 024 flipbook"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

### 3. Enable GitHub Pages

1. Open the repository on GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, select **GitHub Actions** as the source.
4. Open the **Actions** tab and confirm that the “Deploy to GitHub Pages” workflow completes successfully.

The published address will normally be:

```text
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/
```

For an organisation repository, replace `YOUR-USERNAME` with the organisation name.

## Update the site

Replace `index.html`, commit, and push to `main`. The included workflow redeploys the site automatically.

## Custom domain

In **Settings → Pages**, enter the custom domain. GitHub will create or update the `CNAME` file. Configure the DNS records shown by GitHub, then enable **Enforce HTTPS** after DNS verification succeeds.

## Local preview

Because the page uses JavaScript modules, preview it through a local web server rather than opening `index.html` directly:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Runtime dependencies

The page fetches these resources when opened:

- Google Fonts (`fonts.googleapis.com`)
- PDF.js 6.1.200, with jsDelivr as the primary source and unpkg as fallback
- PageFlip 2.0.7, with jsDelivr as the primary source and unpkg as fallback

The embedded PDF and all catalogue content remain inside `index.html`. An internet connection is still required for the libraries above unless they are downloaded and hosted locally.

## Repository contents

- `index.html` — complete flipbook and embedded PDF
- `.github/workflows/deploy-pages.yml` — automatic GitHub Pages deployment
- `.nojekyll` — disables Jekyll processing
- `404.html` — returns visitors to the flipbook root
- `README.md` — publishing and maintenance instructions

## Important checks before publishing

- Confirm you have permission to publish the catalogue, photographs, trademarks, contact details, and embedded PDF.
- Test the PDF download button, page navigation, fullscreen mode, mobile layout, and email links after deployment.
- The repository will contain the original PDF data in readable/downloadable form. Do not use a public repository if the document is confidential.
