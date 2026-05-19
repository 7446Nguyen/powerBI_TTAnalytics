# 🏓 Table Tennis Analytics Dashboard

A clean, minimal web app that embeds a Power BI analytics dashboard for table tennis performance data. Hosted free on GitHub Pages.

**Live site:** `https://<your-username>.github.io/<repo-name>/`

---

## What's inside

```
├── index.html        # Main page — embeds the Power BI report
├── _config.yml       # GitHub Pages configuration
├── .gitignore        # Standard Git ignores
└── README.md         # This file
```

The entire site is a single `index.html` — no build step, no dependencies, no server required.

---

## Deploy to GitHub Pages (step by step)

### 1. Create a new GitHub repository

Go to [github.com/new](https://github.com/new) and create a repository. You can name it anything — e.g. `tt-dashboard` or `table-tennis-analytics`.

Make it **Public** (required for free GitHub Pages).

### 2. Upload the files

**Option A — drag & drop in the browser**

1. Open your new repo on GitHub
2. Click **Add file → Upload files**
3. Drag all the files from this folder into the upload area
4. Commit to `main`

**Option B — Git CLI**

```bash
git init
git add .
git commit -m "Initial commit: table tennis dashboard"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

### 3. Enable GitHub Pages

1. In your repo, go to **Settings → Pages**
2. Under **Source**, select **Deploy from a branch**
3. Choose branch: `main` / folder: `/ (root)`
4. Click **Save**

GitHub will give you a URL like `https://<your-username>.github.io/<repo-name>/` — it usually goes live within 1–2 minutes.

---

## Updating the Power BI embed link

The embed URL is set in `index.html` on this line inside the `<iframe>` tag:

```html
src="https://app.powerbi.com/view?r=eyJr..."
```

To swap in a new report:

1. In Power BI, open your report and click **File → Embed report → Website or portal**
2. Copy the embed URL (the `src=` value from the `<iframe>` code Power BI gives you)
3. Open `index.html`, find the `<iframe>` tag, and replace the `src` value
4. Commit and push — GitHub Pages will update automatically within a minute

> **Note:** The embed link must be a **public** Power BI publish-to-web link. Reports behind organizational authentication will not load for visitors.

---

## Customization

| What | Where in `index.html` |
|---|---|
| Page title (browser tab) | `<title>` tag in `<head>` |
| Header title & subtitle | `.site-title` and `.site-subtitle` text |
| Accent color | `--accent` CSS variable (default `#4f8ef7`) |
| Background color | `--bg` CSS variable (default `#0f1117`) |
| Footer text / links | `<footer>` block at the bottom |
| Logo emoji | The `🏓` inside `<div class="logo">` |

---

## Troubleshooting

**Dashboard shows a blank or "This content can't be displayed" error**
Your Power BI report may be set to require sign-in. Re-publish it via **File → Embed report → Website or portal** to generate a public embed link.

**The iframe loading spinner never disappears**
This is a known browser behavior — cross-origin iframes sometimes don't fire the `load` event. The spinner auto-hides after 8 seconds as a fallback. The report itself is still loading correctly.

**GitHub Pages URL returns a 404**
Make sure `index.html` is in the root of the `main` branch (not in a subfolder), and that Pages is configured to deploy from that branch.

---

## Tech stack

- Pure HTML / CSS / JS — no frameworks, no build tools
- [Power BI Embedded](https://powerbi.microsoft.com/en-us/power-bi-embedded/) (public publish-to-web)
- [GitHub Pages](https://pages.github.com/) for free static hosting

---

*Built by Jeff Nguyen*
