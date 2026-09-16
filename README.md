# The Living Field — site starter

This is a static, no-build-step website: plain HTML/CSS/JS, no framework, no server required to run it. Open `index.html` in a browser and it works as-is.

## What's built

- **Home** (`index.html`) — hero, mission, teasers for Electroculture/Water Energetics/Radionics, Our Shared Mission, and an Alchemical Formulations section introducing The Collections (Cultivate Elevate, Elemental Wizdom, Sacred Heart Plant Essences) — see "0. Image sources" and "7. The Body section" below
- **Education hub** (`education/`) — hub page + one full sample guide (`education/guides/electroculture-antenna-basics.html`)
- **Shop** (`shop/`) — hub page with Electroculture equipment, Training, Water Energetics and Radionics categories: one sample electroculture product (`shop/electroculture/cw-antenna.html`), one sample training course + bundle (`shop/training/antenna-installation-course.html`), one Water Energetics product (`shop/water-energetics/cloud-sea-aqua-inductor.html`), and two Radionics products (`shop/radionics/heaven-earth-broadcaster.html`, `shop/radionics/murmuration-transmitter.html`)
- **For the Body** (`body/`) — new wellness/supplement vertical, see "7. The Body section" below
- **FAQ** (`faq/`) — accordion FAQ with schema markup
- **Contact** (`contact/`) — contact form, wired to Netlify Forms (see below)
- **Legal** (`legal/terms.html`, `legal/privacy.html`) — starter templates only, **must be reviewed by a solicitor before launch**
- Shared design system in `assets/css/style.css`, shared behaviour in `assets/js/main.js`
- `robots.txt` and `sitemap.xml` for search engines

## Before you launch — a checklist

### 0. Image sources — replace before launch
Several real images are already wired in as a look-and-feel demo, sourced from Fertile Current (used here under the partnership, not by default license):
- `assets/img/cw1-antenna-demo.jpg` — used on the CW1 product page and the homepage Electroculture card
- `assets/img/rainbow-field-hero.jpg` — the plain rainbow/field photo, used on the homepage hero
- `assets/img/rainbow-field-hero-antenna.jpg` — same photo with an antenna cutout composited in artistically (not currently used, kept in case it's wanted again)
- `assets/img/cloud-sea-aqua-inductor.jpg` — Fertile Current's "Cloud Sea Aqua Inductor" product photo, used on the homepage Water Energetics card
- `assets/img/murmuration-radionics.jpg` — Fertile Current's "Murmuration" radionics transceiver kit photo, used on the homepage Radionics card

These were captured via browser screenshot rather than the original source files, so resolution is capped around 1500-2000px — fine for preview, soft if stretched much larger on a big monitor. Before real launch, replace all of these with either genuine high-resolution files from Fertile Current (ask for the originals rather than reusing these compressed versions), your own photography of your own products, or — since Water Energetics and Radionics aren't yet real product lines on The Living Field — swap in photography of whatever you end up actually stocking under those two categories.

Four more were sourced the same way, from Master Your Greatness Academy (also used under a confirmed partner/reuse arrangement) — these replaced an earlier, lower-resolution pair of screenshots and are the current live images on both product pages:
- `assets/img/shilajit-tablets-master.jpg` — MYGA's "Cultivate Elevate" shilajit tablets box (hero shot), used on the Shilajit Tablets product page
- `assets/img/shilajit-lifestyle-master.jpg` — MYGA's shilajit box-and-tablets lifestyle shot, used further down the same page
- `assets/img/lions-mane-capsules-master.jpg` — MYGA's "Cultivate Elevate" Lions Mane capsules packet (hero shot), used on the Lions Mane Mushroom Capsules product page
- `assets/img/lions-mane-lifestyle-master.jpg` — MYGA's packet-and-capsules lifestyle shot, used further down the same page

Same caveats apply: screenshot-resolution only, replace with genuine high-res files or your own product photography before real launch, and confirm reuse terms directly with MYGA before this goes into a fully public storefront (see note in section 7 below on the private-membership framing MYGA itself uses for these claims).

Three more were sourced for the homepage's "Alchemical Formulations" / "The Collections" section. Unlike most images in this list, these came from MYGA's actual source files rather than a page screenshot — `cultivate-elevate-logo.png` and `elemental-wizdom-logo.png` are their own hosted PNG logo files (background keyed out to transparent so they sit cleanly on the card instead of showing a mismatched box), and `myga-emblem.png` is cropped from MYGA's own site logo, which is served as an SVG (vector), so it stayed crisp even scaled up:
- `assets/img/cultivate-elevate-logo.png` — MYGA's "cultivate ELEVATE" wordmark, used on the homepage Cultivate Elevate card (links to `body/`, since that's where the two live Cultivate Elevate protocols — Shilajit, Lions Mane — actually are)
- `assets/img/elemental-wizdom-logo.png` — MYGA's "Elemental Wizdom" emblem and wordmark, used on the homepage Elemental Wizdom card (marked "Coming soon," links to `contact/` — this is a real MYGA collection but has no Living Field products yet)
- `assets/img/myga-emblem.png` — just the triangle emblem cropped from MYGA's own site logo (not a full MYGA logo, and not a MYGA collection at all), used on the homepage "Sacred Heart Plant Essences" card by explicit request. Worth flagging: **Sacred Heart Plant Essences is not an actual MYGA collection** — MYGA's real four collections are Cultivate Elevate, Elemental Wizdom, The Fertile Current and Law of the Luminaries (confirmed directly on their site and via their own site search). The name and card copy here were supplied directly rather than sourced, so there's nothing to fact-check against MYGA for this one — treat it as an original Living Field placeholder ("Coming soon," links to `contact/`) until a real plant-essence line and matching mark exist.

