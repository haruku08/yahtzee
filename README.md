# Yatzy Scorecard

A Material 3 Yatzy scorecard for the dice you roll at the table.

- **Live game:** start a game, share the 4-letter code (or the link with `#CODE` on the end), and every phone sees scores update live. No sign-in needed.
- **Classic scorecard:** one device, everyone on one sheet. Saved on that device.
- **TV view:** a big read-only scoreboard for casting to a TV (Chrome → ⋮ → Cast → Cast tab).

Scoring: tap a box and pick the points. Ones–Sixes pick how many dice, 3/4 of a kind pick the number (3× / 4× that number, Scandinavian Yatzy style), Full house 25, Small straight 30, Large straight 40, Yahtzee 50, Chance 5–30. The upper bonus (+35 at 63) and Yahtzee bonuses (+100 each) are added automatically.

## How it's built

A single static page (`index.html`) with no build step. Live games sync through Supabase (tables `yatzy_games` and `yatzy_players`, plus the `yatzy_set_score` function) using the public publishable key. `vendor/` holds the Supabase JS browser build so the page doesn't depend on a CDN.

Hosted with GitHub Pages from the `main` branch.
