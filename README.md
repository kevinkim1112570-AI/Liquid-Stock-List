# Liquid StockList

A single-page app for listing all liquid stock, grouped by brand.

Each entry stores: Liquid Brand, Model, Type of Liquid, Detail, Stock Place and Quantity.

## Features

- Add a liquid with brand, model, type, detail, stock place and quantity
- Cards grouped by brand, with per-brand actions: add model, rename, delete brand, hide
- Quantity stepper (+ / −) on every card, edit and delete per entry
- Search and filter by type of liquid
- Data is saved in the browser's local storage (key `liquid-stocklist-v1`)

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

## Note on data

Local storage is per browser and per device. Each person who opens the site sees their own list. Sharing one live list across a team needs a shared database.
