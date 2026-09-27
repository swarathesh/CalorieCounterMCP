# Steady — fitness journal

A responsive fitness tracker with a four-day lifting plan, two rest days, daily weight / calorie / protein / step / sleep / waist logging, exercise set tracking, progress charts and editable targets.

## Use

Open `index.html` in a modern browser, or host the repository root on any static website host. No build, dependencies, account or API key is required.

Entries are saved automatically in this browser's local storage. **Clearing site data, switching origins or switching browsers does not preserve or sync entries.** Use **Backup & restore → Download .txt backup** regularly. The file contains a readable journal plus JSON used for restoration. Import it to move your records to another browser. On import, existing dates are preserved unless the replacement checkbox is selected.

The application makes no requests to upload journal entries. The repository contains application code and default targets, not your ongoing health logs.

## GitHub Pages

The GitHub mirror keeps the self-contained app at `index.html`. In repository **Settings → Pages**, select **Deploy from a branch**, branch **main**, folder **/ (root)**, then save. No Actions workflow or server is needed. The source can also be served by the live link provided in the project handoff.

## Starting plan

- 2,300 kcal and 170 g protein daily; editable in My plan.
- Monday Upper A, Tuesday Lower A, Thursday Upper B, Friday Lower B.
- Saturday brisk walking; Wednesday and Sunday rest.
- 10,000 steps on active days, flexible 5,000 on rest days.
- 90 kg starting point and 85 kg first checkpoint; these are goals, not fabricated journal entries.

Calorie targets are estimates. This plan assumes gym access and no limiting injury. Review several weeks of weight trends and recovery before adjusting targets.

## Implementation

One self-contained HTML file, including CSS and JavaScript. Text imports are validated before any mutation. User notes are escaped when rendered. Weight averages use logged measurements in the trailing seven calendar days; missing data is not treated as zero. The browser's local calendar date is used. Unsupported or failed local storage is reported visibly; export remains available. An optional feature-detected WebMCP interface exposes journal reads and validated batched check-ins in supporting browsers.
