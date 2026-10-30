# Student Portal — Two-page demo

A React/Vite mobile-first recreation of the supplied school portal dashboard and Apply Leave screen.

## Local development

Requires Node.js 22 or newer.

```bash
npm install
npm run dev
```

Open the localhost URL printed by Vite. For a production web bundle run `npm run build` (output: `dist/`).

## Generate Android APK using GitHub Actions (no Android Studio required)

1. Create a new **private** GitHub repository.
2. Upload the **contents** of this folder to the repository root, including `.github/workflows/android-apk.yml` (the `.github` directory is hidden on some file browsers).
3. Commit to the `main` branch.
4. Open **Actions → Build Android APK → Run workflow** (or let the push to `main` start it).
5. Wait for the build to finish. Open the workflow run and download the `student-portal-debug-apk` artifact.
6. Unzip the artifact and install `app-debug.apk` on your Android phone, allowing installs from that source if prompted.

This produces a **debug APK** suitable for testing, not a signed Play Store release. The workflow needs GitHub Actions to be enabled. For production, configure a private signing key, use `assembleRelease`, and secure the keystore in GitHub Secrets.

## Scope and privacy

This is a UI prototype. Leave submissions are stored **only in memory in the current app session**. They disappear on reload. Uploads are not sent anywhere; only the filename is recorded locally in the session. Fee payment and other school menu actions are placeholders. No school API, authentication, payment processing, or backend is connected. The name, class, ID and due fee are demo values transcribed from the reference screenshots; replace them with fictional values before publishing the app publicly.
