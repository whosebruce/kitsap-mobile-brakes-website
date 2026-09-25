# Kitsap Mobile Brakes & Oil

Website for Kitsap Mobile Brakes & Oil, a mobile brake, oil change and general mechanical service in Kitsap County, Washington. Live at [kitsapmobilebrakes.com](https://kitsapmobilebrakes.com).

The site is three static HTML pages with inline styles and no JavaScript or build step. Customers call or text the business line; there is no booking system or contact form.

## Pages

| Page | URL | File |
| --- | --- | --- |
| Home | `/` | `index.html` |
| Services and prices | `/services/` | `services/index.html` |
| Contact | `/contact/` | `contact/index.html` |

`services.html` and `contact.html` are `noindex` redirects to the clean URLs so older links keep working. Logos live in `assets/`. `sitemap.xml` and `robots.txt` list the three clean URLs.

## Preview locally

From the repo root:

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>. Serve the folder rather than opening the files from disk: the pages use root-relative links like `/services/` and `/assets/kmbo-wordmark.png`.

## Deployment

GitHub Pages publishes the `main` branch from the repo root. There is no workflow or build step, so a push to `main` goes live once the Pages build finishes. `CNAME` holds the custom domain and `.nojekyll` turns off Jekyll processing.

## Making changes

Prices, the phone number and the service-area list are written directly into the HTML:

- The phone number appears on all three pages.
- Prices appear on the home page and the services page.
- Canonical and Open Graph URLs should stay on `https://kitsapmobilebrakes.com/`.

Business records and the invoicing tool are kept out of this public repo on purpose.

## Maintainer

Built and maintained by [Bruce Works](https://bruceworks.net).
