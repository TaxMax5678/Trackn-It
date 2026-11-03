# Attendance Tracker (Android)

Web app lives in `www/index.html`. Everything else wraps it as an Android app with Capacitor.

## Get the APK (no Android Studio needed)
1. Create a new private repository on GitHub.
2. Upload every file in this folder to it (keep the `.github` folder), on the `main` branch.
3. Open the repository's **Actions** tab. The "Build Android APK" run starts by itself. If it doesn't, choose **Build Android APK** then **Run workflow**.
4. When the run turns green, open it and download **attendance-tracker-apk** from Artifacts. Unzip it to get `app-debug.apk`.
5. Send `app-debug.apk` to your phone, tap it and allow "Install unknown apps" when asked.

## Update the app after changing the web page
1. Replace `www/index.html` with the new file.
2. Upload it to the repository. The build runs again and gives a new APK.
3. Before a Play Store upload, raise `versionCode` in `android/app/build.gradle` by 1 each release.

## Build on your own computer instead
1. Install Node 22, JDK 21 and Android Studio.
2. In this folder run `npm install`, then `npx cap sync android`, then `npx cap open android`.
3. In Android Studio choose **Build > Build APK(s)**.

## Details
- App id: `com.taxi.attendancetracker`
- Name: Attendance Tracker
- Android 7.0 and up
