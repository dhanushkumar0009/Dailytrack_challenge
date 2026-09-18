# 100 Days Challenge Tracker

A single-file web tracker for the 100 Days Challenge (19 Sep – 27 Dec 2026), with
separate progress for **Dhanush Kumar** and **Ramya Sree** across all 10 daily habits.

Everything — HTML, CSS, JavaScript — lives in `index.html`. No build step, no
dependencies, no server.

## Deploy on GitHub Pages

1. Create a new repository on GitHub (e.g. `100-days-tracker`), public.
2. Upload `index.html` to the repository root (**Add file → Upload files**).
3. Go to **Settings → Pages**.
4. Under *Build and deployment*, set **Source** = `Deploy from a branch`,
   **Branch** = `main`, folder = `/ (root)`. Save.
5. Wait ~1 minute. Your tracker is live at:
   `https://<your-username>.github.io/100-days-tracker/`

Add it to your phone's home screen for one-tap daily check-ins.

## Using it

- **Daily check-in** — tick ✓ or cross ✕ each habit for the day. Arrow keys (← →)
  move between days; *Mark all done* logs a perfect day in one click.
- **Full 100-day grid** — the whole tracker, 25 days at a time (or All). Click any
  box to cycle blank → tick → cross.
- **Backup & sync** — progress is saved in the browser's local storage, so it
  survives refreshes and redeploys but does not travel between devices. Use
  **Export JSON** on one device and **Import JSON** on another to move it.

Switch profiles with the Dhanush / Ramya toggle at the top right; each keeps its own
data. The ◐ button toggles light/dark.

## Customising

Open `index.html` and edit the config block near the top of the `<script>`:

```js
var START = new Date(2026, 8, 19);   // Day 1 (month is 0-based: 8 = September)
var DAYS  = 100;
var TASKS = [ "5 AM Wake-up", "LeetCode Streak", ... ];
var PROFILES = [ { id:"dhanush", name:"Dhanush Kumar", short:"Dhanush" }, ... ];
```

Changing `TASKS` order or `PROFILES` ids will orphan existing saved marks — export a
backup first if there's progress worth keeping.
