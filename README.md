# Character Ledger — D&D 5e (2024) Character Sheet

A fillable, digital D&D 5e (2024 Player's Handbook rules) character sheet that runs entirely in the browser — no server, no database, no build step. Styled like an old ledger/parchment page, with autosave, printing, and installable-app support built in.

## Features

- **Species & Class dropdowns** with conditional Sub-species and Subclass menus that populate automatically based on your pick
- **Background & Alignment dropdowns**
- **Ability score cards** — one card per ability showing Score, Modifier, Saving Throw, and the skills tied to that ability, each with:
  - A proficiency dot (click to cycle: none → proficient → expertise)
  - An Advantage / Disadvantage toggle (click to cycle: — → A → D)
- **Combat tab** — AC, Initiative, Speed, Passive Perception, HP/Temp HP, Hit Dice, Death Saves, an Exhaustion track (2024 cumulative −2 rules), and an Attacks table with a Weapon Mastery column
- **Spells tab** — spellcasting ability, auto-calculated Save DC and Spell Attack Bonus, and slots/spell lists for levels 1–9
- **Equipment tab** — currency, a gear table, and attunement slots
- **Features tab** — repeatable cards for Species Traits, Class Features, and Feats (name + source + description)
- **Backstory tab** — personality traits, ideals, bonds, flaws, appearance, backstory, allies, and notes
- **Character portrait upload**
- **Theme controls** — 6 accent color presets (plus a custom color picker) and 3 paper presets (Parchment, Ivory, Midnight) with text colors pre-matched for readability
- **Autosave** as you type, plus manual Export/Import to a JSON file for backups or moving between devices
- **Print support** — each tab prints as its own page, with the community logo watermarked faintly in the background
- Installable as a **Progressive Web App**: works offline, gets a home-screen icon, and opens full-screen on mobile
- **Shareable links** — save your character to the cloud and get a private edit link plus a read-only view link to send your DM or party (see `backend/README.md` for setup)

## Files

| File | Purpose |
|---|---|
| `index.html` | The character sheet itself (HTML/CSS/JS, single page app) |
| `manifest.webmanifest` | PWA manifest (name, icons, theme color) |
| `service-worker.js` | Offline caching for the PWA |
| `icon-192.png`, `icon-512.png`, `icon-512-maskable.png`, `apple-touch-icon.png` | App icons |
| `backend/` | Small API + MongoDB setup that powers the "Save & Share" links — see `backend/README.md` |

## Getting Started

### Just open it
Double-click `index.html`, or open it in any modern browser. That's it — everything runs client-side.

### Host it as a website / installable app
1. Upload all the files in this folder to any static host (GitHub Pages, Netlify, Vercel, Cloudflare Pages, etc.), keeping them in the same folder together.
2. Visit the hosted URL on your phone or desktop.
3. Your browser will offer **"Add to Home Screen"** / **"Install app"** — accept it to use the sheet like a native app, including offline.

### GitHub Pages (quick path)
1. Push this folder to a repo.
2. In the repo settings, enable **Pages** and point it at the branch/folder containing `index.html`.
3. Your sheet will be live at `https://<username>.github.io/<repo>/`.

## Data & Privacy

Everything is stored locally in your browser (or, when used inside Claude, via Claude's per-conversation storage) — nothing is sent to a server. Use the **Export JSON** button to back up a character or move it to another device/browser, and **Import JSON** to load it back in.

## Tech

Plain HTML, CSS, and vanilla JavaScript — no frameworks, no build tools, no dependencies.
