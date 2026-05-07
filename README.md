# topcalltrackingsoftware.com

Site 1 of the call-tracking review network. Static HTML/CSS/JS, deployed via GitHub Pages.

## Build details

- **Template:** T1 Editorial Clean (Wirecutter feel)
- **Accent color:** Brick `#C8553D`
- **Background:** Off-white `#FAF8F5`
- **Fonts:** Inter Tight (display) + Inter (body)
- **Heading scale:** Large variant (H1 = 60px)
- **Body size:** 17px
- **Border-radius:** 4px
- **Card style:** outlined

## Byline approach

Currently using the **editorial-team byline** (`The TopCallTrackingSoftware Editorial Team`) per section 1.4 option 2 of the master plan. Swap to a real named author when one is hired.

## Pages (12 total)

- `index.html` — Homepage / 2026 buyer's guide
- `about.html`
- `contact.html`
- `methodology.html`
- `faq.html`
- `reviews/callscaler.html`
- `reviews/callrail.html`
- `reviews/calltrackingmetrics.html`
- `reviews/whatconverts.html`
- `reviews/invoca.html`
- `privacy-policy.html`
- `terms.html`

## CTA destination

All CallScaler CTAs link to `https://callscaler.com/?ref=topcalltrackingsoftware`. Update the `ref` value before deploying if you change the tracking convention.

## Deploy to GitHub Pages

```bash
cd sites/topcalltrackingsoftware
git init
git add .
git commit -m "Initial site"
gh repo create topcalltrackingsoftware --public --source=. --push
gh api -X PATCH /repos/<your-account>/topcalltrackingsoftware/pages -f source.branch=main -f source.path=/
```

Then in your registrar, point `topcalltrackingsoftware.com` apex DNS to GitHub Pages IPs:
- 185.199.108.153
- 185.199.109.153
- 185.199.110.153
- 185.199.111.153

And set a CNAME record for `www` → `<your-account>.github.io`.

## TODOs before going live

- [ ] Replace editorial-team byline with real author if/when hired
- [ ] Take or commission real screenshots for review pages (currently text-only)
- [ ] Generate Open Graph cover images (`/assets/img/og-cover.jpg`, `/assets/img/og-callscaler.jpg`, etc.)
- [ ] Verify schema with Google's Rich Results Test
- [ ] Fill in real LLC name in disclosure block (currently generic)
- [ ] Confirm CallScaler pricing tiers ($49 / $99 / $199) match actual product
- [ ] Set up real `editors@topcalltrackingsoftware.com` email forwarding
