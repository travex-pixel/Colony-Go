# Mochi Colony

A cosy, hand-painted path puzzle. Guide the little forest spirits home by drawing routes across a storybook board.

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

52 levels across six areas, plus a fresh daily puzzle with a streak counter.

## The garden

Friends you meet move into the garden on the home screen. Tap a friend to pet them, hold for a cuddle, or tap the
grass to call one over. Every new star earns an acorn: drag one from the basket onto a friend, or tap the basket to
toss one into the grass. Well-fed, well-loved friends do a happy dance. Hungry ones show a little acorn bubble.

## Releasing an update

Bump the `app-version` meta tag in `index.html` with every deploy. Open copies of the game check it in the
background and refresh themselves between levels when a newer build is live.
