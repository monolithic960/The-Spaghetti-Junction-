# The Spaghetti Junction — one-page site

Static site for The Spaghetti Junction, 4510 Charlestown Rd, New Albany, IN. No build step, no dependencies — deploy anywhere that serves HTML (`netlify.toml` included, publish dir = root).

**`index.html`** — the finished site. Fast & Loud direction: brand-true red/green/yellow, Anton/Lilita display type, dense photo menu, catering mega-section. The style switcher and the alternate "Warm Classic" design have been removed; the classic design is recoverable from git commit `21f3c4d` (`classic.html`) if ever needed.

## Deploy

- **GitHub Pages:** Settings → Pages → deploy from `main` / root. Done.
- **Netlify:** drag the folder in, or connect the repo. No build command, publish dir = root.
- Point `italianfoodnewalbany.com` at it when ready (currently on Hibu — DNS swap, ~5 min).

## What's in here

- Loud, dense, fast-food-style one-pager in the brand's real colors (logo red/green/yellow): marquee bar → hero (real spaghetti photo) → Sunday AYCE deal band → order-your-way → full HTML menu with photos woven in → catering mega-section → gallery → loyalty QR + review CTA → about → 6 real reviews → map/hours → hiring strip → footer
- `Restaurant` JSON-LD schema (address, hours, rating, images, sameAs) — the old site has none
- Open-now badge (JS, Indiana time, fails safe to static hours text)
- Sticky mobile bar: Call / Directions / Order
- One primary CTA throughout: **Order Online** (Toast)
- `images/` — all content images pulled from the current Hibu/Yext CDNs (logo, food shots, catering spread, loyalty QR, DoorDash logo) so nothing breaks when Hibu is cancelled. The heavy Yext PNGs were recompressed to JPEG (1.3–2.8 MB → 78–218 KB each); total image weight is now ~1 MB.

## Confirm with the owner before launch

1. **Hours** — site says Mon–Thu 11–8:30, Fri–Sat 11–9, Sun 11–8:30. Google Business Profile shows different closing times. Whichever is true, fix the other (and Yelp/Tripadvisor).
2. **Sunday all-you-can-eat** — confirm it still runs and what's included. Price intentionally not shown.
3. **Menu prices** — intentionally omitted. Export from Toast at launch and drop into each `.item` (add a `<span class="mono">` after the `h4`).
4. **Menu items** — list is built from confirmed dishes only (reviews + their categories). Owner should add/remove.
5. **Suite number** — Toast/Tripadvisor say "Ste 200"; their site and most citations omit it. Match whatever Google Business Profile says, everywhere.
6. **Review link** — currently the Hibu survey (owner-provided). Strong recommendation: swap to the Google review link (`g.page/r/...`) so reviews build the 4.2 public rating instead of a private widget.
7. **Second phone** — (812) 944-5400 appears on some listings. Retire it or label it; one number everywhere.
8. **Photography** — biggest remaining upgrade. Half-day shoot, 4 shots: baked spaghetti hero, the room, the family, garlic bread. Drop the hero shot in place of the SVG art.

## Links wired

| Action | URL |
|---|---|
| Order Online | order.toasttab.com/online/the-spaghetti-junction-4510-charlestown-rd-ste-200 |
| Catering | toasttab.com/catering/the-spaghetti-junction-4510-charlestown-rd-ste-200 |
| DoorDash | doordash.com/store/the-spaghetti-shop-new-albany-536625 |
| Review | hibu.us/merchants/64147/take_survey?response_set_code=lq-3Mer8sw |
| Facebook | facebook.com/thespaghettijunction.net |
| Jobs | mrcharlestonstationinc.easyapply.co |

Site by Monolith Systems.
