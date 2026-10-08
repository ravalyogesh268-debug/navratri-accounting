# 🌺 Navratri 2026 — One Link Firebase + GitHub Pages

આ versionમાં **Public Dashboard અને Admin Login એક જ `index.html` link પર છે.** અલગ `admin.html` link share કરવાની જરૂર નથી.

## Features
- 🌺 Public Dashboard
- 🔐 એ જ page પર Admin Login tab
- 📱 Mobile friendly
- 💰 Live income / expense / balance
- 📊 Daily / payment / expense charts
- 🧾 CSV report
- 🔎 Public + Admin record search
- ✏️ Admin Edit
- 🗑️ Admin Delete
- ➕ Admin Entry
- ⚙️ Festival settings
- 🌙 Dark Mode
- 🔥 Firebase Authentication + Firestore
- 🚀 GitHub Pages

## Firebase setup
1. Firebase project બનાવો.
2. Authentication → Sign-in method → Email/Password Enable કરો.
3. Firestore Database બનાવો.
4. Authentication → Users → Add userથી admin email/password બનાવો.
5. તે userનું UID copy કરો.
6. Firestoreમાં `admins` collection બનાવો અને document ID તરીકે UID મૂકો. Example fields: `role: admin`, `email: your@email.com`.
7. `firestore.rules` publish કરો.
8. `firebase-config.js`માં Firebase Web App config મૂકો.

## Firestore rules
Public read કરી શકે છે. માત્ર `admins/{uid}` ધરાવતો authenticated user create/update/delete કરી શકે છે.

## GitHub Pages
Repository rootમાં `index.html`, `one-link-app.js`, `firebase.js`, `firebase-config.js`, `styles.css` અને `firestore.rules` રાખો.
Settings → Pages → Deploy from branch → `main` → `/root`.

તમારી GitHub Pagesની **એક જ link** public અને admin બંને માટે છે. Link ખોલીને `🔐 Admin Login` tab દબાવો.
