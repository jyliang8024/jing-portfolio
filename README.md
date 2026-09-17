# JING

A static cinematic portfolio. No build step is required.

- Website: https://jyliang8024.github.io/jing-portfolio/
- Repository: https://github.com/jyliang8024/jing-portfolio
- GitHub Pages source: `main`, `/ (root)`

## Site files

- `index.html`: root entry point, page styles and behavior.
- `assets/videos/`: three web-optimized H.264 videos.
- `assets/images/`: video posters, favicon and grain texture.
- `assets/fonts/`: VT323 font; its SIL Open Font License is included in `index.html`.
- `.nojekyll`: serves the site as plain static files.
- `originals/`: local source videos and PDF backup; excluded from Git and deployment packages.

RESUME opens the supplied Google Drive link in a new tab. The local PDF backup is not deployed.

All bundled assets use document-relative URLs without a leading slash, supporting both domain-root and repository-subpath deployment. Video URLs include content-version queries. External project/social links and the Tailwind/GSAP scripts use HTTPS URLs. No backend is required.

## Update the site

Edit the page or replace the corresponding assets, verify the result, then commit and push to `main`. The prepared local checkout uses `codex/github-pages`, tracking `origin/main`, so use an explicit destination:

```sh
git add index.html assets README.md .gitignore .nojekyll
git commit -m "Update JING portfolio"
git push origin HEAD:main
```

Update the matching video version query when replacing a video. Preserve original files in the ignored `originals/` folder.

GitHub Pages automatically redeploys after changes are pushed to `main`. Check the repository's **Actions** tab for deployment status, or **Settings → Pages** for the published URL.

## Verify after deployment

- The page title is JING.
- Hero loads and follows scrolling in both directions.
- Both Featured Work videos play silently when visible.
- RESUME opens Google Drive in a new tab.
- Navigation anchors remain under the site subpath.

Official documentation: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
