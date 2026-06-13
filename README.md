# Midnight Mini Golf

A neon, midnight-island themed mini golf game that runs entirely in the
browser — no install, no account, works on desktop and mobile (touch).
Live at **[akarev-maker.github.io](https://akarev-maker.github.io)**.

## Play

- **Landing page:** `index.html`
- **Game:** `game/golf.html`

Drag back **from the ball** to aim (slingshot) — the further you pull, the
more power, with the aim line shifting green → yellow → red. Release to shoot.
Sink the ball in as few strokes as possible across **18 holes**.

From the title screen, **Start** opens the hole-select screen:

- **Play All 18** — a full round (1 → 18) with a complete scorecard.
- **Any hole** — single-hole practice; the scorecard shows just that hole.

## Features

- 18 hand-designed holes (two nines) with rising difficulty — pars 2 to 6
- Obstacles: walls/bumpers, sand traps, slope zones, windmills, moving gates
- Slingshot aiming with a power meter and star ratings per hole
- Full mouse **and** touch support; the board auto-scales to fit any screen
- Animated neon starfield + a live game preview on the landing page

## Project structure

```
.
├── index.html          # Landing page (self-contained: HTML/CSS/JS)
├── game/
│   └── golf.html       # The game (self-contained: HTML/CSS/JS)
├── css/
│   └── style.css       # Shared design tokens (scaffolding for future use)
├── assets/
│   ├── icons/          # favicon.svg
│   └── sounds/         # (reserved for future sound effects)
├── CNAME               # Custom domain config for GitHub Pages
└── README.md
```

Both `index.html` and `game/golf.html` are intentionally **single-file**:
their CSS and JavaScript are inline so each page is fully portable and has
zero build step. The `css/` and `assets/sounds/` folders are scaffolding for
features that haven't been added yet.

## Running locally

It's all static files — open `index.html` directly, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

Hosted on GitHub Pages from the `main` branch; pushes deploy automatically.
The `CNAME` file points the custom domain at the Pages site.
