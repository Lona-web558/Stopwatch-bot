# Stopwatch-bot

# Stopwatch Bot

A simple stopwatch web app that counts up to **20 minutes**, automatically restarts, and repeats for **5 rounds**. After round 5 it stops, and you press **Start** again to begin a new session.

Built with HTML5, CSS3, Bootstrap 5, and vanilla JavaScript. Single file, no build step.

## Features

- Counts up from `00:00` to `20:00` per round
- Auto-restarts each round, 5 rounds per session
- Beep at every round change and a longer beep when the session ends
- Start, Pause/Resume, and Reset buttons
- Progress bar and round indicators (1 to 5)
- Accurate timing using `performance.now()`, with no drift and no lost time between rounds
- Responsive layout with automatic light/dark mode

## Getting Started

1. Save the code as `index.html`.
2. Open it in any modern browser, or double-click the file.

No installation or dependencies are needed. Bootstrap loads from a CDN.

## Usage

| Button | Action |
| --- | --- |
| **Start** | Begins round 1 (or starts a new session after one finishes) |
| **Pause / Resume** | Pauses or continues the current round |
| **Reset** | Stops everything and returns to round 1 at `00:00` |

When round 5 hits 20:00, the timer stops and shows "All 5 rounds complete!". Press **Start** to run another session.

## Configuration

Edit these two values at the top of the `<script>` block in `index.html`:

```js
var LIMIT = 20 * 60 * 1000;   // length of each round (milliseconds)
var TOTAL = 5;                // number of rounds per session
```

For example, use `10 * 60 * 1000` for 10-minute rounds, or `TOTAL = 3` for 3 rounds. If you change `TOTAL`, also update the "5 rounds" text in the subtitle and the completion message.

## Deployment

Works on any static host:

- **Netlify**: drag and drop the folder containing `index.html`
- **Neocities**: upload `index.html` in the dashboard
- **Render**: create a Static Site and point it at your repo

## Browser Support

Any modern browser (Chrome, Edge, Firefox, Safari). Audio beeps require a user interaction first, which the Start button provides.

## Project Structure

```
stopwatch-bot/
├── index.html   # HTML, CSS, and JavaScript in one file
└── README.md
```

## License

Free to use and modify.
