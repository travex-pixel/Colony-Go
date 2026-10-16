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

## How to play

Drag from a creature to its matching home (same colour and the same little symbol). Paths cannot cross rocks, other creatures or other homes. Drawing over a friend's path cuts it short. Undo, reset and a hint are always available. Stars reward finishing with few redraws.
