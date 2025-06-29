
📦 Firebase Storage: Public Installer Hosting

You can host your generated install files (.apk, .exe, .dmg, .AppImage) in Firebase Storage and share direct download links.

---

🔧 1. Upload Files via Firebase CLI
Run the following in terminal:

firebase login
firebase init storage
firebase deploy --only storage

Then manually upload to `storage/app/releases/` in the Firebase Console or using:

firebase storage:upload path/to/CollabApp.apk --path /app/releases/CollabApp.apk
firebase storage:upload path/to/CollabApp.dmg --path /app/releases/CollabApp.dmg
firebase storage:upload path/to/CollabApp.exe --path /app/releases/CollabApp.exe

---

🌍 2. Public File URLs (after uploading)

You will be able to share URLs like:

https://firebasestorage.googleapis.com/v0/b/YOUR_PROJECT_ID.appspot.com/o/app%2Freleases%2FCollabApp.apk?alt=media

---

✅ Enable CORS or public read permissions from Firebase console if required.

Then share your links in newsletters, web landing page, or emails to users.
