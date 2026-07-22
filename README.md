# Kat's 10-Year Lyftiversary 🎉

A fun, interactive tribute site for Kat Murray's 10 years at Lyft. There are **two versions** of the same celebration:

| File | What it is | Live path |
|---|---|---|
| `index.html` | **"Lyft Wrapped"** style — a scrolling, Spotify-Wrapped-style recap | `/` |
| `playbill.html` | **"Playbill"** style — a page-flip theater program (the main one we're building) | `/playbill.html` |

They cross-link to each other (buttons top corner). Live site: https://spruhareddy.github.io/kat-lyftiversary/

---

## The Playbill pages (`playbill.html`)
It's a "flip book" — navigate with the ‹ › arrows, arrow keys, or swipe. Pages in order:
1. **Cover** — title + looping video portrait of Kat (`ohmurray.mp4`)
2. **About the production** — real tenure stats (employee #130, etc.)
3. **Acts & Scenes** — her story in 5 acts (2016 contractor → 2026)
4. **Accolades** — badge medallions + chip wall
5. **Tonight's tallies** — ride stats (1,416 lifetime rides)
6. **The Company** — the team / cast
7. **Featuring Nikki** — the cat
8. **Production stills** — photos
9. **Critics rave** — teammate quotes ⚠️ *placeholder text*
10. **Sponsor** — parody ad
11. **Curtain call** — finale + confetti

Each page is a `<section class="page">` in the HTML.

## Still TODO (placeholders to fill)
- **Critics rave** (page 9): real teammate quotes instead of `[bracketed]` placeholders
- **The Company** (page 6): real cast names instead of initials (`DR`, `JS`, …)
- Optional: real badge art for the 3 featured Accolades medallions (`images/badge-*.png`)

---

## How to preview
Just **double-click `playbill.html`** (or `index.html`) — it opens in your browser. No build step, no server needed. Refresh after edits. Hard-refresh (`Cmd+Shift+R`) if the video/font looks stale.

## How to edit
Open this folder in **Claude Code** and ask for changes — same as any project. It's plain HTML/CSS/JS in single files, so edits are self-contained.

---

## Working together (git)
We collaborate on the **`collab` branch**. `main` is the live site — we only merge to it when we're ready to publish.

**Every time you sit down to work:**
```bash
git checkout collab   # be on the collab branch
git pull              # download the latest changes
```

**When you're done with a change:**
```bash
git add -A
git commit -m "short note about what you changed"
git push              # upload to GitHub
```

Then the other person runs `git pull` to get it.

**Tip:** avoid both editing the exact same lines at once. If `git pull` shows a "merge conflict," don't panic — ask Claude Code to help resolve it.

## Publishing (going live)
When we're both happy and want the team to see it:
```bash
git checkout main
git merge collab
git push
```
GitHub Pages rebuilds `main` automatically (~1 min) and the live link updates.

---

## Files
```
index.html       → Wrapped version
playbill.html    → Playbill version (main build)
ohmurray.mp4     → cover video
images/          → photos (nikki, kat-panel, kat-hat, team-*, kat-child)
```
