# ExamSprint Android

This Android project wraps the supplied `examsprint.html` as a local Android WebView app. The HTML is bundled inside the app, so the current quiz functionality works without an internet connection.

## Build without installing Android Studio (GitHub cloud build)
1. Create a GitHub account if you don't already have one.
2. Create a new repository and upload all files from this project folder (including the hidden `.github` folder).
3. Open the repository's **Actions** tab and select **Build ExamSprint APK**.
4. Click **Run workflow** (or push the files to the `main` branch to trigger it).
5. When the workflow finishes, open the run and download **ExamSprint-debug-apk** under Artifacts.
6. Extract the downloaded artifact to get `app-debug.apk`, then transfer it to your Android phone and install it. Android may ask you to allow installs from your browser or file manager.

## Build using Android Studio
1. Open this folder in Android Studio.
2. Allow Gradle sync and install the Android SDK platform requested by the project (API 35).
3. Choose **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
4. Android Studio will show the APK location after the build completes.

## Notes
- Application ID: `com.examsprint.app`
- App name: `ExamSprint`
- Minimum Android version: Android 6.0 (API 23)
- The app currently stores recent results in local browser storage on that device.
- No backend, login, cloud sync, or remote question updates are included.
- This is an unsigned debug-build project unless you create a signed release in Android Studio.
