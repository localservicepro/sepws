# SEPWS Pty Ltd — Website

Modern, SEO/GEO/AEO-optimised, **Webflow-ready** static website for **SEPWS Pty Ltd — South East Pressure Washing Services** (Morwell, Victoria).

Built in clean, semantic HTML + a single CSS design system + lightweight vanilla JS — no build step, no framework lock-in. Everything is self-contained and portable into Webflow, Squarespace, or any host.

---

## 📄 Pages

| File | Purpose | Primary keyword | H1 |
|------|---------|-----------------|-----|
| `index.html` | Homepage | Pressure Washing Traralgon | Pressure Washing in Traralgon & Across Gippsland |
| `pressure-washing.html` | Service | Pressure Washing Traralgon & Gippsland | Pressure Washing in Traralgon & Across Gippsland |
| `concrete-sealing.html` | Service | Concrete Sealing Traralgon | Concrete Sealing in Traralgon & the Latrobe Valley |
| `external-window-cleaning.html` | Service | External Window Cleaning Traralgon | External Window Cleaning in Traralgon & Gippsland |
| `about.html` | About | — | Your local exterior cleaning specialists |
| `contact.html` | Contact / Quote | — | Get your free quote today |

Shared assets: `css/styles.css`, `js/main.js`, `images/`, `favicon.svg`, `sitemap.xml`, `robots.txt`.

---

## 🎨 Brand design system

Built from SEPWS's existing "South East" blue identity, elevated to a modern 2026 look. All tokens live at the top of `css/styles.css` (`:root`).

- **Primary blue** `#0e6fd6` · **Fresh aqua accent** `#14c4e0` · **Deep navy ink** `#0a1b33`
- Light tints `#eaf4fe` / `#f4f9ff`, success green `#16a34a`, review-star gold `#ffb020`
- **Headings:** Sora (700/800) · **Body:** Inter — both via Google Fonts (Webflow-native)
- Rounded 18px cards, soft shadows, gradient hero, wave/gradient accents

> **Note on the Claude Design brand kit:** the supplied Claude Design homepage link
> (`claude.ai/design/p/...`) requires the `/design-login` OAuth flow, which isn't available
> in an automated build session, so it couldn't be imported directly. The design here was
> instead built from SEPWS's existing blue branding + the water/clean theme. If you'd like the
> exact Claude Design layout mirrored, share an exported HTML file and it can be matched.

---

## 🔍 SEO / GEO / AEO — mapped to the strategy doc

**On-page SEO**
- Unique, keyword-led `<title>` + **meta description on every page** (fixes the empty-meta issue flagged in the audit)
- One keyword-led `<h1>` per page, semantic H2/H3 hierarchy
- Canonical URLs, descriptive SEO-friendly image filenames + alt text on every image
- Clean internal linking: Homepage → 3 service pages → Contact; footer + nav cross-links
- `sitemap.xml` + `robots.txt` (submit the sitemap in Google Search Console)

**Structured data (GEO — AI search)**
- `LocalBusiness` / `HomeAndConstructionBusiness` schema with NAP, geo-coordinates, opening hours, `areaServed`, `sameAs` socials, and `makesOffer`
- `Service` schema on each service page · `BreadcrumbList` on inner pages · `WebSite` + `AboutPage` / `ContactPage`
- Consistent NAP entity signals across site, footer, and schema (match your Google Business Profile exactly)

**Answer Engine Optimisation (AEO — voice / featured snippets)**
- `FAQPage` schema on the homepage and every service/contact page
- FAQ headings phrased as natural spoken questions ("How much does pressure washing cost in Traralgon?") with concise, direct, citable answers
- Explicit "welcome" rules for GPTBot / PerplexityBot / Google-Extended in `robots.txt`

**Performance / UX**
- `.webp` imagery, `loading="lazy"` (hero uses `fetchpriority="high"`), width/height on images to reduce layout shift
- Mobile-first responsive, sticky header, mobile menu, fixed Call/Quote bar, scroll-reveal + counters, `prefers-reduced-motion` respected

---

## 🧩 Webflow import notes

The markup is intentionally Webflow-friendly:
- Semantic HTML5 with clear, single class names (easy to recreate as Webflow classes/combo classes)
- Repeated **header** and **footer** — in Webflow, convert each into a **Symbol/Component** once, then reuse
- All CSS in one stylesheet; paste tokens/utilities into Webflow's custom CSS embed, or rebuild the handful of components visually
- JS (`js/main.js`) is a single vanilla file — drop it into **Project Settings → Custom Code → Footer**, or before `</body>`
- The **contact form** uses a standard `<form>` with named fields + a honeypot. On import, connect it to **Webflow Forms** (or Formspree/Netlify). `action="#"` is a placeholder.
- Google Fonts (Sora + Inter) — add them in Webflow's Fonts panel

---

## ✅ Before you go live — client checklist

1. **Testimonials** — the 3 homepage reviews are clearly-marked **placeholders**. Replace with genuine quotes from your Google Business Profile (see the HTML comment above the testimonials section).
2. **Business facts** — confirm **opening hours** (currently Mon–Sat 7am–6pm), **"fully insured"** claim, and add your **ABN** if you'd like it displayed.
3. **Contact form** — connect it to your preferred form handler so submissions reach `sepwsmelbourne@gmail.com`.
4. **Google Search Console** — verify the domain and submit `sitemap.xml`; request indexing on each new page.
5. **NAP consistency** — make sure the address/phone match your Google Business Profile, Facebook and Instagram exactly.
6. **Optional** — add suburb landing pages (Traralgon, Morwell, Warragul, Pakenham, Berwick, Mornington) as outlined in the strategy for more "service + suburb" ranking entry points.

---

## 🖼️ Image manifest

All 22 photos are genuine SEPWS job images from the client's Google Drive, renamed to SEO-friendly filenames. Full Drive-ID → filename mapping is in [`images/IMAGE-MANIFEST.md`](images/IMAGE-MANIFEST.md).
