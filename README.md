# School Portal — Next.js + Firebase (Netlify-ready)

This project is a scaffold for a school portal using **Next.js** on the frontend and **Firebase** (Auth + Firestore) as the backend, designed to be deployed on **Netlify** (frontend) with no server required.

## Quick setup (local)

1. Install dependencies:
```bash
npm install
```

2. Add Firebase config (see `firebase/clientApp.js`) — replace with your Firebase project's values or set environment variables.

3. Run development server:
```bash
npm run dev
```

4. Build for production:
```bash
npm run build
npm run export
```

The static export will be generated in the `out/` folder (Netlify publish directory).

## Deploy to Netlify

1. Create a Netlify site (https://app.netlify.com/sites/new).
2. Connect your GitHub repo or use drag-and-drop of the `out/` folder (after `npm run export`).
3. Set environment variables in Netlify (if you prefer to use them) — see `.env.example`

## Firebase setup

1. Create a Firebase project at https://console.firebase.google.com/
2. Enable **Authentication** (Email/Password) and **Firestore Database**.
3. Copy config values into `firebase/clientApp.js` or set as environment variables (recommended).
4. For security rules, lock down writes to authorized admins — this scaffold uses Firestore calls from client side, so add rules to restrict access.

## Files added
- pages/ (Next.js pages)
- components/ThemeEditor.jsx — premium drag-and-drop theme editor
- firebase/ — client initialization and helpers
- styles globals, README, and deployment instructions

---
