# D/Quarters — Static HTML Site (No Server Required)

This package contains the full D/Quarters website as **standalone HTML files**.
Each page is a self-contained `.html` file that opens directly in any modern
web browser from your computer — no Node, no server, no installation.

## How to use

1. **Unzip** this folder anywhere on your computer
2. **Double-click `index.html`** (or right-click → Open With → your browser)
3. Navigate between pages using the normal site links — they all work via `file://`

Tested on Chrome, Edge, Safari and Firefox.

## Pages included (21 files)

| URL                                | File                                              |
|------------------------------------|---------------------------------------------------|
| Homepage                           | `index.html`                                      |
| About                              | `about.html`                                      |
| Office Quarters                    | `office-quarters.html`                            |
| Desk Quarters                      | `desk-quarters.html`                              |
| Open Quarters                      | `open-quarters.html`                              |
| Locations overview                 | `locations.html`                                  |
| Dubai Media City — Building 8      | `locations/dubai-media-city-8.html`               |
| Dubai Media City — Building 12     | `locations/dubai-media-city-12.html`              |
| Dubai Science Park                 | `locations/dubai-science-park.html`               |
| Dubai Design District              | `locations/dubai-design-district.html`            |
| Facilities                         | `facilities.html`                                 |
| Community                          | `community.html`                                  |
| Insights (blog list)               | `insights.html`                                   |
| 6× blog articles                   | `insights/<slug>.html`                            |
| Contact                            | `contact.html`                                    |
| FAQs                               | `faq.html`                                        |

## Folder structure

```
dquarters-static-html/
├── index.html                ← start here
├── about.html
├── office-quarters.html
├── desk-quarters.html
├── open-quarters.html
├── locations.html
├── facilities.html
├── community.html
├── insights.html
├── contact.html
├── faq.html
├── locations/
│   ├── dubai-media-city-8.html
│   ├── dubai-media-city-12.html
│   ├── dubai-science-park.html
│   └── dubai-design-district.html
├── insights/
│   └── (6 blog post HTML files)
├── brand/
│   ├── logo-mark.png         ← DQ monogram
│   └── logo-wordmark.png     ← horizontal logo
└── static/
    ├── css/main.7f6c3084.css ← all styles (~65 KB)
    └── js/                    ← optional bundle (not used by static pages)
```

## What works out of the box

✅ All page styles, typography, brand colors (mint/teal + plum-charcoal)  
✅ All page-to-page navigation  
✅ All imagery (hero photos, location galleries, blog cards, testimonials)  
✅ Mobile responsive layouts  
✅ Sticky navigation with scroll state  
✅ FAQ accordions (vanilla-JS replacement)  
✅ Mobile menu toggle  
✅ Back-to-top button  
✅ Inquiry forms (visual — submit shows "Thank you" but does not send data)  
✅ Embedded Google Maps on location pages  
✅ Google Fonts (Almarai, Open Sans, Playfair Display) loaded over HTTPS  

## What's intentionally limited

⚠️ **Form submissions** — the inquiry form on Contact / Workspace pages updates the
button to "THANK YOU" but does not send data anywhere. To capture leads you'll need
to wire the form to a backend (Netlify Forms, Formspree, your own API, etc).

⚠️ **Workspaces dropdown** — the React mega-dropdown is replaced with simpler
navigation; the three workspace pages are still reachable from the Home page and
the mobile menu.

⚠️ **Carousels / animations** — entrance fade-ups still run via CSS keyframes;
scroll-linked motion is reduced.

## Customising

To change copy, swap brand colors, or replace imagery, edit the corresponding
HTML file in a text editor. All text content lives inline in each file. Brand
colors are in `static/css/main.7f6c3084.css` — search for:
- `#6dbdab` — mint/teal primary accent
- `#2b2425` — deep plum-charcoal dark surface

## Brand tokens

| Token       | Value     | Usage                                    |
|-------------|-----------|------------------------------------------|
| Accent      | `#6dbdab` | CTAs, links, overlines, accent type      |
| Dark        | `#2b2425` | Footer, TECOM section, hero overlay      |
| Background  | `#f7f7f7` | Page background                          |
| Surface     | `#ececec` | Alternate sections                       |
| Body text   | `#131313` | Headings, body copy                      |
| Muted text  | `#747474` | Captions, metadata                       |
| Border      | `#d2d2d2` | Card borders, dividers                   |

**Fonts:** Almarai (headings), Open Sans (body), Playfair Display (accent serif).
All loaded from Google Fonts CDN.

---

Built for D/Quarters · A TECOM Group brand · Dubai
