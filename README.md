# Andromeda Game Collection

This repository contains various small games.

## Maze Mouse Game

Navigate a mouse through a 3D maze in a first-person view. A timer tracks how long it takes to escape the maze.

### Running Locally

The game needs to be served over HTTP so the JavaScript modules load correctly. Run a simple server from the `maze-game` directory:

```bash
cd maze-game
python3 -m http.server
```

Then open <http://localhost:8000/> in your browser.

The required `three.js` files are included in `maze-game/js/`, so no network access is needed.

Open `maze-game/index.html` in a modern web browser (via the local server) to play.

### Deploying to Firebase Hosting

1. Install the Firebase CLI if you haven't already:

```bash
npm install -g firebase-tools
```

2. Initialize Firebase in this repository and select **Hosting** (you can accept the defaults and set the public directory to `maze-game`).

```bash
firebase init
```

3. Deploy the game:

```bash
firebase deploy
```

This publishes the `maze-game` directory to Firebase Hosting, so you can access the game via your Firebase project's URL.

