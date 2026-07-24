# Chineme Uba — "The Universe" (interactive resume) + hidden CHINEME-OS terminal

A single interactive site with two connected experiences:

- **`index.html`** — *The Universe*: a three.js particle world. Your name assembles from thousands of glowing particles that scatter from the cursor and dissolve as you scroll through a cosmic journey of your career.
- **`terminal/index.html`** — *CHINEME-OS*: a retro CRT terminal resume you can type commands into (including a playable chess game). It's hidden — reached as an easter egg from the Universe.

## What's new in this version

- **"A doctor on every wrist" — a live AI × wearables demo.** A new section (05 · The Horizon) with an interactive smartwatch: a live ECG, heart rate, SpO₂ and temperature. Visitors click **Simulate allergic reaction / cardiac event / fall** and watch the on-device AI detect the anomaly, escalate, and autonomously "contact first responders" with location + live vitals. This is the section built to be screenshotted and shared — it shows both the vision and the engineering behind it.
- **The terminal as a hidden portal.** Type **`sudo`** (or `terminal`) anywhere on the Universe, or click the glowing `sudo` in the footer, and a boot sequence takes over the screen and drops you into CHINEME-OS. A **"↖ exit to the Universe"** link brings people back. Finding it counts toward the secret tracker.
- **Six secrets to find** (tracked top-right): Konami code ↑↑↓↓←→←→BA, type `grandma`, type `chess`, click your name 5×, open the console and run `hire()`, and boot the terminal.
- **Recruiter mode** (top-right) opens a clean printable resume — the fast path — now including your AI-wearables interest.

Everything is procedural three.js loaded from a CDN — no assets to upload, no build step. The whole thing works on mobile and respects reduced-motion.

---

## Deploy it free on GitHub Pages (step by step)

Because this site has **two files in two folders**, keep the folder structure intact when you upload. Don't rename anything — the Universe links to `terminal/` by that exact path.

### The fastest route (drag-and-drop, no command line)

1. **Sign in** at https://github.com (create a free account if needed).
2. Click **➕ → New repository** (top-right). Name it exactly **`your-username.github.io`** (e.g. `chineme-uba.github.io`) for the cleanest URL. Set it **Public** → **Create repository**.
3. On the empty repo page, click **uploading an existing file**.
4. **Drag the *contents* of this folder in** — that's `index.html`, the `terminal` folder (with its `index.html` inside), and optionally `README.md`. GitHub preserves the folder structure when you drag a folder in. Scroll down, click **Commit changes**.
   - *Tip:* if drag-and-drop flattens the folder, instead upload `index.html` first, commit, then use **Add file → Create new file**, type `terminal/index.html` as the name (the `/` creates the folder), paste the terminal's HTML, and commit.
5. Go to **Settings → Pages**. Source = **Deploy from a branch**, Branch = **main**, folder = **/ (root)** → **Save**.
6. Wait ~1 minute, refresh. Your site is live at **https://your-username.github.io** 🎉
   - The hidden terminal lives at `https://your-username.github.io/terminal/` — but let people *discover* it by typing `sudo`.

### If you prefer the command line (git)

```bash
# inside this folder:
git init
git add .
git commit -m "The Universe + CHINEME-OS"
git branch -M main
git remote add origin https://github.com/your-username/your-username.github.io.git
git push -u origin main
```
Then enable Pages as in step 5 above.

### Notes
- **Don't judge it by double-clicking `index.html` locally** — browsers block the 3D engine (and the `terminal/` link) over `file://`. It only works once served (GitHub Pages, or `python3 -m http.server` locally).
- **Updating later:** edit the file in GitHub (pencil icon) or re-upload; changes go live within a minute.
- **Custom domain** (optional, the only paid part): buy a domain (~$10/yr), add it under Settings → Pages, and point the DNS records GitHub shows you. HTTPS is free and automatic.

## Tech
three.js r170 (MIT, via jsDelivr CDN) · vanilla JS · no frameworks · no build tools · no trackers.
