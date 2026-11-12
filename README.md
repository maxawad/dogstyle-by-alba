# DOGSTYLE By Alba

A one-page Spanish-language website for a dog grooming salon and pet shop run by Alba. Visitors can read about the services, see a photo gallery and reviews, contact Alba on WhatsApp to book, and buy a few dog products through an online cart.

## What it does

- Presents the grooming services (full grooming, bath and brushing, nail and paw care, creative styling, anti-shedding treatment).
- Shows an "about me" section, a gallery and customer reviews.
- Has a small shop with five products and a shopping cart (add, remove, total).
- Sends the cart to Stripe Checkout (hosted payment page) in "client-only" mode, so no server is needed.
- Every booking button opens a WhatsApp chat with a prefilled message. There is also a link to the salon's Instagram.
- Works on phones, with a mobile menu and cart button.

## Tech stack

- Plain HTML, CSS and JavaScript in a single file, `index.html`. No build step and no dependencies.
- Google Fonts (Playfair Display and Inter), loaded from the web.
- Stripe.js v3 for checkout, loaded from `https://js.stripe.com/v3/`.
- GitHub Pages for hosting (see `.github/workflows/deploy.yml`).

## Run it

You only need a static file server. From the repository root:

```bash
npm start
```

or, without npm:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000. You can also open `index.html` directly in a browser, but checkout redirects work best when the page is served over http.

## Live demo and hosting

The site is a static page, so the repository root is the whole site. Pushing to `main` runs the GitHub Pages workflow, which publishes the root folder. If Pages is enabled for the repository, the demo is at `https://maxawad.github.io/dogstyle-by-alba/`.

## Shop and payments

The cart uses Stripe Checkout with prices created in the shop owner's Stripe account (the price IDs are listed near the top of the script in `index.html`). The Stripe key in the page is a publishable key, which is meant to be public. Payments only work for the owner's Stripe account, and Stripe must have client-only Checkout enabled in the dashboard. If you fork this project, replace the publishable key and the price IDs with your own, and change the contact number and social links.

## Status

Working. It is a live business website, so the shop is wired to real products. Visitors trying the demo should not complete a real purchase.

## Credits

Built for DOGSTYLE By Alba. Fonts by Google Fonts, payments by Stripe.
