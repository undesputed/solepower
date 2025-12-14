## HTML Website SEO Optimization Checklist

Use this checklist when creating or updating any HTML page.

### Site-wide (do once)
- **Domain consistency**: choose one (e.g. `https://www.solepowertech.com`) and use it everywhere.
- **Redirects**: enforce HTTPS + chosen domain (www/non-www) with 301 redirects.
- **robots.txt**
  - Allow/disallow rules as needed
  - `Sitemap: https://www.yourdomain.com/sitemap.xml`
- **sitemap.xml**
  - Include every indexable URL
  - Use canonical URLs only (no duplicates, no double slashes)
  - Keep `lastmod` updated if you use it
- **404/redirect behavior**
  - Real 404 for missing pages (don’t send everything to homepage)
  - Use 301 for permanent moves
- **Performance basics**
  - Compress images (WebP/AVIF when possible)
  - Avoid huge inline images/styles that block rendering
  - Add caching headers on static assets (server/CDN)

### Per-page (every page)
- **HTML basics**
  - `<!doctype html>` and valid HTML
  - `<html lang="…">` (e.g. `en-AU`)
  - One `<h1>` per page; logical heading order (`h2` → `h3`…)
- **Core meta tags**
  - `<title>` unique per page
  - `<meta name="description">` unique per page
  - `<link rel="canonical" href="https://www.yourdomain.com/your-page">`
  - `<meta name="robots" content="index,follow">` (or noindex when needed)
- **Open Graph (social sharing)**
  - `og:type` (article for guides/posts, website for generic pages)
  - `og:url`, `og:title`, `og:description`
  - `og:image` + `og:image:alt`
  - Optional: `og:site_name`, `og:locale`
- **Twitter card**
  - `twitter:card`, `twitter:url`, `twitter:title`, `twitter:description`, `twitter:image`
- **Structured data (JSON-LD)**
  - Use the **correct schema type** for the page:
    - Home/guide: `Article` (optional) + `Organization` + `BreadcrumbList`
    - About: `AboutPage` + `Organization` + `BreadcrumbList`
    - Contact: `ContactPage` + `Organization` (+ `ContactPoint`) + `BreadcrumbList`
    - Blog post: `Article` (or `BlogPosting`) + `Organization/Person` + `BreadcrumbList`
    - FAQ-heavy page: `FAQPage` (only if the page truly contains FAQs)
  - Make sure JSON-LD `url`/`@id` match the page’s canonical URL.
  - Do not paste homepage schema onto other pages.
- **Accessibility (helps SEO + UX)**
  - Landmarks: `<header> <nav> <main> <footer>`
  - Add a skip link: `Skip to main content`
  - Images have meaningful `alt` (or empty alt for decorative images)
  - Buttons are real `<button>` elements (not clickable `<div>`)
  - Keyboard navigation works
- **Mobile responsiveness**
  - `<meta name="viewport" content="width=device-width,initial-scale=1">`
  - No horizontal scrolling except intentional table/overflow areas
  - Tables: wrap in an overflow container for small screens
  - Images: responsive (`max-width: 100%; height: auto;`)
- **Links**
  - Internal links use the correct relative/absolute paths
  - External links opened in a new tab use `rel="noopener noreferrer"`

### Content quality (per page)
- **Match search intent**: page topic is clear in H1 + intro.
- **Semantic sections**: use headings for major sections.
- **Avoid duplication**: don’t reuse the same title/description across pages.

### Quick validation (before publish)
- **Manual checks**
  - View-source: title/description/canonical correct
  - Resize: 1200px / 768px / 480px / 375px
  - Verify no layout overflow
- **Tools**
  - Google Rich Results Test (schema)
  - Lighthouse (SEO + Accessibility)
  - W3C HTML validation (optional but helpful)

### Notes / placeholders to replace
- Replace `www.yourdomain.com` with your production domain.
- Ensure social images exist at the referenced URLs.
