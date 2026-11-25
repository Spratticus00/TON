# TON

A hole-swallowing city arcade game. Steer a hole around a freshly generated toy city (dense downtown, suburbs, farms, an airport, industrial yards, parks and stadiums), swallow anything smaller than you, grow, and outscore six rival holes in 5 minutes.

Plain HTML, CSS and JavaScript with no build step and no dependencies. Works offline once it's installed.

## Put it on GitHub Pages

1. Create a new public repository on GitHub, for example `ton`.
2. Upload everything in this folder to the root of the repo: `index.html`, `manifest.json`, `sw.js`, `icons/` and this README. On github.com, use **Add file → Upload files** and drag them in.
3. Open **Settings → Pages**. Under "Build and deployment", set the source to **Deploy from a branch**, pick `main` and `/ (root)`, then save.
4. After a minute the game is live at `https://<your-username>.github.io/ton/`.

## Add it to your iPhone home screen

1. Open the Pages URL in **Safari**.
2. Tap **Share**, then **Add to Home Screen**, then **Add**.
3. Launch it from the icon. It runs full screen with no Safari bars, and works offline after the first launch.

## Coins, power-ups and skins

- Coins and power-ups are Classic-only; Totality has neither.
- Gold coins (1) and purple gems (5) are scattered around the city. Roll over them to collect. They grow back over time, and your total is saved on the device.
- Spend coins mid-round on the buttons at the bottom:
  - **Speed:** +5% speed per level, up to 6 levels. Costs 8, 12, 16 and up.
  - **Vacuum:** +12% pull range per level, up to 5 levels. Costs 10, 15, 20 and up.
  - **Repopulate:** instantly regrows everything that's been eaten (not coins). Costs 50, then 80, 110 and up within a round.
- Upgrades last for that round only.
- Rival bots collect coins too and buy a few Speed and Vacuum levels (at most 3 and 2). They never use Repopulate.
- All the original colors and skins are free. 14 more skins can be unlocked in **Customize** for 40 to 300 coins.

## Updating

Edit the files and push. Because the service worker is network-first, the installed app picks up the new version the next time it opens online. If you change the list of files, bump `CACHE` in `sw.js` (for example to `ton-v2`).

## How to play

**Classic:** 5 minutes, highest score wins.

**Totality:** one life and no clock. Every bite gives a ridiculous size boost. The round ends when you've swallowed the whole map (a strong run takes about 1:50) or when a bigger hole swallows you. Your fastest Totality time is saved.


- Drag anywhere to steer. The joystick appears where your finger lands. On a computer you can also use WASD or the arrow keys.
- You can swallow an object once it's smaller than about 85% of your hole's size. Go from people and cones to cars, houses, shops and towers, then work up to the landmarks: Ferris wheels, skyscrapers and stadiums.
- Consumed things slowly grow back, 35-60 seconds later and only where nobody is looking, so you can't camp one spot.
- Tap **Customize** on the menu to pick a name, a color and a skin: Classic, Rainbow, Donut, Pizza, Cookie, Lava, Chomper, Googly, Toilet or Galaxy. Your choice is saved on the device.
- Holes 20% bigger than another hole can swallow it, and get a huge size boost for it. A consumed hole respawns smaller, and blinks while it's safe.
- The highest score after 5:00 wins. Your best score is saved on the device.
