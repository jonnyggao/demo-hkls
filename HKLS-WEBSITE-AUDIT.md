# Hong Kong Language School — Website Audit & Modernization Plan

**Site reviewed:** [https://hkls.com.hk/](https://hkls.com.hk/)  
**Audit date:** 5 July 2026  
**Purpose:** Identify what works today, what should change for better SEO and UX, and open decisions that need your input before implementation.

---

## Executive summary

HKLS has a **credible, long-running language school** with strong social proof (recent 2026 testimonials), a prestigious corporate client list, and practical contact channels (phone, email, WhatsApp). The site is actively maintained — schedules reference June–September 2026 and content was updated in June 2026.

However, the site **looks and behaves like a legacy WordPress build from the late 2010s**. Information architecture, visual design, performance, and SEO fundamentals lag behind what prospective students expect in 2026. The homepage tries to do everything at once (marketing, gallery, videos, contact, enrollment, student login, testimonials), which hurts clarity and conversion.

**Highest-impact improvements:**

1. **Reposition and restructure** around clear user journeys (learn Cantonese → choose format → see schedule/pricing → enroll/contact).
2. **Fix SEO basics** — meta descriptions, page titles, structured data, sitemap hygiene.
3. **Modernize UX** — mobile-first layout, fewer popups, faster load, consistent branding, Cantonese-forward messaging.
4. **Decide platform strategy** — refresh current WordPress vs. rebuild on a modern stack.

---

## What is working well (keep or build on)

### Brand & trust signals

| Strength | Why it matters |
|----------|----------------|
| **Recent, detailed testimonials** | Lauren Thiesse (Feb–Mar 2026), Imran Shakir (8 years), Jordy Vos (Feb 2026), and others give authentic, specific stories — not generic praise. |
| **Corporate client list** | UBS, Citibank, Burberry, Baker & McKenzie, AXA, etc. — strong B2B credibility. |
| **Small class sizes (3–6)** | Clear differentiator vs. large language centres. |
| **Native teachers & custom materials** | Repeated in testimonials; worth featuring prominently. |
| **Wan Chai location** | Central, expat-friendly; “Tips in Hong Kong” page adds practical value. |

### Business & conversion

| Strength | Notes |
|----------|-------|
| **WhatsApp CTAs** | Branda (9215 2245) and Mini (6110 6966) — low-friction for HK users. |
| **Online enrollment form** | Exists on Group Classes page with course/timeslot selection. |
| **Flexible private tuition** | Home/office/school, hourly tiers, free consultation — well explained. |
| **Upcoming course dates** | Half-day, full-day, and evening options listed with July 2026 start dates. |
| **Office hours & map** | Clear Mon–Sat hours; static map image on homepage. |

### Technical foundations (partial)

| Item | Status |
|------|--------|
| HTTPS | HTTP and `www` redirect to `https://hkls.com.hk/` ✓ |
| CDN | Cloudflare ✓ |
| CMS | WordPress 6.8.5 (recent) ✓ |
| XML sitemap | Present at `/sitemap.xml` ✓ |
| RSS feed | Available ✓ |
| Robots.txt | Blocks `/wp-admin/`, login, PDFs, `/material-*` ✓ |

---

## Critical issues by area

### 1. SEO

#### Missing fundamentals (high priority)

| Issue | Current state | Impact |
|-------|---------------|--------|
| **Meta descriptions** | Not found on homepage, group classes, private tuition, contact, or testimonials | Google writes its own snippets; lower click-through from search |
| **Open Graph / social tags** | Not detected | Poor previews when shared on WhatsApp, LinkedIn, Facebook |
| **Canonical URLs** | Not detected | Risk of duplicate-content signals (multiple contact URLs, fragment pages) |
| **Homepage title** | Generic: `Hong Kong Language School` | Misses keywords like “Cantonese classes Hong Kong”, “learn Cantonese Wan Chai” |
| **Structured data** | Minimal (one VideoObject); no LocalBusiness, Course, or Organization schema | Lost rich results in Google (hours, location, ratings) |

#### Content & URL problems

| Issue | Example |
|-------|---------|
| **Testimonial URLs too long** | `/locals-really-appreciate-when-you-use-cantonese-and-you-can-have-a-better-understanding-of-the-culture/` |
| **“Test post” visible on testimonials** | Filter/category label `AllTest postTestimonials` looks unfinished |
| **Duplicate / fragment pages in sitemap** | `contact-us-2/`, `front-login/`, `front-testimonials/`, `sample-page/`, `front-logobar/`, etc. |
| **Sitemap vs robots conflict** | `robots.txt` disallows `/material-*` but dozens of material URLs remain in sitemap |
| **Legacy URL patterns** | Corporate page links to `index.php/hk/testimonials/94-client-list.html` |
| **Truncated homepage testimonial** | Sanjay Garla (2013) email cut off mid-sentence |

#### Keyword & positioning gap

- Homepage headline: **“Boost your career by learning Chinese”** — broad, Mandarin-leaning, not Cantonese-specific.
- You described HKLS as a **Cantonese school**; the site treats Mandarin and Cantonese equally everywhere.
- No dedicated landing pages for high-intent searches, e.g.:
  - “Cantonese course Hong Kong”
  - “Cantonese for expats”
  - “Cantonese evening class Wan Chai”
  - “Business Cantonese Hong Kong”

#### Recommended SEO changes

1. **Unique title + meta description** per page (60 / 155 char targets).
2. **LocalBusiness + EducationalOrganization JSON-LD** with address, phone, hours, geo.
3. **Course schema** on group/private pages (name, provider, schedule, price range if publishable).
4. **Clean sitemap** — remove template/fragment pages; align with robots rules.
5. **Short testimonial slugs** — e.g. `/testimonials/lauren-thiesse-cantonese-beginner/`.
6. **Cantonese-focused content hub** — blog/guides targeting expat search intent.
7. **Google Business Profile** alignment — ensure NAP (name, address, phone) matches site exactly.

---

### 2. UX & information architecture

#### Homepage overload

The homepage currently stacks:

- Welcome hero
- WhatsApp links
- Photo gallery (2009–2018-era filenames: “NYX”, “00293”)
- Animated GIF banner (449 KB)
- Multiple YouTube embeds (some duplicated)
- About paragraph
- Contact block + map
- Quick question form
- **Student login form**
- Testimonials (one stale 2013 story)
- Popups: Spring Sale, Terms, Payment Method, Aged 5–16 promo

**Problem:** A first-time visitor cannot quickly answer: *What do you offer? → Which course is for me? → When does it start? → How much? → How do I sign up?*

#### Navigation & page structure

| Page | Issue |
|------|-------|
| **Group Classes** | Schedule tables appear empty in main sections; upcoming courses only at bottom; no group-class pricing visible |
| **Private Tuition** | Good content; pricing table is clear |
| **Corporate Training** | Client list good; same pricing table duplicated from private tuition |
| **Aged 5–16** | Very thin — one paragraph + adult pricing table (likely wrong for kids) |
| **Contact Us** | URL says contact, but page content is **testimonials** (duplicate of `/testimonials/`) |
| **Login** | Full homepage sidebar (gallery, forms, testimonials) on login page — confusing |
| **Tips in Hong Kong** | Useful but buried; could support SEO if expanded |

#### Conversion friction

| Issue | Detail |
|-------|--------|
| **Long enrollment form** | Asks for HKID, nationality, occupation, home/office address upfront — high abandonment risk |
| **No group class pricing on site** | Forces WhatsApp/phone for basic question |
| **Popups** | “Our Spring Sale Has Started” with visible Popup Maker plugin boilerplate — looks unprofessional and may be outdated |
| **Terms & payment in modals** | Important info, but modal-on-load pattern is disruptive |
| **Student login on homepage** | Exposes internal portal to all visitors; username rule (“firstname + lastname”) is unclear |

#### Visual & brand

| Issue | Detail |
|-------|--------|
| Logo animation GIF | From 2017; dated aesthetic |
| Gallery images | Low resolution (250×250), cryptic titles |
| Layout | Table-based terms/conditions; inconsistent typography |
| Footer | “Copyright© 2017” — undermines trust |
| Fax number | Rarely used today; clutters contact block |

#### Mobile experience (inferred)

- Viewport allows `maximum-scale=4.0` — outdated pattern.
- 43 stylesheets + 64 scripts on homepage — likely slow on mobile networks.
- “Menu” toggle suggests non-standard nav; needs real-device testing.

---

### 3. Performance & technical debt

| Metric (homepage) | Value | Concern |
|-------------------|-------|---------|
| HTML size | ~100 KB | Heavy for a landing page |
| Stylesheets | 43 | Render-blocking |
| Scripts | 64 | Main-thread cost |
| Images | 16+ on homepage | Mix of old JPEGs and GIFs |

**Plugin footprint (visible):** Popup Maker, Buttonizer, Go Portfolio, XML Sitemap Feed, Virtual Robots.txt, and others — typical of an accreted WordPress site.

**Other technical notes:**

- IE6–8 conditional comments still in `<head>` (dead weight).
- Protocol-relative URLs (`//hkls.com.hk/...`) — minor, but prefer absolute HTTPS.
- No analytics tags detected in HTML source (may be injected elsewhere — verify in browser).
- Student area appears to use WordPress membership (`/members/`, `/account/`, `/password-reset/`).

---

### 4. Content strategy

#### What to keep

- Testimonials (especially 2022–2026) — migrate to a dedicated, filterable section.
- Corporate client logos/names — with permission, use logo strip.
- “Tips in Hong Kong” — expand into an expat resource hub.
- Course schedule blocks — make these the hero of Group Classes.

#### What to update or remove

| Content | Action |
|---------|--------|
| Sanjay 2013 truncated email on homepage | Replace with recent testimonial |
| Spring Sale popup | Remove or replace with current promotion |
| Photo gallery (old classroom shots) | Refresh with 2024–2026 photos |
| Copyright 2017 | Update to 2026 |
| Fax | Remove or move to footer fine print |
| “Test post” category | Delete or hide |
| Duplicate pages (`contact-us-2`, `sample-page`, front-* fragments) | Noindex or delete |

#### Missing content opportunities

- **About / Why HKLS** — teaching philosophy, teacher profiles.
- **Cantonese vs Mandarin** — help visitors choose (HKLS’s strength is Cantonese for HK life).
- **Group class fees** — even a “from $X” or sample package pricing.
- **FAQ** — typhoon policy, class size rules, payment, make-up lessons (terms exist but are buried).
- **Curriculum overview** — beginner → advanced pathway with sample topics.
- **Kids programme detail** — age groups, syllabus, pricing distinct from adults.

---

## Suggested site structure (modern IA)

```
Home
├── Learn Cantonese          ← primary funnel (NEW dedicated hub)
│   ├── Group Classes
│   ├── Private Tuition
│   ├── Corporate Training
│   └── Kids (5–16)
├── Courses & Schedules      ← unified calendar / upcoming starts
├── Pricing                  ← transparent tiers (or “from” pricing)
├── About / Teachers
├── Testimonials
├── Tips for Living in HK    ← SEO blog hub
├── Contact / Enroll
└── Student Portal (login)   ← separate, not on homepage
```

**Homepage should contain:**

1. Hero — Cantonese-focused value prop + primary CTA (WhatsApp / Book consultation).
2. Three paths — Group / Private / Corporate cards.
3. Next start dates — scannable schedule strip.
4. Social proof — 3 recent testimonials + link to all.
5. Location & hours — map + contact.
6. Single footer form or CTA — not three competing forms.

---

## Prioritized recommendation roadmap

### Phase 1 — Quick wins (1–2 weeks, WordPress)

- [ ] Add SEO plugin config: titles, meta descriptions, OG tags, canonicals.
- [ ] Add LocalBusiness + Organization schema.
- [ ] Remove/disable stale popups (Spring Sale).
- [ ] Fix Contact Us page content (currently shows testimonials).
- [ ] Update footer copyright year.
- [ ] Noindex fragment pages (`front-*`, `sample-page`, duplicate contacts).
- [ ] Replace homepage hero copy with Cantonese-forward messaging.
- [ ] Move student login off homepage to `/login/` only.
- [ ] Shorten enrollment form (collect essentials first; rest on follow-up).

### Phase 2 — UX refresh (2–6 weeks)

- [ ] New homepage layout (hero, course cards, schedule, testimonials).
- [ ] Refresh photography and gallery.
- [ ] Redesign Group Classes with visible schedules and pricing.
- [ ] Expand Kids page with age-appropriate content and pricing.
- [ ] Testimonials page with filters (Cantonese / Private / Corporate / Year).
- [ ] Sticky WhatsApp / “Book now” on mobile.
- [ ] Performance: consolidate CSS/JS, replace GIF banner with WebP/video, lazy-load embeds.

### Phase 3 — Growth & SEO (ongoing)

- [ ] Cantonese keyword landing pages.
- [ ] Expand “Tips in Hong Kong” into monthly articles.
- [ ] Google Business Profile optimization + review funnel.
- [ ] Analytics (GA4) + conversion tracking (form submit, WhatsApp click).
- [ ] Consider hreflang if adding Traditional Chinese site version.

### Phase 4 — Platform decision (optional, larger scope)

| Option | Pros | Cons |
|--------|------|------|
| **A. WordPress theme rebuild** | Keeps existing CMS, forms, student portal; lower migration risk | Still plugin-heavy if not carefully rebuilt |
| **B. Headless / modern frontend** (Next.js + WP API) | Best performance & UX; strong SEO control | Higher cost; student portal integration work |
| **C. Full replatform** | Cleanest long-term | Most expensive; content + enrollment migration |

---

## Decisions needed from you

Before design or development starts, please clarify:

### 1. Brand positioning

> **Should the site lead with Cantonese only, or keep Mandarin + Cantonese equally?**

The live site treats both equally; your brief emphasizes Cantonese. This affects homepage copy, SEO keywords, and navigation labels.

### 2. Primary audience

> **Who is the #1 target visitor?**

- Expat professionals in HK  
- Corporate HR / L&D buyers  
- Parents (kids 5–16)  
- Overseas Chinese / returnees  
- All equally  

This determines hero message, imagery, and CTA priority.

### 3. Pricing transparency

> **Are you willing to publish group class fees on the website?**

Private/corporate hourly rates are already public. Group pricing is not — forcing WhatsApp may reduce tire-kickers but also reduces qualified leads from search.

### 4. Enrollment flow

> **Preferred conversion path:**

- A) WhatsApp-first (current lean)  
- B) Online form → staff follow-up (current form, simplified)  
- C) Self-serve booking/payment (larger build)

