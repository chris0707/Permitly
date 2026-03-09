# Permitly — User Guide

> **Important:** Permitly does **not** load data automatically. You must click the **Refresh** button to fetch permit data. Before your first refresh, review your Settings to make sure the date range and limits are what you need.

---

## Table of Contents

1. [First-Time Setup](#1-first-time-setup)
2. [Loading Data](#2-loading-data)
3. [Understanding the Status Bar](#3-understanding-the-status-bar)
4. [What Is Geocoding?](#4-what-is-geocoding)
5. [Using the Map](#5-using-the-map)
6. [Searching and Filtering](#6-searching-and-filtering)
7. [Results Table](#7-results-table)
8. [Viewing Permit Details](#8-viewing-permit-details)
9. [Clearing Data](#9-clearing-data)
10. [Tips and Troubleshooting](#10-tips-and-troubleshooting)

---

## 1. First-Time Setup

When you first open Permitly, the screen will be empty with the message: *"No data cached — click Refresh to load permits."*

**Before clicking Refresh, check your settings:**

1. Click the **gear icon** (top-right corner of the header bar).
2. A small panel will appear with these options:

| Setting | What It Means | Default |
|---|---|---|
| **Date Span (Days)** | How far back to look for permits. A value of `10` means "permits from the last 10 days." | 10 |
| **Include Issued Date** | When checked, also matches permits by their issued date (not just application date). | Off |
| **Max Records** | The maximum number of permits to download per city. Check **All** to remove the limit. | 5,000 |
| **Max Geocode** | How many addresses to locate on the map per session (see [What Is Geocoding?](#4-what-is-geocoding)). Check **All** for no limit. | All |
| **Page Size** | How many rows to show per page in the results table. | 25 |

3. Adjust the values to your needs. Your choices are saved automatically and persist even after closing the browser.
4. Click anywhere outside the panel to close it.

---

## 2. Loading Data

Once your settings are ready:

1. Click the blue **Refresh** button (top-right).
2. A loading screen will appear showing progress for each city (e.g., *"Fetching Mississauga... 2,500 permits"*).
3. You can click **Cancel** at any time to stop the download.
4. When finished, the map and table will populate with permit data.

```
 ┌──────────────────────────────────────────────────────┐
 │  Permitly              [gear icon]  [Refresh button] │  <-- Header
 ├──────────────────────────────────────────────────────┤
 │  Mississauga: 5,000 (just now) · Brampton: 1,200... │  <-- Status Bar
 └──────────────────────────────────────────────────────┘
```

**On your next visit**, Permitly will load instantly from saved data — no need to click Refresh again unless you want fresh data.

---

## 3. Understanding the Status Bar

The thin bar below the header has two zones:

```
 ┌────────────────────────────────────────────────────────────┐
 │  [LEFT: City summaries]              [RIGHT: Geocoding]    │
 │  Mississauga: 5,000 · Brampton: 1,200    Geocoding 45/200 │
 └────────────────────────────────────────────────────────────┘
```

- **Left side** — Always visible. Shows the number of permits loaded for each city and how long ago the data was fetched (e.g., *"2h ago"*).
- **Right side** — Only appears while geocoding is in progress (see next section). Shows a pulsing blue dot, a counter, and an X button to cancel.

---

## 4. What Is Geocoding?

Some cities provide permit addresses but **not** map coordinates (latitude/longitude). Geocoding is the process of converting those addresses into map pins.

**How it works in plain terms:**

> Imagine you have a list of 500 addresses on paper. Geocoding is like looking up each address on a map and sticking a pin on it — one by one. Permitly does this automatically in the background after loading your data.

**What you'll see:**

1. After data loads, the status bar shows *"Geocoding... 0/500"*.
2. A pulsing blue dot appears to indicate work is happening.
3. Pins appear on the map in real time as each address is located.
4. The counter updates: *"Geocoding... 45/500"*, *"120/500"*, etc.
5. When finished, the blue dot disappears and the status bar returns to normal.

**Can I cancel it?** Yes — click the small X next to the geocoding counter. All pins mapped so far will remain.

**Why are some permits missing from the map?** If an address cannot be found (misspelling, incomplete data, etc.), it won't appear on the map. Use the **"Show only unmapped"** checkbox (above the results table) to see which permits have no map location.

---

## 5. Using the Map

### Map Controls

The map has several controls around its edges:

```
 ┌──────────────────────────────────────────────────────┐
 │  [+]                              [Light|Medium|Dark]│
 │  [-]                                                 │
 │  [Home]                                              │
 │  [Fullscreen]                                        │
 │                                                      │
 │                     (map area)                       │
 │                                                      │
 │                                           ┌────────┐ │
 │                                           │ Scope  │ │
 │                                           │ legend │ │
 │                                           └────────┘ │
 └──────────────────────────────────────────────────────┘
```

| Control | Location | What It Does |
|---|---|---|
| **+ / -** | Top-left | Zoom in and out |
| **Home** (house icon) | Top-left | Reset the map to the default view (centered on the GTA) |
| **Fullscreen** | Top-left | Expand the map to fill your entire screen. Press **Escape** or click again to exit |
| **Light / Medium / Dark** | Top-right | Switch the map style between a light, neutral, or dark background |
| **Scope Legend** | Bottom-right | Shows which colors represent which permit types. Click the header to collapse/expand it. The legend scrolls if there are many categories |

### Interacting with Pins

- **Clustered pins** — When many permits are close together, they group into a circle with a number (e.g., "42"). Click the cluster to zoom in and see individual pins.
- **Individual pins** — Click any colored dot to see a popup with the permit number, address, scope, and date.
- **Detail panel** — Clicking a pin also opens a slide-out panel on the right with the full permit details. Click the X or click outside the panel to close it.

---

## 6. Searching and Filtering

### Search Bar

Type any keyword into the search box and click **Search** (or press Enter). The search looks across:
- Permit numbers
- Addresses
- Descriptions

As you type, a dropdown of suggestions appears. Use the arrow keys to navigate and Enter to select.

**Tip:** Leave the search box empty and click Search to see all permits (within your filter settings).

### Advanced Filters

Click the **Filters** button (next to Search) to reveal additional options:

| Filter | What It Does |
|---|---|
| **Municipality** | Show permits from a specific city only |
| **Filter Date By** | Choose whether to filter by Applied Date, Issued Date, or Either |
| **Date From / Date To** | Narrow results to a specific date range |
| **Scope** | Filter by permit type (e.g., New Construction, Renovation) |
| **Building Type** | Filter by structure type (e.g., Residential, Commercial) |

Click **Clear Filters** to reset all filters back to their defaults.

---

## 7. Results Table

Below the map, the results table shows all matching permits:

```
 ┌──────────────────────────────────────────────────────────────────┐
 │  Permits                    [ ] Show only unmapped   1,234 total │
 ├─────────┬──────────┬───────┬──────┬────────┬────────┬───────────┤
 │ Permit# │ Address  │ Scope │ Type │ Value  │Applied │ Issued    │
 ├─────────┼──────────┼───────┼──────┼────────┼────────┼───────────┤
 │ BP-1234 │ 100 Main │ New   │ Res  │ $250K  │ Jan 5  │ Feb 10    │
 │ ...     │ ...      │ ...   │ ...  │ ...    │ ...    │ ...       │
 └─────────┴──────────┴───────┴──────┴────────┴────────┴───────────┘
                         [1] [2] [3] ... [Next]
```

- **Sort** — Click any column header to sort ascending. Click again to reverse.
- **Pages** — Use the numbered buttons at the bottom to navigate between pages.
- **Show only unmapped** — Check this box to see permits that have no map location (useful for data quality checks).
- **Click a row** — Opens the full detail panel on the right.

---

## 8. Viewing Permit Details

When you click a table row or a map pin, a panel slides in from the right:

- Shows all available information: permit number, status, address, description, scope, building type, estimated value, dates, and municipality.
- Click the **X** in the top-right corner (or click the dimmed area behind it) to close the panel.

---

## 9. Clearing Data

If you want to start fresh:

1. Click the **gear icon** to open Settings.
2. Click the red **Clear Cache** button at the bottom.
3. All downloaded permit data and geocoded locations will be removed.
4. Your settings (date span, max records, map theme, etc.) are **preserved** — only the data is cleared.
5. Click **Refresh** to load new data.

---

## 10. Tips and Troubleshooting

| Situation | What To Do |
|---|---|
| Map is empty | Click **Refresh** to load data. Permitly never fetches automatically. |
| Data looks outdated | Click **Refresh** to pull the latest permits from each city's database. |
| Geocoding is too slow | Open Settings and lower the Max Geocode number, or uncheck "All" and set a specific limit. |
| Settings feel wrong | Open the gear icon and adjust. Changes take effect on the next Refresh. |
| Map pins overlap | Zoom in — clustered pins will split apart. Or click the cluster circle to zoom automatically. |
| Can't find a permit | Try searching by address or permit number. Clear any active filters first. |
| Want a lighter map | Use the **Light / Medium / Dark** switcher in the top-right corner of the map. |
| Page loads but no data appears | You may need to serve the folder with a local web server (ask your technical contact for help). |
| Want to see more rows at once | Open Settings and increase the **Page Size** value. |

---

*This guide covers Permitly v1.11. For technical details and configuration, see [README.md](README.md).*
