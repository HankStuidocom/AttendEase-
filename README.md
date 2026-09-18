# AttendEase

AttendEase is a mobile-first attendance manager for students. It helps track daily attendance, calculate safe bunk counts, plan timetables, manage leaves, view reports, and sync data with Firebase.

## Features

- Dashboard with overall attendance, subject health, streaks, and today's timetable
- Mark attendance as present, absent, or skipped
- Bunk calculator with per-subject targets and semester forecasting
- Weekly timetable builder with share/import support
- Leave manager and attendance reports
- Local notifications, haptics, and Capacitor Android support
- Firebase authentication and cloud sync
- Premium/trial plan handling with payment flow hooks
- Biometric app lock on native devices

## Tech Stack

- React 19
- Vite 8
- Firebase Auth and Firestore
- Capacitor 8 for Android/native integrations
- ESLint 9

## Getting Started

Install dependencies:

```bash
npm install
```

Create a `.env` file with your Firebase values:

```bash
VITE_FIREBASE_API_KEY=
VITE_FIREBASE_AUTH_DOMAIN=
VITE_FIREBASE_PROJECT_ID=
VITE_FIREBASE_STORAGE_BUCKET=
VITE_FIREBASE_MESSAGING_SENDER_ID=
VITE_FIREBASE_APP_ID=
```

Run the app locally:

```bash
npm run dev
```

Build for production:

```bash
npm run build
```

Run lint checks:

```bash
npm run lint
```

## Android

After building the web app, sync Capacitor:

```bash
npx cap sync android
```

Then open or build the Android project from the `android` folder.

## Notes

- Do not commit real `.env` secrets.
- Firebase security rules should restrict user data by authenticated UID.
- Payment success should be verified by a trusted backend/webhook before granting premium access.
