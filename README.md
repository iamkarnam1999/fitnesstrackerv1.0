# 💪 Fitness Coach Dashboard

Personal fitness tracking dashboard with progressive overload, food logging, weight tracking, and no-junk streak tracker.

## Features

- **Workout Tracker** — Full weekly plan with set-by-set checkboxes, weight inputs, and target reps
- **Progressive Overload** — 3-week double progression cycle (8→10→12 reps, then +5 lbs)
- **Food Log** — Daily meal tracking with calories, protein, carbs, fat
- **Weight Tracker** — Morning weigh-in log with progress bar toward goal (100 kg by Aug 2026)
- **No-Junk Streak** — 14-day clean eating calendar with streak counter
- **Session Notes** — Log how workouts felt, energy, PRs

## Weekly Schedule

| Day | Session | Core |
|-----|---------|------|
| Sunday | Push — Chest · Shoulders · Triceps | ✅ |
| Monday | Pull — Back · Biceps | ✗ |
| Tuesday | Legs — Hamstring Focus | ✅ |
| Wednesday | Cardio — 25 min brisk walk | ✗ |
| Thursday | Upper Body — Full | ✅ |
| Friday | Legs — Quad Focus | ✗ |
| Saturday | Complete Rest | ✗ |

## Progressive Overload — Double Progression

| Week | Top Set | Back-off Sets (×2) |
|------|---------|---------------------|
| Week 1 | 8 reps | 10 reps |
| Week 2 | 10 reps | 12 reps |
| Week 3 | 12 reps | 15 reps |
| Week 4 | Reset + **+5 lbs** on all compounds | 8 reps again |

## How to Host on GitHub Pages

1. Create a new GitHub repository (e.g. `fitness-dashboard`)
2. Upload `index.html` to the repository
3. Go to **Settings → Pages**
4. Under **Source**, select `main` branch and `/ (root)` folder
5. Click **Save**
6. Your dashboard will be live at `https://yourusername.github.io/fitness-dashboard`

## Data Storage

All data is saved in your browser's **localStorage**. This means:
- ✅ Data persists across sessions on the same browser
- ✅ Works offline
- ✅ No account or backend needed
- ⚠️ Data is browser-specific — clearing browser data will erase it
- ⚠️ Does not sync across devices

**Tip:** Use the same browser on the same device every time for consistent data.

## Backup Your Data

To back up your data, open browser DevTools (F12) → Console, and run:
```js
console.log(JSON.stringify(localStorage.getItem('coach-fitness-v1')));
```
Copy the output and save it somewhere safe.

To restore, run:
```js
localStorage.setItem('coach-fitness-v1', '<paste your backup here>');
location.reload();
```
