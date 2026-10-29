# MintTrail Android app

This project wraps the MintTrail offline-first personal finance app in an Android WebView. You do **not** need Android Studio to build the APK; GitHub Actions can build it online.

## Build an APK without Android Studio

1. Sign in to GitHub and create a new repository (a private repository is fine).
2. Upload the **contents** of this `MintTrail-Android` folder to the repository. Make sure `.github/workflows/build-apk.yml` is included. If uploading through the website, GitHub may hide dot-folders in some upload flows; confirm the workflow exists under `.github/workflows` after uploading.
3. Open the repository's **Actions** tab and select **Build MintTrail Android APK**.
4. Press **Run workflow** (or wait for the first push build to finish).
5. Open the completed workflow run. Under **Artifacts**, download `MintTrail-debug-apk`.
6. Extract the downloaded artifact ZIP to get `app-debug.apk`.
7. Send the APK to your Android phone and open it to install. If Android asks, allow your browser/file manager to install unknown apps for this one installation.

The debug APK is for personal testing and is not a Play Store release. To publish to Google Play, a properly signed release build and Play Console setup are needed.

## App details
- App name: MintTrail
- Android package: `app.minttrail.finance`
- Minimum Android: 7.0 (API 24)
- Target SDK: 34
- UI: local HTML/CSS/JavaScript loaded inside Android WebView
- Core data is designed to remain on-device. Back up your financial data before replacing or uninstalling an app.

## Build locally (optional)
If you later have a build machine with Android SDK and Gradle, run `gradle assembleDebug` from this folder.
