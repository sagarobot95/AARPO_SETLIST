# AARPO ★ SET LIST

A retro, 80s Sega-arcade themed web app for the AARPO band's set list and chords.

## Use it
Just **double-click `index.html`** — it opens in your default browser. No install, no server, works offline (all songs are embedded in the file as a fallback).

## Flow
1. **Select your player** — the roster (names + roles) comes from the PLAYER/ROLE table at the bottom of the LEGEND sheet. Roles set each player's instrument icon; drums/percussion get a no-chords structure view.
2. **Select a track** — songs are numbered in the sheet's tab order (🎯 marks tracks where your part is written).
3. **Play** — the whole song fits on one screen (no scrolling) in three columns:
   **LINE · CHORDS · YOUR PART**. Auto-fits font/columns; `A+`/`A−` or `+`/`−` to resize, `Esc` to go back. **FIT/SCROLL** toggles single-page vs scrollable. **♭/♯** transpose the chords.

## Key, tempo, tone & metronome
The LEGEND sheet supplies each song's **Key**, **Tempo (BPM)** and per-player **tone/preset**, shown as badges on the song screen. A built-in **metronome** runs at the song's BPM — start/stop, fine-tune speed (local only, never written back to the sheet), pick a click sound, and adjust volume.

## Live sync (Google Sheets)
Tap **⟳ SYNC FROM SHEETS** (track screen) or the **⟳** in the song bar to pull the latest from the linked Google Sheet via the Sheets API. Re-ordering tabs, adding new song tabs, and adding player columns are all picked up automatically. The last sync is cached in the browser so it persists offline; if a sync fails it falls back to the saved/built-in copy.

The sheet must stay shared as **Anyone with the link → Viewer**.

## Files
- `index.html` — the app (self-contained, data + sync engine baked in).
- `AARPO CHORDS STRUCTURE.xlsx` — original source spreadsheet snapshot.
