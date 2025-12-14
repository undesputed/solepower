## SolepowerTech (Static HTML Website)

This repository is a **static HTML website** (no build step, no framework). Pages are written as plain `.html` files with inline CSS/JS.

### Pages
- `index.html` — homepage / main guide
- `about.html` — about page
- `contact.html` — contact page

### Assets
- `img/` — images used by the pages
- `favicon.webp` — site favicon

### SEO / Crawling
- `robots.txt` — crawler rules + sitemap location
- `sitemap.xml` — list of indexable URLs (uses the **www** domain)
- `.htaccess` — Apache rewrite rules (currently redirects unknown URLs to `https://www.solepowertech.com/`)

### Mobile responsiveness
The site includes responsive CSS rules for common breakpoints (desktop/tablet/mobile). Tables use overflow scrolling on smaller screens.

### How to view locally
You can open files directly in a browser:
- Open `index.html` via `file://...`

For a more realistic environment (recommended), serve the folder with a simple local server.

### Adding a new page (recommended steps)
1. Copy an existing page structure (head + header/nav + main + footer).
2. Update:
   - `<title>` and `<meta name="description">`
   - canonical URL and OG/Twitter URLs
   - JSON-LD schema type (match the page: AboutPage/ContactPage/Article/etc.)
3. Add the page to `sitemap.xml`.

Use the full checklist here:
- `SEO_CHECKLIST.md`

### Notes
- Canonical/OG/Twitter URLs are intentionally set to **production** (`https://www.solepowertech.com/...`). When viewing locally via `file://`, those tags still point to production (this is expected for SEO).
# solepower