All three display via a `.scroll-card-logo` tile (`assets/css/style.css`) — the `<img>` is pulled out of normal flow (`position:absolute; inset:0`) with `object-fit:contain` so it can never stretch the tile's own square shape, and scales evenly to fill the available space regardless of its native aspect ratio. (Earlier drafts of this tile let the image sit in normal flow, which let a tall/portrait logo push its own box taller than its neighbours — worth knowing if a future logo swap ever brings back a "boxes are different sizes" symptom.)

One more image sits above the two "Alchemical Formulations" paragraphs: `assets/img/five-elements.png`, a five-classical-elements (Earth/Fire/Air/Water/Aether) graphic supplied directly by the client rather than sourced from MYGA — it breaks up what was previously two text blocks stacked directly on top of each other, in the same dark-plate style as the rest of the alchemical framing.

Four more were sourced from Fertile Current for the new Water Energetics and Radionics product pages (real products, real pages — not placeholders like the homepage cards above):
- `assets/img/cloud-sea-hero.jpg` and `assets/img/cloud-sea-lifestyle.jpg` — Cloud Sea Aqua Inductor product and in-use shots, used on `shop/water-energetics/cloud-sea-aqua-inductor.html`
- `assets/img/patterns-broadcaster.jpg` — Heaven &amp; Earth "Patterns" Soil Broadcaster, used on `shop/radionics/heaven-earth-broadcaster.html`
- `assets/img/murmuration-transmitter.jpg` — Murmuration Divine Order Transmitter, used on `shop/radionics/murmuration-transmitter.html` (distinct from `murmuration-radionics.jpg`, the placeholder used on the homepage scroller/dark-section cards)

These were captured at their original Squarespace CDN resolution (~750px on the short side) rather than a compressed screenshot, so they're closer to launch-ready than the homepage placeholders, but confirm with Fertile Current whether higher-resolution originals are available before printing or using them much larger than shown here. Copy on both new pages is adapted from `thefertilecurrent.com/waterenergetics` and `thefertilecurrent.com/radionics` under the same partner arrangement — lightly edited for Living Field voice and given placeholder £ pricing (numeric values carried over from the source $ prices, not verified UK retail conversions).

