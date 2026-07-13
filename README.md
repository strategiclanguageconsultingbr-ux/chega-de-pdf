# Chega de PDF — Landing Page

Direct-response landing page (PT-BR) for **Chega de PDF**: 40 interactive, self-correcting English exercises for Brazilian ESL teachers. R$29,99.

## Structure

- `index.html` — single-file landing page (all CSS/JS inline)
- `assets/` — hero screenshots, testimonial images, founder photo, exercise gallery

## Configure before launch

Open `index.html` and edit the config block at the top of `<head>`:

```js
var TRACKING = {
  metaPixelId: 'YOUR_META_PIXEL_ID',
  googleAnalyticsId: 'YOUR_GA4_ID',
  googleTagManagerId: 'YOUR_GTM_ID'
};

var CHECKOUT_URL = 'https://pay.cakto.com.br/YOUR_PRODUCT_ID';
```

All CTA buttons point to `CHECKOUT_URL`. Pixel/GA/GTM auto-init only when their IDs are set.

## Purchase event

Fire from the Cakto webhook or thank-you page:

```js
fbq('track', 'Purchase', { value: 29.99, currency: 'BRL' });
```

## Deploy

Hosted via GitHub Pages from the `main` branch, root `/`.
