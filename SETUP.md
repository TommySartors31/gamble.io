# Gamble.io Deluxe — setup

## Upload to GitHub Pages
1. Create a new GitHub repository.
2. Upload all project files to its root.
3. In **Settings → Pages**, choose **Deploy from a branch**, then select `main` and `/(root)`.
4. Wait for Pages to deploy and open the generated site address.

## Connect Firebase
1. Create a project at Firebase Console.
2. Add a **Web app** and copy its config object.
3. Paste values into `firebase-config.js`.
4. Enable **Authentication → Google** and **Anonymous** sign-in.
5. Add your `YOURNAME.github.io` domain in Authentication → Settings → Authorized domains.
6. Create a Firestore database.
7. In Firestore → Rules, publish the contents of `firestore.rules`.

## Built-in codes
- `JACKPOT1000`: adds 1,000 virtual chips once to a signed-in player profile.
- `devperms54321`: enables a **local browser developer flag**. It is intentionally not a secure administrative system and does not grant Firebase server privileges, ban users, alter other user data, or bypass Firestore rules.

## Notes
- This project is a virtual-chip game only. Do not add buying, cashing out, or exchanging chips for real value without suitable professional legal/compliance guidance.
- The code is written for a simple static GitHub Pages project. Do not place service-account keys or Firebase Admin SDK keys in this repository.
- The active theme is saved in the profile. The current visual build changes the site accent immediately; expand `shop()` for full per-theme background/layout variants.

## Test checklist
1. Guest entry: opens doors, plays 3D casino tour, shows a 20-game lobby.
2. Signed-in entry: receives 10,000 chips on first profile creation.
3. Dice: low = 1–2, exact = 3, high = 4–6; no overlapping win logic.
4. Blackjack: dealer stands on 17, aces adjust, push gives wager back.
5. Horse Races: one randomly selected winner per race.
6. Slots: reels animate before final payout.
7. Plinko: chip animates into a random lane.
8. Use `JACKPOT1000` twice; the second use should be blocked.
