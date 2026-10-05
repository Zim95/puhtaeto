# Puhtaeto Portfolio

A dependency-free static portfolio built with HTML, CSS, and a small amount of JavaScript.

## Project structure

```text
puhtaeto-static/
├── index.html
├── styles.css
├── script.js
├── assets/
│   ├── puhtaeto-logo.jpg
│   └── namah-profile.jpeg
└── README.md
```

## Run locally

You can open `index.html` directly, or serve the directory locally:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Create the Git repository

```bash
git init
git add .
git commit -m "Initial Puhtaeto portfolio"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
git push -u origin main
```

## Deploy on Cloudflare Pages

1. Push this directory to a GitHub repository.
2. In Cloudflare, open **Workers & Pages** and select **Create application**.
3. Choose **Pages** and connect the GitHub repository.
4. Use these build settings:
   - Framework preset: `None`
   - Build command: leave empty
   - Build output directory: `/`
5. Deploy the project.

Cloudflare Pages will serve `index.html` from the repository root. Every push to `main` will trigger a new deployment.

## Connect `puhtaeto.com`

1. Open the deployed Pages project.
2. Go to **Custom domains**.
3. Select **Set up a custom domain**.
4. Enter `puhtaeto.com`.
5. If you also want `www.puhtaeto.com`, add it separately and redirect one hostname to the other.

If the domain already uses Cloudflare DNS, Cloudflare normally creates the required DNS records automatically.

## Editing the site

- Page content and links: `index.html`
- Colors, typography, layout, and responsive styles: `styles.css`
- Mobile navigation behavior: `script.js`
- Logo and profile image: `assets/`

Keep all paths relative so the site works locally, on Cloudflare Pages, and from any static web server.
