GAMBLE.IO MASTER BUILD

This master build is intentionally ONE FILE: index.html. Replace your old index.html with it. Do not use the prior app.js, style.css, or firebase-config.js files: this version contains its own styles, JavaScript, and Firebase configuration so the earlier module-export failure cannot happen.

DEPLOY
1. Upload index.html to the ROOT of your GitHub Pages repository (same location that GitHub Pages serves).
2. Commit it. Wait until GitHub Pages completes deployment.
3. Open your site and hard-refresh Ctrl+Shift+R.
4. Click Play as guest to confirm games work immediately.

FIREBASE
The provided Firebase config is already embedded. In Firebase Console enable Authentication > Sign-in method > Google. Add tommysartors31.github.io under Authentication > Settings > Authorized domains. Create Firestore Database, then publish firestore.rules.

GAME TESTS INCLUDED
Dice conditions do not overlap: Low 1–2, Exact only 3, High 4–6. Blackjack handles ace reduction, dealer 17 stand, push, bust and natural blackjack. Horse race chooses exactly one winner. Each wager is a positive whole number no higher than current chips.

The site remains virtual-chip only; chips have no cash or exchange value.
