# Mochi Colony

A cosy, hand-painted puzzle game with two modes that share one garden:

- **Paths:** guide the little forest spirits home by drawing routes across a storybook board.
- **Nibbles:** tap hungry animals to nibble the plain sponge off a cake, leaving only the iced picture.

## Run it

Everything lives in a single file, `index.html`, with no build step and no network dependencies.

- Open `index.html` directly in a browser, or
- serve the folder for a phone on the same network:

```
python3 -m http.server 8080
# then open http://<your-computer-ip>:8080/
```

For GitHub Pages, publish the repository root. `preview.png` and `icon.png` are the link preview and app icon
referenced from the page's meta tags.

## How to play

Drag from a creature to its matching home. Every home wears a little portrait of who lives there, and tapping a
creature makes its home glow. Paths cannot cross rocks or logs, other creatures or other homes. Drawing over a
friend's path cuts it short. Undo, reset and a hint are always available.

- 1 star: everyone is home.
- 2 stars: with only a couple of redraws.
- 3 stars: a perfect garden, every tile covered (from level 7 onwards).

82 levels across eight areas, plus a fresh daily puzzle with a streak counter.

## Nibbles

Each animal sits beside the cake with a little sign showing the shape it nibbles. Tap an animal and it walks in
along its row or column to the first piece of cake, then nibbles its shape there. Each animal nibbles once, and
a nibble that would touch the icing is refused. Hold an animal to peek at what it would nibble.

| Animal | Nibbles |
|---|---|
| Mouse | One crumb |
| Bunny | Three in a row |
| Duckling | Three side by side |
| Hedgehog | A little square |
| Squirrel | An L shape |
| Frog | Two with a hop between |
| Kitten | A zigzag |
| Fox | A plus |
| Bear | A big block |

24 cakes across three bakeries. Stars count spoiled tries and undos, and every new star earns an acorn.

## The garden

Friends you meet move into the garden on the home screen. Tap a friend to pet them, hold for a cuddle, or tap the
grass to call one over. Every new star earns an acorn: drag one from the basket onto a friend, or tap the basket to
toss one into the grass. Well-fed, well-loved friends do a happy dance. Hungry ones show a little acorn bubble.

## Choosing what the site shows

`classic/` holds a frozen copy of the original game from before the Nibbles mode. Edit `MAIN` in `site.config`
to choose which version appears at the main address:

- `MAIN=combined` shows the current game with both modes.
- `MAIN=classic` shows the frozen original.

Both are always reachable as well, at `<site>/new/` and `<site>/classic/`. Publishing runs from
`.github/workflows/pages.yml` on pushes to the default branch. It needs a one-time setting:
**Settings > Pages > Build and deployment > Source: GitHub Actions**.

## Releasing an update

Bump the `app-version` meta tag in `index.html` with every deploy. Open copies of the game check it in the
background and refresh themselves between levels when a newer build is live.
