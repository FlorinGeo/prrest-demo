# PRREST - live demo link

Two files. Publish this folder as its own GitHub repository with Pages serving
from the root, and the address it gives you never changes again.

    Settings -> Pages -> Source: Deploy from a branch -> main -> / (root)

`live.json` holds the address of the tunnel that is currently running. The demo
itself runs on a laptop behind a temporary Cloudflare tunnel whose hostname is
random and changes every restart, so this page is the part that stays put: it
reads `live.json`, checks whether the machine is actually answering, and either
forwards visitors or tells them plainly that the demo is offline.

`npm run demo` in the main project rewrites `live.json` every time the tunnel
comes up. Add `--publish` and it commits and pushes it here for you.

Nothing in this folder discloses anything about the system: an address, a
timestamp, and a description.
