# Family Budget Tracker

A single-file HTML budget tracker that runs on any device. Data lives in `localStorage` on the device — nothing is sent to a server. Use the export/import workflow to sync between devices.

**Live URL:** https://mangokarate.github.io/FamilyBudgetTracker/

---

## Overview

This repository hosts the Family Budget Tracker via GitHub Pages. The `index.html` file at the root is the entire app — open the live URL in any modern browser and the tool runs locally in that browser tab.

There are two variants of the tool:

- **Desktop version** — full-width table layout, inline editing, keyboard shortcuts, print reports
- **Mobile version** — card layout, bottom sheets, native month picker, optimized for touch

Both share the same `localStorage` storage key (`familyBudgetV1`) and identical JSON export format, so you can move data between them seamlessly.

The file currently deployed is whichever version (desktop or mobile) was most recently committed as `index.html`. Pick whichever fits your primary use case and bookmark the URL.

---

## Updating the file (push a new version)

When a new version of the tracker is ready, replace `index.html` in this repo. GitHub Pages auto-deploys within ~30 seconds.

### Step 1 — Open the repo on GitHub

Go to https://github.com/MangoKarate/FamilyBudgetTracker

### Step 2 — Delete the old `index.html`

1. Click `index.html` in the file list
2. Click the trash icon 🗑️ at the top-right of the file viewer
3. Scroll down and click **Commit changes**

### Step 3 — Upload the new file

1. From the repo root, click **Add file → Upload files**
2. Drag the new HTML file from your Mac into the upload area
3. **Important:** rename the file to `index.html` before committing — GitHub Pages only serves a file with that exact name as a webpage
4. Scroll down and click **Commit changes**

### Step 4 — Wait and refresh

GitHub Pages deploys the new version within about 30 seconds. Pull up the live URL in Safari and refresh.

> **Note:** Your existing budget data is unaffected. Data lives in `localStorage` on the browser, not in the HTML file. Updating the tracker code does not touch your transactions.

---

## Bookmarking on Safari (Mac)

Bookmarks sync across devices via iCloud, so this is the most efficient way to set up access on your iPhone too.

### Step 1 — Open the live URL in Safari

Paste https://mangokarate.github.io/FamilyBudgetTracker/ into the address bar and press **Return**.

### Step 2 — Add the bookmark

Press **⌘ + D** (or use the **Bookmarks** menu → **Add Bookmark…**)

### Step 3 — Save it to Favorites

In the dialog, set the location to **Favorites** so it appears on Safari's start page on every device. Click **Add**.

### Step 4 — Confirm iCloud sync

- **Mac:** System Settings → Apple ID → iCloud → confirm Safari is enabled
- **iPhone:** Settings → [your name] → iCloud → confirm Safari is enabled

The bookmark appears under Favorites on your iPhone within a minute.

### Bonus — Add to iPhone Home Screen

For a more app-like experience on iPhone:

1. Open the bookmark in Safari on your phone
2. Tap the Share button ↗
3. Choose **Add to Home Screen**

It now launches like a native app, runs full-screen, and remembers your localStorage data between sessions.

---

## Finding the live URL

If you ever forget the URL or need to confirm it's still live:

1. Go to the repo Settings tab
2. Click **Pages** in the left sidebar
3. The live URL is shown at the top, with a **Visit site** button

---

## Data and privacy

- The HTML file is just the application logic — no personal data
- Your transactions, balances, and categories are stored in your browser's `localStorage`
- Nothing is sent to GitHub or any server
- The repo can be private or public — either way, the data never leaves your device
- To back up data, use the in-app **Export Data** option (downloads a date-stamped JSON file)
- To restore or sync to another device, use **Import Data** with that JSON file

---

## File structure

```
FamilyBudgetTracker/
├── index.html      ← The tracker (desktop or mobile build)
└── README.md       ← This file
```

That's the entire repo. No build step, no dependencies, no framework.
