# MAFNR — Complete public website (Square Country)

This is a **multi-page, responsive, static demonstration website** for the Ministry of Agriculture, Fisheries and Natural Resources.

## Getting started

1. Unzip the package.
2. Double-click `index.html` to browse, or run `python3 -m http.server 8000` in this folder and open `http://localhost:8000/`.
3. To publish, place all files in a GitHub Pages repository, keeping `assets/`, `downloads/` and `images/` beside the HTML files. Use `index.html` as the homepage.

The website **does not contain a login page**, as requested. The existing navigation link is `login.html`. If you already have one, add your file at the project root without replacing it. If you don't, that one link will not resolve until your own login page is supplied.

## Original images

If you have the images from your original code, copy these into `images/`:
- `mafnr-logo.png` — ministry header logo
- `pm-copy.png` — homepage hero photograph

The website includes its own local SVG fallback images, so neither is required for layout testing.

## Included content and tools

- Homepage and complete navigation across Agriculture, Fisheries, Natural Resources, Services and News & resources.
- Register an agricultural holding: dedicated first-time registration guide and 4-stage local draft form (holder, land, activities, declaration), save/restore/JSON export.
- All 8 dedicated licence/permit information pages.
- 4-step local application draft wizard, save/reopen/delete drafts, JSON export and print summary.
- Personal catch log with local saving, individual/all deletion and CSV export.
- Search across the site, service filters, permit filters, news filters, publication filters, FAQs and event filtering.
- 6 sample articles, 7 printable publications, 3 sample consultations and sample notices/events.
- Contact, feedback and concern report composition with copy and `mailto:` options.
- Public information, careers, policies, emergency information, service standards, privacy, cookies, accessibility, terms, site map and custom 404 page.
- 5 downloadable blank CSV record templates.

## IMPORTANT: Production limitations and setup

This is a **static prototype**. Its news articles, events, notices, consultations, policies, programmes and contacts are illustrative. It is *not* connected to a ministry database or regulatory workflow.

**Applications are not submitted, fees aren't charged, and licences aren't issued.** Browser localStorage is used for draft applications and catch logs, so those records remain on the same device/browser and are not transmitted. Contact/feedback/report forms prepare a message locally, and may open the user's own email client. No mail is sent by the site.

Before public or official deployment:
1. Edit `assets/data.js`, including `contactEmail`, `address` and `phone`, and replace demonstration text with approved information.
2. Verify all legal rules, permits, fees, timeframes, public notices and programme status with official sources.
3. Connect official forms to a secure, authorised backend before enabling submission. Add authentication, privacy, records handling, accessibility and security assessments as required.
4. Upload the original logo/hero photos to `images/` and verify their use rights.
5. Add your separately maintained `login.html` (not included here).
6. If deploying to a case-sensitive host, preserve filenames as provided.

## Editing the design

- `assets/site.css` — all visual styling and responsive layouts.
- `assets/site.js` — page rendering, navigation, search, filters and interactive functions.
- `assets/data.js` — topics, guide content, permits, news, publications, FAQs and consultations.

## Special page URLs

The article and printable document detail pages use query strings:
- `article.html?id=new-service-portal`
- `publication.html?doc=farm-planning`
- `consultation.html?id=service-access`
- `application.html?service=commercial-fishing`

All HTML pages are actual files, so they work on plain static hosting without rewrites.


## Sprout — website chatbot assistant

Sprout is included on all public HTML pages (not the excluded login page). It opens from the bottom-right corner, answers common agriculture/fisheries/ministry questions, links to relevant pages and provides **MAFNR number recovery guidance**. Sprout is rule-based and works without a server, AI subscription or API key. It cannot search real account records, validate identities or recover a private number. The number-recovery wording is illustrative; configure your organisation’s actual recovery procedure and verified contact details before publishing. See `assets/sprout.js` and `assets/sprout.css` to edit it. It does not store messages or send them to a server.

## Agricultural holding registration

Open `register-holding.html` from Agriculture, Services, homepage or Sprout. This is the first registration path for a new holding, not an agricultural activity permit. Drafts are saved only to browser localStorage (`mafnr-holding-registration-draft-v1`), and can be downloaded as JSON. No real applications are lodged and no MAFNR number is issued. A secure server, approved government validation, and account workflow are required before accepting real personal details or issuing references.
