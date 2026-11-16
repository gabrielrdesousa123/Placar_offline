# 🎯 Boccia Scoreboard Offline — SCBP

**Complete digital scoreboard for Paralympic Boccia matches, 100% offline.**

A faithful replica of the live scoreboard from [SCBP](https://scboccia.com) (Paralympic Boccia Championship System), running in a single HTML file with no server, internet, or installation required. Ideal for referees, competition organizers, and coaches who need to score matches anywhere.

---

## 🌐 Languages / Idiomas / Idiomas

- 🇧🇷 **Português (BR)** — [README.md](README.md)
- 🇺🇸 **English** — [README.en.md](README.en.md) ← you are here
- 🇪🇸 **Español** — [README.es.md](README.es.md)

The scoreboard itself includes a **language selector** at the top (PT | EN | ES).

---

## ✨ Features

### ⚽ During the match
- **Giant scoreboard** red × blue, matching the official SCBP layout
- **Individual timer per athlete** with play/pause (separate countdown for each side)
- **Ends (partials)**: P1, P2, P3, P4 + Tiebreak (TB1, TB2) with separate scores
- **Balls per end** with clickable counters (+/−)
- **Full violations system** based on Article 16 of World Boccia Rules 2025-2028:
 - Retraction (Art. 16.5)
 - Penalty Ball (Art. 16.6)
 - Retraction + Penalty (Art. 16.7)
 - Penalty + Yellow Card (Art. 16.8)
 - Yellow Card (Art. 16.9)
 - Red Card (Art. 16.11)
 - Forfeit (Art. 16.12)
- **Penalty ball counter (1P)** with yellow chip
- **Automatic tiebreak** when tied at the end of the last end
- **Auto-save** to `localStorage` — close the browser and resume where you left off

### 📺 Scoreboard Display (TV Mode)
- **"Scoreboard"** button in the menu opens a new tab with a TV-ready layout for court display
- Auto-refreshes every 2 seconds (reads `localStorage`)
- Perfect for TVs, projectors, or tablets placed beside the court

### 📄 Official Scoresheet
- Modal with scoresheet **identical** to the World Boccia / ANDE template used in SCBP
- Partial scores table with individual athlete times
- Grouped violations (with "N × 1 Penalty Ball" counter)
- Winner box with highlighted border
- **"Print / Save PDF"** button — uses native browser printing, works offline

### 🏅 Supported official classes
| Class | Format | Ends | Balls/athlete | Time/end |
|-------|--------|------|---------------|----------|
| BC1 | Individual | 4 | 6 | 4:30 min |
| BC2 | Individual | 4 | 6 | 3:30 min |
| BC3 | Individual (w/ RO) | 4 | 6 | 6 min |
| BC4 | Individual | 4 | 6 | 3:30 min |
| Pairs BC3 | Doubles | 4 | 3 | 7 min |
| Pairs BC4 | Doubles | 4 | 3 | 4 min |
| Team | Trio (BC1+BC2) | 6 | 2 | 5 min |
| ⚙️ Custom | Personalized | 1-10 | 1-6 | 60-900s |

### 💻 Desktop
- Desktop application (Windows, Mac, Linux)
- Fullscreen mode (F11) available in the menu

---

## 🚀 How to use

### Option 1 — Direct download (recommended)
1. Download the [`index.html`](./index.html) file from this repository
2. Double-click to open in any modern browser (Chrome, Edge, Firefox, Safari)
3. Done! No installation, server, or internet needed

### Option 2 — Clone the repository
```bash
git clone https://github.com/gabrielrdesousa123/Placar_offline.git
cd Placar_offline
# Open index.html in your browser
```

### Option 3 — Use as PWA
In Chrome/Edge, click the "Install" icon in the address bar to add the scoreboard as an app on your desktop or phone.

---

## 🎮 Quick start guide

1. **Select the class** (BC1, BC2, BC3, BC4, Pairs, Team, or Custom)
2. **Enter names** (optional — if left blank, defaults to "RED" and "BLUE")
3. **Add clubs/teams** (optional)
4. Click **▶ START MATCH**
5. Use the ▶ buttons next to each timer to control each athlete's time
6. Click the score numbers to add points (+1)
7. Use the **−** and **+** buttons to control balls thrown
8. Click **⚠️ Add Violation** to record infractions
9. Click **NEXT END ▶** to advance
10. When finished, click **☰ Menu → View Scoresheet → Print / Save PDF**

---

## 💾 Storage

- All data is saved in the browser's `localStorage`
- When reopening the page, the match resumes where it left off
- To start a new game: **☰ Menu → Reset Complete Game**

---

## 📂 Project structure

```
Placar_offline/
├── index.html ← Complete scoreboard (HTML + CSS + JS in one file)
├── README.md ← Portuguese README
├── README.en.md ← This file (English)
├── README.es.md ← Spanish README
└── LICENSE ← MIT License
```

**Zero external dependencies.** Everything is embedded in `index.html` (~55 KB).

---

## 🧠 Implemented rules

This scoreboard follows the **Official World Boccia (BISFed) Rules 2025-2028**, specifically:

- **Art. 10.16** — Tiebreak criteria
- **Art. 16** — Violations and penalties (16.5 through 16.12)
- **Section 2.1.5.1** — W.O. score (6-0 or largest margin)

---

## 🤝 Contributing

Contributions are welcome! Open an issue or pull request.

---

## 📜 License

[MIT License](LICENSE) — free for personal, commercial use, and modifications.

---

## 🔗 Links

- **SCBP (online system):** [scboccia.com](https://scboccia.com)
- **World Boccia:** [worldboccia.com](https://worldboccia.com)
- **Author:** Gabriel R. de Sousa

---

## ❓ FAQ

**Does it work without internet?**
Yes, 100%. It's a self-contained HTML file.

**Is any data sent to a server?**
No. Everything stays in your browser (localStorage). No data leaves your device.

**Can I use it in official competitions?**
Yes. The layout and rules are identical to those used in SCBP, the system adopted by ANDE and various Brazilian Paralympic Boccia competitions.

**Where is the scoresheet?**
In the ☰ side menu, option "View Scoresheet". You can print or save as PDF.

**How do I open the TV scoreboard?**
In the ☰ side menu, option "Scoreboard Display". A new tab opens with an enlarged scoreboard, ideal for court TVs.