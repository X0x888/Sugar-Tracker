# Sugar Tracker — release notes

What changed in each release, in the same words the extension shows you
in its update banner.

This is the user-facing summary. It is generated from the extension’s own
release copy — run `npm run build:release-notes` to refresh it.

## 1.17.0

**Polish & UX**

Every supported grocer now says "Pick a store" instead of "Sugar Tracker may need updating" when first-visit listings need a postcode. Offline banner now reassures that cached badges keep working and flashes "Reconnected" when you come back online. Cleaner popup hierarchy: hero card lifts, settings rows flatten, footer links read as actions, nutrient chips no longer share colours.

## 1.16.1

**New features**

Big update since v1.1: Iceland is back as the eighth supported grocer, Health Modes let you pick the threshold preset that matches how you shop, and the popup shows a per-product distribution plot with colour-blind-safe themes. Co-op now says "Pick a store" when no postcode is set, and tried-and-failed badges read distinctly from still-loading ones.

## 1.16.0

**Polish & UX**

Co-op now says "Pick a store" when products won't load because no postcode is set, instead of looking like a defect. Badges that already tried and failed now read distinctly from badges still waiting to load — the dashed-circle X reads as 'tried, no luck' at a glance. And the auto-update banner now actually shows what changed for releases 1.10–1.16.

## 1.15.0

**New features**

Iceland (chain) is back as the eighth supported grocer — nutrition is read from Iceland's own product data, so atomic-CSS class hashes can't break it again. Tesco listings stop needing a refresh to show badges, Sainsbury's badges sit over the image again, Co-op badges no longer leak onto hero pictures, and Ocado's lazy-loading tiles re-attach reliably during fast-flick scroll.

## 1.14.0

**New features**

Health Modes — pick the threshold preset that matches how you shop. FSA Default stays the default; Reduced-Sodium ships free for shoppers actively cutting salt. Reduced-Sugar and Reduced-Saturates are in early access. Every numeric is sourced verbatim from a published, legally-binding instrument.

## 1.13.2

**Polish & UX**

Listing-page reliability pass on the v1.13.1 CSP fix — three residual sources of stranded `?` overlays closed (cross-origin link guards, fetch-context cooldown surfacing, no-URL attribution) so a `?` badge tells you what actually failed.

## 1.13.1

**Bug fixes**

CSP `connect-src` directive now lists every grocer host the service worker fetches from. A regression in v1.13.0 had silently blocked all background fetches with "Failed to fetch" across every supported grocer.

## 1.13.0

**Audit pass**

Live-DOM audit pass against all 7 grocers — selectors refreshed where retailers had renamed data-test → data-testid or migrated to CSS-module class names. Adds a daily live-site check workflow so layout changes surface within a day.

## 1.12.0

**Audit pass**

Cleanup hygiene + ship-readiness pass: lint and type-check tightened, bundle-size budgets enforced, Limited Use affirmative statement added, Firefox compatibility documented.

## 1.11.0

**New features**

Daily local maintenance sweep (`alarms` permission) trims the cache and writes a fresh diagnostics ring snapshot. New diagnostics ring buffer surfaces the last 50 events for the "Copy diagnostics" footer button — the bug-report turnaround should be much faster.

## 1.10.0

**New features**

Color-theme picker: Okabe-Ito (colorblind-safe default), Traffic Light, Deuteranopia-safe, and a fully-custom mode. Every text colour passes WCAG AA on its surface; level letters (L/M/H) survive grayscale.

## 1.9.0

**Audit pass**

A 19-wave next-level pass: tighter architecture, sharper diagnostics, distinct fetch-failed badge icon, goal-preset quick-select, and a refreshed welcome page.

## 1.8.0

**Audit pass**

Security and reliability hardening across the fetch and cache paths, plus a tightened palette where chrome and data colours never compete.

## 1.7.0

**Polish & UX**

Stale cached badges (older than 7 days) are subtly de-emphasized so a freshly-fetched badge stands out. Loading affordances no longer stack: the spinning badge is the affordance. Tooltip copy distinguishes "we tried but failed" from "no link to load from". Typography snapped to a clean 4-step scale.

## 1.6.0

**Audit pass**

Tooltip "Report wrong data" actually opens the form now. Multi-nutrient hero says "Medium Sugar" instead of bare "Medium". Tooltip subcopy stays legible on every level theme. Faster scans on listing pages with 30+ tiles.

## 1.5.0

**Audit pass**

Security audit: redirect validation, DOMPurify CVE bumps, cache cross-tab merge bounds. Cache split into store / persistence / migration. New focus rings on the Per 100g/ml toggle.

## 1.4.1

**Polish & UX**

Time-to-first-badge histogram surfaces in diagnostics. Error notifications dedup. Tooltip threshold caption matches the basis (per 100g vs per 100ml).

## 1.4.0

**New features**

"This Page" plot is now the first thing you see. Every badge carries an L/M/H letter so the level reads even in grayscale. Daily selector audit so layout changes surface within a day, not a week.