### 5. Student portal

> **Keep the WordPress student login on the public site, or move to a separate subdomain/app?**

Login on the homepage confuses prospective students and adds clutter.

### 6. Platform & budget

> **Refresh existing WordPress, or rebuild?**

The `demo-hkls` repo is currently empty — suggest confirming whether this repo will hold the new site code.

### 7. Language of site

> **English only, or add Traditional Chinese (繁體) version?**

Important for local SEO and parent audience; doubles content maintenance.

### 8. Popups & promotions

> **Any active promotions that should replace “Spring Sale”?**

If none, recommend removing auto-opening popups entirely.

---

## Competitive UX patterns to adopt (2026 language school sites)

- **Clear course finder** — “I’m a beginner / I know some Cantonese / I need business Cantonese.”
- **Schedule at a glance** — calendar or card list with “Enroll” per cohort.
- **Teacher credibility** — photos, credentials, “native Hong Kong speaker.”
- **Trust bar** — Google rating, years in operation, student count, corporate logos.
- **One primary CTA colour** — WhatsApp green or brand accent, repeated consistently.
- **Fast mobile load** — target LCP under 2.5s; hero image WebP, no autoplay GIF.

---

## Appendix: pages inventoried

| URL | Role | Notes |
|-----|------|-------|
| `/` | Homepage | Overloaded single-page feel |
| `/group-classes/` | Group courses + enrollment | Schedules at bottom; empty table placeholders |
| `/private-tuition/` | 1:1 / small group private | Strong content |
| `/corporate-training/` | B2B | Good client list |
| `/aged-5-16/` | Kids | Thin content |
| `/testimonials/` | Social proof | Good posts; “Test post” label |
| `/tips-in-hong-kong/` | Expat tips | SEO opportunity |
| `/contact-us/` | Contact | **Content mismatch — shows testimonials** |
| `/login/` | Student portal | Buried in homepage clutter |
| `/photo-gallery/`, `/video-gallery/` | Media | Dated assets |
| `/learning-resources/` | Materials | Likely student-facing |
| Material pages (`/material-*`) | Course PDFs/resources | Blocked in robots; should be excluded from sitemap |

---

## Next step

Once you answer the **Decisions needed** section (even briefly), a follow-up document can define:

- Wireframes for homepage + Group Classes  
- Exact page titles and meta descriptions  
- Cantonese-first messaging copy  
- Implementation plan aligned to WordPress refresh vs. full rebuild  

---

*Audit performed via live site review, HTML/sitemap/robots analysis, and page-by-page content inspection of [hkls.com.hk](https://hkls.com.hk/).*

---

## Demo MVP (July 2026)

A static sales-pitch demo has been built in this repo:

- **`index.html`** + **`css/styles.css`** — pure HTML/CSS, no JS
- Expat-focused Cantonese positioning, English-only copy
- WhatsApp / phone enrollment only — no forms, login, or popups
- Open `index.html` in a browser to preview

See `README.md` for local preview instructions.
