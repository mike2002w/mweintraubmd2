# Outlet logos

Self-hosted SVGs for the "In the News" press grid and other press surfaces.

## Why files, not hotlinks or inline SVG

Previously the NBC logo was hotlinked from Wikipedia's CDN, which started returning HTTP 429 (rate limited). Self-hosted SVGs are stable, cacheable, and don't break when someone else's CDN changes policy.

## Add a new outlet

1. Drop an SVG into this directory (`outlet-name.svg`). Prefer SVG over PNG/JPG — crisp at any size, tiny file size.
2. Reference it in HTML:
   ```html
   <a href="press.html" class="press-logo" aria-label="Featured on Outlet Name">
     <img src="images/logos/outlet-name.svg" alt="Outlet Name" loading="lazy">
   </a>
   ```
3. The `.press-logo` wrapper handles hover state + sizing. No per-logo CSS needed.

## Sources

- `nbc.svg` — NBC peacock, downloaded from Wikimedia Commons (NBC logo file). Trademark: NBCUniversal.
- `cnbc.svg` — CNBC wordmark, downloaded from Wikimedia Commons. Trademark: NBCUniversal. (Not currently rendered on the site; available for future use.)
- `time.svg`, `medscape.svg`, `wired.svg` — stylized text wordmarks (own composition). Readable at small sizes; can be swapped for an outlet's official SVG at any time without touching the HTML.

## Fair-use note

"As seen on / featured in" use of third-party marks to state a factual claim (the outlet actually covered us) is generally considered nominative fair use. Use each outlet's unmodified official logo where possible and do not imply endorsement beyond mention.
