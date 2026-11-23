# Space Dodger

Samuel's first space-themed vertical-scrolling game.

## First playable version

- Steer the ship with the arrow keys (WASD also works).
- Dodge falling asteroids. The game gets faster and busier over time.
- Start with five lives. A collision costs one life and gives the ship two seconds of flashing collision protection.
- Collect gold coins for bonus points.
- Collect a green shield for 20 seconds of invincibility.
- See your final score and coins when the game ends, then play again.
- Your best score is saved in this browser.

## Play

[Play Space Dodger](https://jaredchurch.github.io/space-dodger/)

## Run locally

Open `site/index.html` in a modern web browser. No build tools or dependencies are required.

## Deployment

Every push to `main` deploys the contents of `site/` to GitHub Pages using `.github/workflows/deploy-pages.yml`.

## Next ideas

- **Version history requirement:** Every released version of Space Dodger must remain available on the site. The approach for retaining and accessing previous releases is not yet decided; leave the implementation design for a later discussion.
- **Ship upgrades:** Add upgrades to the player's ship in a later iteration, with Samuel helping choose and build the features.
- **Cheat code:** Add a cheat code in a later iteration; its effect and activation sequence are still to be decided.
- **Coin magnet power-up:** Add a temporary power-up that attracts nearby coins towards the player's ship, making them easier to collect.
- **Asteroid-to-coin power-up:** Add a power-up that temporarily turns asteroids into coins for a fixed period.
- **Occasional high-value coins:** Introduce special coins that appear occasionally and are worth more points than regular coins.
