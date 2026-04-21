# Budget Tracker

A personal expense tracker that runs entirely in your browser — no server, no account, no dependencies. One HTML file.

## Features

- **Manual entry** — add expenses with amount, category, date, and an optional note
- **Paste & Parse** — paste messy text like `starbucks 6.50 tuesday` and it extracts the amount, guesses the category, and parses relative dates (today, yesterday, Monday, etc.)
- **Bulk CSV / TSV import** — copy cells directly from Google Sheets and paste them in; auto-detects headers and maps columns, with an editable preview before committing
- **24 built-in categories** — Bank, Bill, Coffee, Food, Grocery, Health, Rent, Transportation, Travel, and more; add custom categories at any time
- **Monthly summary sidebar** — total spent this month, total this week, and a CSS bar chart breaking down spending by category
- **Month navigation** — step back through past months to review historical spending
- **Inline edit & delete** — edit any expense in place without leaving the list
- **Export / Import JSON** — download a full backup and restore it later; imports merge by ID so no duplicates
- **localStorage** — all data persists in the browser automatically, no setup required
- **Mobile-friendly** — responsive layout that works from 375 px iPhones up to wide desktop screens

## Running locally

Just open the file:

```bash
open index.html
```

Or double-click `index.html` in Finder. No build step, no `npm install`, no server needed.

## Deploying to GitHub Pages

1. Push this repo to GitHub (see below).
2. Go to **Settings → Pages** in your repo.
3. Set source to **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. Your tracker will be live at `https://<USERNAME>.github.io/<REPO-NAME>/`.

## Known limitations

- **Single-browser storage** — data lives in `localStorage` for the browser you use. Clearing browser data will erase it. Use Export JSON regularly as a backup.
- **No cloud sync** — expenses don't sync across devices or browsers. To move data, export on one device and import on another.
- **No multi-user support** — the app is designed for one person's personal budget.
- **No recurring transactions** — there's no way to schedule or auto-repeat a monthly bill; each expense must be added manually or imported.
- **CSV date parsing** — unusual date formats from bank exports may not parse correctly; the preview lets you catch this before importing.
