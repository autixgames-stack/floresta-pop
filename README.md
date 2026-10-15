# Floresta Pop

Floresta Pop is a casual block puzzle game for Android, developed by AutixGames. Place pieces on the board, complete rows and columns, collect fireflies, and use the butterfly power to clear space. The game saves the high score on the device and currently has no advertising or analytics SDK.

The browser version is in `index.html`. The Android WebView project is in `android/`; its packaged game page is `android/app/src/main/assets/public/index.html`.

## Build the Android app

1. Install Android Studio with Android SDK Platform 36 and a compatible JDK.
2. Open the `android` folder in Android Studio and let Gradle sync.
3. To build a debug APK from PowerShell:

   ```powershell
   .\gradlew.bat :app:assembleDebug
   ```

   The APK is written to `app\build\outputs\apk\debug\app-debug.apk`.

4. To build a release bundle, configure a private signing properties file outside the repository and use the Play App Signing upload key. Never commit a keystore or signing properties. The checked-in release build configuration expects the local signing file at `../../../work/floresta-pop-signing.properties` relative to the Android project; maintainers may adjust that local path for their setup.

## Browser version

Open `index.html` in a modern browser. The game is designed for touch and pointer input; progress is stored locally in the browser.

## Privacy

The published privacy policy is available at <https://sites.google.com/view/floresta-pop-privacidade>. It describes the current build; update the policy and Play Console declarations before adding ads, analytics, accounts, or network features.

## Play testing

Closed testing is managed through the Google Play Console. Testers must use the official opt-in link and follow the Console's participation requirements. Do not post personal email addresses publicly.

## License

No open-source license is provided in this repository. All rights are reserved by the copyright holders unless they grant permission separately.
