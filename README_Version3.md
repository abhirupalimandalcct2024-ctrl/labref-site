# LabRef — Static site

This folder contains a ready-to-publish static website for LabRef.

Included files:
- `index.html` — main landing page
- `privacy.html` — privacy policy
- `styles.css` — shared stylesheet
- `favicon.svg` — small SVG favicon
- `site.webmanifest` — manifest for PWA metadata

Before publishing:
- Replace the contact email and update the "Last updated" date in `privacy.html`.
- Confirm Section 2 / Section 5 of `privacy.html` matches any analytics/ads/SDKs your app will use.
- Replace `favicon.svg` with your preferred icon file if needed.

Local testing:
- Open `index.html` in a browser, or serve with a simple local server:
  - Python 3: `python -m http.server 8080` then open `http://localhost:8080`
  - Node: `npx serve .`

Publishing options:
1. GitHub Pages
   - Create a repository, push these files to the `main` branch.
   - In repo Settings → Pages, set source to `main` branch (root).
   - The site will be served at `https://<username>.github.io/<repo>/` or your custom domain.

2. Vercel / Netlify
   - Drag & drop the folder in the dashboard, or connect your GitHub repo. Both services will auto-deploy on push.

3. Any static host (S3 + CloudFront, Surge.sh, Firebase Hosting, etc.) — upload the files to the host root.

Tips:
- For improved performance, consider serving fonts from your own CDN or subset the Google fonts used.
- Add analytics later (if used) and update the privacy policy accordingly.
- If you want automated builds and CI (minify CSS, images), I can provide a simple build script or GitHub Actions workflow.

If you'd like, I can:
- Create a ZIP of the files (I can't upload it here but I can give you a ready patch or a git commit diff).
- Provide a GitHub Pages-ready commit (diff) or a GitHub Actions workflow for automated deployment.
- Add optional GDPR/CCPA clauses to the privacy policy.