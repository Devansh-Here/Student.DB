# 🎓 Student.DB — Student Record System

A clean, responsive, single-file web app for managing student records with an integrated Achievers leaderboard. No backend required — runs entirely in the browser.

---

## ✨ Features

### 📋 Records Tab
- **Add / Edit / Delete** student records via a smooth modal form
- **Search** across name, student ID, and branch in real time
- **Filter** by branch (CSE, IT, ECE, ME, CE, Cybersecurity) and year group
- **Sort** by CGPA (high → low or low → high)
- **Stats bar** showing total students, number of branches, year groups, and average CGPA
- Color-coded CGPA badges: 🟢 ≥ 8.5 · 🟡 7.0–8.4 · 🔴 < 7.0

### 🏆 Achievers Tab
- **Podium** view for the top 3 students with gold/silver/bronze styling
- **Full ranked table** with progress bars, rank badges, and medal emojis
- Ranks update automatically as students are added or edited

### 💾 Persistence
- All data is saved to **localStorage** — records survive page refreshes
- Pre-loaded with 7 sample students on first launch

---

## 🚀 Getting Started

No installation or build step needed.

1. Download or copy `index.html`
2. Open it in any modern browser
3. Start managing records immediately

```
open index.html
```

---

## 🗂 Data Fields

| Field | Required | Notes |
|---|---|---|
| Student ID | ✅ | Must be unique (e.g. `2024CS001`) |
| Full Name | ✅ | |
| Branch | ✅ | CSE / IT / ECE / ME / CE / Cybersecurity |
| Year | ✅ | 1st – 4th Year |
| Email | ✅ | |
| Phone | — | 10-digit number |
| CGPA | — | 0–10 scale, used for rankings |

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Markup | HTML5 |
| Styling | CSS3 (custom properties, grid, flexbox) |
| Logic | Vanilla JavaScript (ES6+) |
| Fonts | Syne · DM Sans (Google Fonts) |
| Storage | Browser `localStorage` |

No frameworks, no dependencies, no build tools.

---

## 📁 File Structure

```
index.html        ← entire app (HTML + CSS + JS in one file)
README.md         ← this file
```

---

## 🖥 Browser Support

Works in all modern browsers: Chrome, Firefox, Safari, Edge.  
Responsive layout supports mobile screens (≥ 375px).

---

## 🔧 Customization

**Adding more branches** — update the `<option>` lists in both the filter toolbar and the modal form inside `index.html`.

**Changing CGPA thresholds** — edit the `cgpaClass()` function:
```js
function cgpaClass(v) {
  if (n >= 8.5) return 'cgpa-high'; // green
  if (n >= 7.0) return 'cgpa-mid';  // yellow
  return 'cgpa-low';                // red
}
```

**Resetting sample data** — clear `localStorage` in your browser's DevTools, then reload.

---

## 📄 License

MIT — free to use, modify, and distribute.
