# 🏓 Table Tennis Analytics Dashboard

A clean, minimal web app that embeds a Power BI analytics dashboard for table tennis team performance. Hosted free on GitHub Pages.

**Live site:** https://7446Nguyen.github.io/powerBI_TTAnalytics/

---

## About the dashboard

This dashboard gives a full picture of team and player performance across matches, tournaments, and league play. It is designed for club-level analysis — coaches and players can use it to track results over time, compare performance across individuals, and monitor standings at a glance.

**What it covers:**

- **Match results** — win/loss records, scores, and head-to-head history across all tracked matches
- **Player stats** — individual performance breakdowns so you can see how each player is contributing and trending over time
- **Tournament & league data** — standings, competition results, and how the team is performing across different events

The data is sourced and maintained in Power BI, and the dashboard updates automatically whenever the underlying dataset is refreshed.

---

## How to use it

The dashboard is fully interactive. Here's what you can do:

**Filter and slice the data**
Use the filter panel (usually on the right side or accessible via the funnel icon) to narrow the view by date range, player, tournament, or match type. Filters apply across all visuals on the page simultaneously.

**Drill into a visual**
Click on a bar, data point, or table row to cross-filter the other visuals on the page — for example, clicking a player's name will highlight only their results throughout the entire report.

**Switch between report pages**
If the dashboard has multiple pages, use the navigation tabs at the bottom of the report to move between views (e.g., Overview, Player Stats, Tournament Results).

**Hover for tooltips**
Hovering over any chart element shows a detailed tooltip with the exact values behind that data point.

**Reset filters**
To clear all active filters and return to the full dataset, click the reset/eraser icon in the Power BI toolbar, or refresh the page.

**Full screen**
For the best viewing experience, click the full screen icon (⤢) in the bottom-right corner of the report, or use the browser's full screen mode (`F11`).

> The report is read-only for viewers — no data can be changed through the dashboard.

## Tech stack

- Pure HTML / CSS / JS — no frameworks, no build tools
- [Power BI Embedded](https://powerbi.microsoft.com/en-us/power-bi-embedded/) (public publish-to-web)
- [GitHub Pages](https://pages.github.com/) for free static hosting

---

*Built by Jeff Nguyen*
