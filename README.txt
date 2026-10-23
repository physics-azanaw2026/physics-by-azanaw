Physics by Azanaw — Android Native Wrapper Project

This is a cloud-build-ready Android Studio/Gradle project. It wraps the exact HTML app the owner tested in Chrome into a native Android WebView and bundles the lessons locally for offline reading.

IMPORTANT: The package contains source code and a cloud-build workflow, not a compiled APK. This environment has Java but no Android SDK/Gradle installation and cannot download build dependencies, so an APK cannot be truthfully claimed as already built here.

Contents
- android-app/: Android Gradle project and the full working HTML app inside app/src/main/assets/www/.
- .github/workflows/physics-by-azanaw-build-apk.yml: build workflow for an existing GitHub repository.
- GITHUB_ACTIONS_WORKFLOW_TO_ADD.yml: duplicate copy of the workflow for easy access.
- README_AMHARIC_AND_ENGLISH.txt: step-by-step build and installation guidance in English and Amharic.
- PROJECT_STATUS.txt: project status and limitations.

To use in the existing repository (do not create a new repo)
1. Add the android-app/ folder at the root of the existing repository.
2. Add .github/workflows/physics-by-azanaw-build-apk.yml at the same path in the existing repository. Review the diff first; do not overwrite existing files without review.
3. Push/commit to a new branch or submit a pull request for owner review.
4. On GitHub, open Actions and run “Build Physics by Azanaw Android APK”. Download artifact “physics-by-azanaw-debug-apk” after the build succeeds; it contains app-debug.apk.
5. Extract the APK on the Samsung phone and install it after reviewing the source/build results.

Android configuration
- Application ID: com.physicsbyazanaw.app
- Display name: Physics by Azanaw
- Version: 1.0.0 (version code 1)
- minSdk 23 (supports Android 12 / API 31)
- compileSdk 36, targetSdk 36
- AGP 8.10.1, Gradle 8.11.1, Java 17
- Local lesson assets are loaded with AndroidX WebViewAssetLoader, following Android developer guidance.

The initial APK build is a debug build for testing only. Do not upload it to Google Play. A public release requires a separately protected owner-controlled signing key and release build. Never put keystores or passwords in the repository.
