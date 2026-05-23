# Urban Gatekeeper — Landing Page

Smart property operations platform for gated communities, visitor security,
and sales associate teams. This repository hosts the public landing page.

## Files in this repo

| File           | Purpose                                                        |
|----------------|----------------------------------------------------------------|
| `index.html`   | The complete website — single self-contained file.             |
| `robots.txt`   | Tells search engines they may crawl the site.                  |
| `sitemap.xml`  | Lists the page for search-engine indexing.                     |
| `.nojekyll`    | Tells GitHub Pages to serve files as-is (do not remove).       |
| `CNAME`        | Created automatically by GitHub when you set a custom domain.  |

## Hosting (GitHub Pages)

1. Upload all files to the repository.
2. Go to **Settings → Pages**.
3. Source: **Deploy from a branch** → Branch: **main** → Folder: **/ (root)** → Save.
4. The site goes live at `https://<username>.github.io/<repo>/` within ~2 minutes.

## Connecting a custom domain (Hostinger)

1. **GitHub** → Settings → Pages → Custom domain → enter your domain → Save.
2. **Hostinger** → Domains → DNS Zone editor:
   - Add four **A** records for host `@` pointing to:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - Add one **CNAME** record: host `www` → `<username>.github.io`
3. Wait for DNS to propagate, then enable **Enforce HTTPS** in GitHub Pages.

## IMPORTANT — before launch

### 1. Waitlist form (required)
The waitlist form will not save submissions until you connect a Google Sheet.
Open `index.html`, find this line near the bottom:

    const GOOGLE_SHEET_URL = 'PASTE_YOUR_GOOGLE_APPS_SCRIPT_WEB_APP_URL_HERE';

Follow the setup steps in `SETUP-google-sheet.txt` (kept separately, NOT in this
repo) to create the Sheet, deploy the Apps Script, and paste the resulting URL.

### 2. Domain references (required if domain differs)
`index.html` and `sitemap.xml` reference `https://urbangatekeeper.com/`.
If your live domain is different, find-and-replace it everywhere first.

### 3. Social share image (recommended)
The meta tags reference `og-image.jpg`. Add a 1200x630 image with that name
to the repo root so link shares show a preview picture.

## Book Demo

"Book Demo" buttons open the visitor's email client addressed to
`anoop.singh@coyasoft.com` with a pre-filled demo-request template.
