# EV Charger Pro — Android project

A WebView-based Android application shell with the EV Charger Pro interface in `app/src/main/assets/index.html`.

## Build APK with GitHub Actions (no Android Studio required)

1. Create a **new empty GitHub repository** named `EVChargerPro` (do not add a README, license, or `.gitignore` on GitHub).
2. Upload the **contents of this folder** to the repository root. The `.github` folder must be included.
3. Open the repository's **Actions** tab and enable workflows if GitHub asks.
4. Select **Build EV Charger Pro APK** and click **Run workflow**.
5. When the run is green, open it and download the artifact named **EV-Charger-Pro-debug-APK**. Unzip it to get `app-debug.apk`.

The workflow uses JDK 17, Android SDK, Gradle 8.9, Android Gradle Plugin 8.7.3, and Kotlin 2.0.21. It runs a task-discovery check before building and verifies that the APK exists before upload.

## Project layout

- `settings.gradle` — includes `:app` and configures plugin/dependency repositories.
- `build.gradle` — pins Android and Kotlin plugin versions.
- `app/build.gradle` — Android application module.
- `app/src/main/AndroidManifest.xml` — launcher activity and app metadata.
- `app/src/main/java/com/evchargerpro/app/MainActivity.kt` — WebView activity.
- `app/src/main/assets/index.html` — app interface.
- `.github/workflows/build-apk.yml` — automated APK build.

## Engineering notice

This is a starter/prototype application, not a certified electrical design tool. Cable sizing and voltage-drop estimates must be independently checked. It does not replace applicable standards, manufacturer instructions, local regulations, or review by a qualified electrical engineer. Do not use it as the sole basis for selecting protective devices or installing EV charging equipment.
