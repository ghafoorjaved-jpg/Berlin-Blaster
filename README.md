# Berlin Word Blaster

Learn German by shooting the right balloon. Pang-style bouncing balloons, A1–C2 vocabulary (600 stages), articles (der / die / das), and spoken German on a hit.

Stage 1 background: Neuschwanstein.

## Play

Open `index.html` in a browser, or use any static host.

```bash
# preview locally
python3 -m http.server 8080
# then visit http://localhost:8080
```

### Controls

- Swipe on the player to move left / right
- Double-tap the player to fire
- Keyboard: A/D or arrows to move, Space to fire

## GitHub

1. Create a new repository (example name: `berlin-word-blaster`).
2. Upload this folder (or `git init`, add remote, push).

```bash
git init
git add .
git commit -m "Initial Berlin Word Blaster release"
git branch -M main
git remote add origin https://github.com/YOUR_USER/berlin-word-blaster.git
git push -u origin main
```

### GitHub Pages

Repo **Settings → Pages → Deploy from branch `main` / root**.  
The game will be at `https://YOUR_USER.github.io/berlin-word-blaster/`.

## Google Play

This is a web game. Play Store needs an Android App Bundle (`.aab`).

See [docs/PLAY_STORE.md](docs/PLAY_STORE.md) for a step-by-step wrapper using [Bubblewrap](https://github.com/GoogleChromeLabs/bubblewrap) (Trusted Web Activity).

You will still need:

- A Google Play Developer account
- A privacy policy URL (use `docs/PRIVACY.md` on GitHub Pages)
- Screenshots from a phone
- A signing key

## License

MIT — see `LICENSE`.
