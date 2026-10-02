# Node Hunger (web build)

The web export of **Node Hunger**, an Agar.io-style multiplayer browser game, as deployed on Vercel.

**Play it:** https://nodehunger.bugblazer.dev

![Node Hunger in game](docs/in-game.png)

This repository only holds the exported files. The source lives elsewhere:

- [nodeHunger](https://github.com/bugblazer/nodeHunger): the Godot 4.5 client source (`client/`).
- [node-hunger-server](https://github.com/bugblazer/node-hunger-server): the Go game server, with the
  full description of the game and how it works.

## What's here

- `index.html`, `index.js`, `index.wasm`, `index.pck`: the Godot web export.
- `loading-screen.html` and `wake-notice.html`: the custom loading screen and the "waking up the
  game server" notice. Both are pasted into the export preset's Head Include, so every export
  carries them.
- `vercel.json`: sets the `Cross-Origin-Opener-Policy` and `Cross-Origin-Embedder-Policy` headers
  the Godot web build needs.

## Updating it

Export from the Godot project with the "Web" preset straight into this folder, then commit and push.
Vercel deploys on every push to `main`.

Built by [bugblazer](https://bugblazer.dev).
