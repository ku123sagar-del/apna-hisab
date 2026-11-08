APNA HISAB — setup (Firebase)

1) Firebase Console > Authentication > Sign-in method > enable Email/Password.
2) Firestore Database > Rules: paste firestore.rules and click Publish.
3) Save index.html and open it using a local web server OR deploy it to Firebase Hosting.
4) For Firebase Hosting, easiest route is Firebase CLI:
   npm install -g firebase-tools
   firebase login
   firebase init hosting
   - choose existing project: kisan-market-40083
   - public directory: current folder containing index.html
   - configure as single-page app: No
   - overwrite index.html: No
   firebase deploy --only hosting

Important:
- The Firebase web config (including apiKey) is a public client identifier, not a password.
- Firestore rules above restrict each user's entries to their own authenticated UID.
- For two phones to see the same records, sign in with the same account on both phones.
- If both people need separate logins with shared household data, add household membership/invitation logic before using separate accounts.
- The ₹2,100 rent is added only when you tap “Paid”; this page does not send push notifications or automatically charge rent.
- Keep downloaded CSV/JSON backups somewhere safe.