### 1. Photography
Every other hero and tile still shows a small "PLACEHOLDER" label describing the photo it needs (e.g. *"hands installing a ground wire around a raised garden bed"*). Search each HTML file for `data-ph=` to find every placeholder and its brief. To swap one in:

```html
<!-- before -->
<section class="hero grad-1" data-ph="wide shot, copper antenna...">

<!-- after -->
<section class="hero" style="background-image:url('assets/img/hero-antenna.jpg');">
```

Removing `data-ph` makes the label disappear automatically; removing the `grad-*` class removes the placeholder gradient.

### 2. Stripe checkout
This site uses **Stripe Payment Links** rather than a custom checkout, so no backend or secret API key is needed:

1. In the Stripe Dashboard, go to **Payment links → New**.
2. Create one link per product/course/bundle, matching the prices already shown on the page (CW1 Antenna £249, Course £45, Bundle £269, etc).
3. Copy the generated `https://buy.stripe.com/...` URL.
4. Find the matching `<!-- STRIPE CHECKOUT -->` comment in the HTML (in `shop/electroculture/cw-antenna.html` and `shop/training/antenna-installation-course.html`) and replace the placeholder `href`.

As you add real products, duplicate the product/course page pattern and repeat.

### 3. Contact form
The contact form (`contact/index.html`) and the homepage newsletter signup are both wired to **Netlify Forms** already (`data-netlify="true"` + a honeypot field) — this works automatically with zero extra code as long as the site is hosted on Netlify, and submissions appear under Site settings → Forms in the Netlify dashboard. Both forms redirect to `/thank-you/` on success. No further setup needed unless you move off Netlify, in which case swap in Formspree or a small serverless function instead.

### 3b. Training videos
`shop/training/antenna-installation-course.html` has a `.video-embed` block wired up with a standard responsive YouTube embed — search for `VIDEO_ID` and swap in your real YouTube video ID once it's uploaded. Unlisted YouTube videos work well for paid content (not searchable, but anyone with the link can view) — the same `.video-embed` markup can be copied onto any page for additional modules/lessons.

### 4. Company details
Search for `XXXXXXXX` and `[address]` across the site (footer on every page, plus `legal/terms.html` and `legal/privacy.html`) and replace with Darklight Design Ltd's real company number, registered office, and VAT number if applicable. This is a UK legal requirement (trading disclosure rules) when trading under a name other than your registered company name — keeping it in the footer only, as discussed, is the standard compliant approach.

### 5. Domain & hosting
The site is written with `https://www.thelivingfield.co.uk/` as the canonical domain throughout (meta tags, sitemap, schema). If you host at a different URL or add the `.eu` version later, do a find-and-replace across all HTML files and `sitemap.xml`.

Any static host works well here (Netlify, Cloudflare Pages, Vercel, or traditional hosting) since there's no build step — just upload the folder as-is.

### 6. SEO follow-ups after launch
- Submit `sitemap.xml` to Google Search Console and Bing Webmaster Tools
- Add a real `assets/img/og-cover.jpg` (1200×630px) for social share previews — referenced in the homepage's Open Graph tags
- Fill in the empty `sameAs` array in the homepage's Organization schema with real social profile URLs once set up
- As real content/products replace the "coming soon" cards in `education/index.html` and `shop/index.html`, give each its own page following the existing article/product pattern (full meta tags + schema) rather than adding them as plain list items

### 7. The Body section
`body/` is a new second product vertical — "protocols for the body's field" (traditional wellness supplements: shilajit, Lions Mane, and more to come), separate from the original soil/electroculture side of the site. It currently has:
- `body/index.html` — hub page, with two flagship products live and several more listed as "Coming soon"
- `body/protocols/shilajit-tablets.html` ("Shilajit Tablets") and `body/protocols/lions-mane-capsules.html` ("Lions Mane Mushroom Capsules") — full product-style pages

