# Liquid Stock List

A single-page app for listing all liquid stock, grouped by brand.

Each entry stores: Liquid Brand, Range, Type of Liquid, Capacity, ABV (alcohol by volume), Detail, Picture link, Stock Place, Note and Quantity.

## Features

- Add a liquid with brand, range, type, detail, place and quantity. Save stays disabled until brand, range, type and quantity are filled in
- Cards grouped by brand, with per-brand actions: add range, rename, delete brand, hide
- Quantity stepper (+ / −) on every card, edit and delete per entry
- Search and filter by type of liquid
- Live data in Supabase (table `public.liquid_stock`), shared by the whole team and updated in real time
- Team sign-in with Supabase Auth (email and password)

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app (HTML, CSS and JavaScript in one file) |
| `vercel.json` | Vercel settings for a static site (clean URLs, basic headers) |

## Deploy to Vercel

1. Sign in at [vercel.com](https://vercel.com) and choose **Add New → Project**.
2. Import this GitHub repository.
3. Leave **Framework Preset** as **Other**. Leave Build Command and Output Directory empty.
4. Click **Deploy**.

Every push to `main` redeploys the site automatically.

## Run locally

Open `index.html` in a browser. No build step or dependencies.

## Supabase

- Project: `gxbhnrovgtiylqsukshm`
- Table: `public.liquid_stock` (brand, model, liquid_type, capacity, abv, detail, image_url, note, stock_place, quantity, is_sample)
- Row Level Security is on. Only signed-in users can read, add, edit or delete rows.
- The publishable key in `index.html` is safe to expose. Access is controlled by the policies above.

### Who can sign in

Anyone who can create an account in this Supabase project counts as signed in. To limit it to your team, open Supabase **Authentication → Sign In / Providers** and turn off **Allow new users to sign up** once your team has accounts, or enable email confirmation. Accounts from other apps in the same project can also sign in.
