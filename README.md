# Glamp Sierra Website

A static HTML website for Glamp Sierra 2026. Designed to be hosted on GitHub Pages.

## Files

- `index.html` — Home page
- `pricing.html` — Lodging & meal plan pricing
- `faq.html` — FAQ with accordion, What to Bring, hike list
- `location.html` — Map, nearby attractions, hike suggestions
- `registration.html` — Full registration form with pricing calculator
- `shared.css` — Shared styles (nav, footer, layout, typography)

## Publishing to GitHub Pages

1. Create a new repository at github.com (e.g. `glamp-sierra`)
2. Upload all these files to the repository
3. Go to **Settings → Pages**
4. Under "Source" select **Deploy from a branch → main → / (root)**
5. Your site will be live at `https://yourusername.github.io/glamp-sierra`

To use a custom domain (glampsierra.com):
- Add a file called `CNAME` containing just: `glampsierra.com`
- Update your domain's DNS settings to point to GitHub Pages

## Things to update each year

All in the `<script>` block at the top of `registration.html`:

```js
const FORMSPREE_ENDPOINT = 'https://formspree.io/f/YOUR_ID';
const VENMO_HANDLE  = '@YourHandle';
const ZELLE_EMAIL   = 'your@email.com';
const PAYPAL_ME     = 'YourUsername';

const LODGE_PRICES  = { dorm: 300, duplex: 700, kings: 850 };
const PLAN_PRICES   = { full: 250, nona: 175 };
```

Also update dates and year across all pages (search for "2026" and "August 6").

## Editing tips (VS Code)

- Install **Live Preview** extension to see changes in real time
- Press `Ctrl+H` (or `Cmd+H` on Mac) to find and replace across files
- All styles shared across pages live in `shared.css`
- Page-specific styles are in `<style>` tags within each HTML file
