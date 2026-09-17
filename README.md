# JING

A static cinematic portfolio, ready for GitHub Pages. No build step is required.

## Site files

- `index.html`: root entry point, with page styles and behavior.
- `assets/videos/`: three web-optimized H.264 videos used by the page.
- `assets/images/`: video posters, favicon and grain texture.
- `assets/fonts/`: VT323 font; its SIL Open Font License is included in `index.html`.
- RESUME opens the supplied Google Drive link in a new tab. The local PDF backup remains in `originals/resume.pdf` and is not deployed.
- `.nojekyll`: serves the site as plain static files.
- `originals/`: locally preserved source videos and PDF backup, excluded from Git and deployment packages.

All bundled assets use document-relative URLs, with no leading slash. They work both at a domain root and under a repository subpath. Video URLs retain content-version queries for cache updates. External project/social links and the Tailwind/GSAP CDN scripts remain HTTPS URLs. The page does not require a backend.

## Publish to GitHub Pages

1. Create an empty GitHub repository, without adding a README, license or gitignore.
2. Commit the prepared files in this repository, connect the new repository as the `origin` remote, then push the `main` branch. No remote is configured automatically.
3. In the GitHub repository, open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Select **main**, choose **/ (root)**, and save.
6. Wait for the Pages deployment to succeed, then open the URL shown in Pages settings.

The commit and push commands, run inside this project folder, are:

```sh
git commit -m "Prepare JING portfolio for GitHub Pages"
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

Replace the two placeholders with your actual repository details. A project repository normally publishes under `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/`. A repository named `YOUR-USERNAME.github.io` publishes at the account site root.

Official instructions: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Check after publishing

- The page title is JING.
- Hero loads and follows scrolling in both directions.
- Both Featured Work videos load and play silently when visible.
- RESUME opens the supplied Google Drive resume link in a new tab.
- Navigation anchors remain on this page.

The local preparation does not create a GitHub repository, push files, or enable Pages. These actions must be completed before the site is online.
