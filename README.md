# Space Dodger

Samuel's first space-themed vertical-scrolling game.

## First playable version

- Steer the ship with the arrow keys (WASD also works).
- Press **P** or **Escape**, or use the on-screen button, to pause and resume. The game and its timers freeze while paused; switching away from the browser tab also pauses it.
- Dodge falling asteroids. The game gets faster and busier over time.
- Start with five lives. A collision costs one life and gives the ship two seconds of flashing collision protection; the asteroid bursts on impact.
- When the final life is lost, the ship explodes before the game-over screen appears.
- Collect gold coins for bonus points.
- Collect a green shield for 20 seconds of invincibility, with a visible countdown.
- Type **GODMODE** during a run for 100× points and invincibility until that run ends.
- See your final score and coins when the game ends, then play again.
- Your best score is saved in this browser.

## Play

- [Production game](https://jaredchurch.github.io/space-dodger/)
- [UAT candidate](https://jaredchurch.github.io/space-dodger/uat/)
- [Version history](https://jaredchurch.github.io/space-dodger/versions/)

## Run locally

Open `site/index.html` in a modern web browser. No build tools or dependencies are required.

## Branch and release process

- `uat` is the candidate/testing branch. Every push to `uat` automatically publishes the candidate at `/uat/`.
- `main` is the production branch. Merge a pull request from `uat` into `main` to release; the merge automatically triggers the production deployment.
- Every production release is assigned a sequential whole-number version (`v1`, `v2`, `v3`, ...).
- Each release remains playable at `/versions/vN/`. The version-history page links to all retained releases.
- The existing live game is retained as `v1` when the archive mechanism is first initialised.
- Deployments assemble the production root, current UAT candidate and all release archives into one complete GitHub Pages artifact. Publishing one environment must not overwrite the others.
- The build is dispatched to a publisher workflow on `main` so the GitHub Pages deployment runs from the Pages-authorised branch; the publisher re-registers the complete artifact before deployment.
- To roll back, open a pull request from the desired historical release source into `main` following the repository's release procedure; do not delete or overwrite the archived version.

The workflow is `.github/workflows/deploy-pages.yml`. GitHub Actions uses Node 24-compatible action versions.

## Next ideas

- **Ship upgrades:** Add upgrades to the player's ship in a later iteration, with Samuel helping choose and build the features.
- **Additional hazards:** Introduce enemy ships and other space hazards that the player must dodge.
- **Game music and sound effects:** Add background music and sound effects for key game events, such as collecting coins, activating power-ups, collisions and losing a life. Include simple controls to mute or adjust the audio.
