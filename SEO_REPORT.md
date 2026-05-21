# SEO Report — sprayfoaminsulationtelluride
Date: 2026-05-21

## 1. Site Identity
- **Framework:** Static HTML (6 .html files, no Next.js/Astro config)
- **Target Audience:** Mountain home owners in Telluride, CO / San Miguel County seeking spray foam insulation services at 8,750+ ft elevation
- **Domain / Niche:** Local service business (spray foam insulation contractor)
- **Deployment Status:** Deployed to production (full domain URLs in canonical tags and og:url tags); no vercel.json, netlify.toml, or package.json found

## 2. Inventory
- **Total Pages:** 6 (.html files: index, services, service-areas, blog, contact, privacy-policy)
- **URL Structure:** Flat routing (all pages in root)
- **Sitemap:** sitemap.xml present (5 URLs listed; privacy-policy.html omitted)
- **Robots.txt:** Present and permissive (User-agent: *; Allow: /; Sitemap URL; crawl-delay: 1)

## 3. On-Page SEO (all 6 pages analyzed)

| Page | Title Length | Meta Description Length | H1 | Canonical | OG Tags |
|------|---|---|---|---|---|
| index.html | 78 chars | 145 chars | "Premium Insulation for High-Altitude Living" | ✓ https://sprayfoaminsulationtelluride.com/ | ✓ Full set (title, desc, type, locale, url, image 1200x630) |
| services.html | 94 chars | 162 chars | "Advanced Insulation Solutions" | ✓ /services | Partial (image only; missing og:title/og:description) |
| service-areas.html | 78 chars | 158 chars | "San Miguel County Expert" | ✓ /service-areas | Partial (image only) |
| blog.html | 91 chars | 165 chars | "Technical Insights." | ✓ /blog | Partial (image only) |
| contact.html | 82 chars | 149 chars | "Secure Your Comfort Zone." | ✓ /contact | Partial (image only) |
| privacy-policy.html | 33 chars | 136 chars | "Privacy Policy" | ✓ /privacy-policy | ✗ No OG tags; robots: noindex, nofollow |

**Issues Found:**
- services.html, service-areas.html, blog.html, contact.html missing og:title and og:description (~line 13 in each)
- All pages have title length 33–94 chars and descriptions 136–165 chars
- All pages have unique H1

## 4. Structured Data
**Present:**
- **LocalBusiness schema** (index.html, lines 72–112): name, image, phone, email, address, geo (37.9375, -107.8123), areaServed (7 towns), priceRange, openingHours
- **FAQPage schema** (services.html, lines 27–66): 4 Q/A on open vs. closed cell, energy savings, health, lifespan
- **ContactPage schema** (contact.html, lines 60–68): minimal

**Missing:**
- BreadcrumbList (visible in UI but no JSON-LD)
- Service schema for individual offerings
- Review / AggregateRating

## 5. Content Quality

**Word counts:**
- index.html: 2,032 words
- services.html: 1,783 words
- blog.html: 1,522 words

**Internal linking:** index.html has 29 internal links; consistent nav across all pages; blog article links are placeholder `#`

**Images:** 24 total, 24/24 with alt attributes (100% coverage); most descriptive, 3 generic on blog previews

## 6. Technical

**robots.txt:**
```
User-agent: *
Allow: /
Crawl-delay: 1
Sitemap: https://sprayfoaminsulationtelluride.com/sitemap.xml
```

**Sitemap:**
- 5 URLs; lastmod 2026-04-01 (stale by 50 days)
- privacy-policy.html omitted (correct — marked noindex)
- changefreq: weekly main pages, monthly for contact

**404 Handling:** Not tested (static site; server-config dependent)
**Redirects/Headers:** No next.config.js, netlify.toml, or vercel.json found

## 7. Top Issues (ranked)

1. **Outdated Sitemap** — lastmod 2026-04-01 (50+ days stale). sitemap.xml lines 4–32.
2. **Missing OG Tags on 4 Service Pages** — services, service-areas, blog, contact lack og:title and og:description (~line 13 each).
3. **Incomplete Structured Data** — No BreadcrumbList, Service, or Review schemas.
4. **Blog Links Are Placeholder** — blog.html lines 161, 169, 186, 196, 210, 220, 228 use `#`.
5. **Contact Page Schema URL Mismatch** — contact.html line 65: "telluridesprayfoam.com" vs. actual "sprayfoaminsulationtelluride.com".
6. **CDN Images from picsum.photos** — 24 images load from picsum.photos placeholder URLs. Production risk + SEO dilution.
7. **No hreflang** — Low impact for English-only site.
8. **Privacy Policy Noindex** — Correct practice; minor crawl-budget note.
9. **No mobile-first meta tag** — Viewport correct, no explicit declaration. Minor.
10. **HTTP image URLs in calculator** — blog.html line 304: external picsum.photos references.

## 8. Top Recommendations

1. **Update sitemap.xml lastmod** to 2026-05-21 and re-submit to GSC.
2. **Add og:title and og:description** to services, service-areas, blog, contact.html.
3. **Add BreadcrumbList JSON-LD** to non-home pages.
4. **Replace placeholder blog links** with real URLs or remove until articles ship.
5. **Fix ContactPage schema URL** on contact.html line 65.
6. **Replace picsum.photos placeholders** with local/optimized production images.
7. **Add Service schema** for open cell, closed cell, attic, crawl space (services.html, around lines 163, 186, 209, 232).
8. **Add AggregateRating** to LocalBusiness once reviews are collected.

---

**Status:** ⚠️ needs work
**Headline:** Strong fundamentals (100% alt text, LocalBusiness + FAQ schema, flat crawlable architecture) undermined by stale sitemap, missing OG tags on 4 pages, placeholder picsum.photos images, and incomplete structured data.