Important things to know before treating this as a normal launch-ready section:
- **Copy and images are taken directly from Master Your Greatness Academy (MYGA), not rewritten.** Both pages' hero copy, protocol descriptions, "Included with this protocol" contents and hero/lifestyle images are copied as-is from MYGA's live "Cultivate Elevate" product pages (masteryourgreatnessacademy.org/natural-living/), by explicit decision — this is a deliberate change from the site's usual approach of rewriting sourced copy into Living Field voice, scoped only to these two live product pages (not the hub page's "Coming soon" placeholders, which remain original). One deliberate edit was made to MYGA's own copy: their "Included with this protocol" line for Lions Mane lists "1 x Lions Mane Extract Powder (100g)," which doesn't match the pictured product (a 120-capsule packet) — this was corrected to "1 x Lions Mane Mushroom Capsules (120 capsules)" rather than propagated as an inconsistency. Confirm reuse terms directly with MYGA before this goes into a fully public storefront (see the framing note below).
- **No pricing or checkout yet.** These are deliberately built as an "open storefront" — informational pages with a "Get in touch" CTA instead of a price or Stripe link, since there's no confirmed sourcing/supplier in place yet. Follow the same Stripe Payment Link pattern from section 2 once that's sorted.
- **No medical/health claims.** Both pages carry a "What we don't claim" section explicitly framing the content as historical/traditional use, not medicinal claims, with a doctor-consultation caveat. This matters because the UK's Advertising Standards Authority (general claims) and the MHRA (anything sounding like a medicinal claim) both regulate supplement marketing — keep any future copy on this section in the same register, and have it reviewed alongside the rest of the legal pages before real launch.
- **MYGA's own framing is different from ours.** The source material on Master Your Greatness Academy is published as a "private membership association" (price-gated behind login), which lets them frame health-related copy as private member-to-member education rather than public advertising. The Living Field's Body section is fully public, so it does not carry that same legal framing — this was a deliberate choice, but worth remembering, and doubly relevant now that the copy itself is a direct copy rather than a rewrite — have this reviewed alongside the legal pages before real launch.
- **Not currently in the "live" trimmed deploy.** Like `shop/`, this section is excluded from the shop-free base site published while the rest of the site is rebuilt (see the deploy notes for `thelivingfield-live/` if you're working from that folder) — it only appears in the full master copy for now.
- Currently live/flagship: Shilajit, Lions Mane. Still "Coming soon": Tremella, Dragon's Blood, a chai-style tonic blend, a placeholder "Vital Force Tonic," and others named on the hub page — these remain original Living Field copy, not MYGA-sourced, until/unless a similar direct-copy decision is made for each.
- **Branding:** this vertical is presented as its own named division under the main brand — "The Living Field — Body" — shown in the eyebrow label on the hub hero and the breadcrumb on every product page, while the equipment/education side stays simply "The Living Field" as the primary brand. Electroculture remains the flagship; Body is deliberately the secondary, clearly-labelled offshoot. The homepage no longer has its own dedicated Body teaser section (removed along with the Robert Fludd engraving image) — the only homepage mention is the brief line in "Our Shared Mission" pointing to the range; the hub page (`body/`) is reachable via the nav Body link and that mission-section context alone.
- **Planned additions (not yet built):** medical qigong training and other "electric body" content are earmarked for this section down the line — worth keeping the hub page's structure (category blocks of cards) in mind as a template when that's ready to build.

## Structure

```
index.html
education/
  index.html
  guides/electroculture-antenna-basics.html
shop/
  index.html
  electroculture/cw-antenna.html
  water-energetics/cloud-sea-aqua-inductor.html
  radionics/
    heaven-earth-broadcaster.html
    murmuration-transmitter.html
  training/
    index.html
    antenna-installation-course.html
body/
  index.html
  protocols/
    shilajit-tablets.html
    lions-mane-capsules.html
faq/index.html
contact/index.html
thank-you/index.html
legal/terms.html
legal/privacy.html
assets/css/style.css
assets/js/main.js
robots.txt
sitemap.xml
```
