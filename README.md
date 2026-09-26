# 🧚 Fairy Delivery

A cozy pixel-art runner game inspired by the Chrome "no internet" dino game. You play a little fairy carrying treasures home to the fairy village, jumping over mushrooms, snails, frogs and thorny roses along the way.

- **One button:** the space bar is the only control.
- **Kid-friendly:** the levels don't get harder, and you can slow the whole game down.
- **No install:** it's a single HTML file with no build step and no dependencies.
- **8-bit music and sound:** everything is generated in code with the Web Audio API.

## Download

**Option 1: clone with git**

```bash
git clone https://github.com/jamesdayhuff/fairy-delivery.git
```

**Option 2: download a ZIP**

On the GitHub page, click **Code → Download ZIP**, then unzip it anywhere.

## Install

Nothing to install. You only need a modern web browser (Chrome, Edge, Firefox or Safari).

## Run

**Easiest:** double-click `index.html` to open it in your browser.

**Or serve it locally**, which is useful if your browser blocks saving settings for local files:

```bash
cd fairy-delivery
python3 -m http.server 8000
```

Then visit <http://localhost:8000>.

> The pixel font loads from Google Fonts. Offline, the game still works and falls back to a standard monospace font.

## How to play

| Action | Space bar |
|---|---|
| Move to the next menu option | **Tap** |
| Select an option | **Hold** (about half a second; a bar fills up) |
| Jump | **Tap**, or **hold** for a higher jump in Dino mode |

### Game modes

- **Normal:** deliver three treasures across three levels. Reach the village at the end of each level to make your delivery. Hitting an obstacle only restarts the current level.
- **Endless:** run for as long as you can on a random level and chase your high score.

### Levels

| Level | Treasure | Obstacles |
|---|---|---|
| Mossy Meadow | Acorn | mushrooms, pebbles, tall grass |
| Honey Garden | Honey Jar | thistles, snails, flowers |
| Twilight Glade | Moonstone | thorny roses, frogs, crystals |

### Settings

| Setting | Options |
|---|---|
| Jump | **Dino** (hold to jump higher) or **Double** (press again mid-air to flutter) |
| Speed | **0.5x**, **1x** (default) or **1.5x**. At 0.5x, levels are shorter so they still take about 37 seconds. |
| Sound | Sound effects on or off |
| Music | Background music on or off |

Settings and the Endless high score are saved in your browser's `localStorage`.

## Customizing

Everything lives in `index.html`, organized into numbered sections:

| Section | What you can change |
|---|---|
| 1. Config | Speed, gravity, jump strength, level length, obstacle spacing |
| 2. Sprites | Pixel art, drawn as text grids where each character maps to a palette color |
| 3. Levels | Level names, treasures, colors, scenery and obstacles |
| 5. Audio | Sound effects |
| 5b. Music | Songs, written as note lists like `E5:2 G5:2 C6:4` (note:length in 16th notes, `r` for rest) |

**Tip:** add `?short` to the URL (for example `http://localhost:8000/?short`) to make levels very short while testing.

## Contributing

Contributions are welcome! Ideas include new levels, new songs, touch controls or accessibility improvements.

1. Fork the repo and create a branch.
2. Make your changes and test them in a browser.
3. Open a pull request describing what you changed.

Please keep the game dependency-free and playable with just the space bar.

## License

[MIT](LICENSE). Free to use, modify and share.
