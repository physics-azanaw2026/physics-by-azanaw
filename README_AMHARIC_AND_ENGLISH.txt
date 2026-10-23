PHYSICS BY AZANAW — ANDROID APP BUILD PROJECT

What this is
------------
This folder contains a native Android WebView application project. The complete current HTML learning app is bundled inside the APK under android-app/app/src/main/assets/www/, so the lessons and quizzes can open offline. External source/video links open in the device's browser.

IMPORTANT HONEST STATUS
-----------------------
This is the Android source project plus a cloud-build workflow, NOT a compiled APK yet. This working environment does not have the Android SDK / Gradle installed and cannot reach the Android download servers. The provided workflow can build a debug APK on GitHub Actions once this project is added to the owner's existing repository.

Why the project uses Android API 36
-----------------------------------
The project targets Android API 36 and supports devices from API 23 onward, including Android 12. API 36 meets Google Play's current minimum target API requirement for new app submissions as of 31 August 2026. That does not mean the app is published or Play-Store approved.

BUILD ON THE EXISTING GITHUB REPOSITORY — DO NOT CREATE A NEW REPOSITORY
-------------------------------------------------------------------------
1. Keep the tested HTML and ZIP files as backups. Do not delete or overwrite the working app.
2. In the existing repository, add this project's complete 'android-app' folder at repository root.
3. Copy the separate file 'GITHUB_ACTIONS_WORKFLOW_TO_ADD.yml' into the repository at this exact path:
   .github/workflows/build-android-apk.yml
4. Commit these additions to a new branch or after reviewing the diff. Do not commit passwords or a private signing key.
5. Open the repository's Actions tab in the browser, choose 'Build Physics by Azanaw Android APK', and run the workflow if it did not run automatically.
6. When the workflow succeeds, open its run summary and download the artifact named 'physics-by-azanaw-debug-apk'. It is a ZIP file that contains app-debug.apk.
7. Extract app-debug.apk on the Samsung phone, tap it, and follow Android's installer prompts. Android may ask you to allow installs from the file manager/browser you used. Only install APKs that you built from your own reviewed source.

AMHARIC — አማርኛ መመሪያ
---------------------
ይህ ፋይል የAndroid መተግበሪያ የምንጭ ፕሮጀክት ነው፤ APK የተጠናቀቀ ፋይል ገና አይደለም። የሚሰራውን HTML መተግበሪያ በAndroid WebView ውስጥ ያካትታል፣ ስለዚህ የተካተቱ ትምህርቶች ያለ ኢንተርኔት ሊከፈቱ ይችላሉ። የቪዲዮና የማጣቀሻ ውጫዊ ሊንኮች በChrome ይከፈታሉ።

በቀጣይ ደረጃ፦
1. የተፈተነውን HTML እና ZIP እንደ ባክአፕ ይያዙ።
2. በአሁኑ የGitHub ሪፖዚቶሪ ውስጥ 'android-app' ፎልደርን ያክሉ። አዲስ ሪፖዚቶሪ አይፍጠሩ።
3. 'GITHUB_ACTIONS_WORKFLOW_TO_ADD.yml' ፋይልን '.github/workflows/build-android-apk.yml' በሚለው ቦታ ያስቀምጡ።
4. ለውጦቹን ከመቀበል በፊት ይመልከቱ፤ ከተቻለ አዲስ branch ይጠቀሙ።
5. GitHub ላይ Actions ይክፈቱና 'Build Physics by Azanaw Android APK' የሚለውን workflow ያስኬዱ።
6. ሲጠናቀቅ 'physics-by-azanaw-debug-apk' artifact ያውርዱ፤ ውስጡ app-debug.apk አለ።
7. APK-ውን ከZIP አውጥተው በSamsung ስልክ ይክፈቱና የAndroid install መመሪያን ይከተሉ።

DEBUG APK VS PUBLIC RELEASE
---------------------------
The workflow creates a debug-signed APK for controlled testing. Do not publish that debug APK to Google Play. A public release needs a protected signing key owned by the project owner, a signed release build (usually an Android App Bundle for Google Play), privacy/data-safety review, store listing, and policy checks. Never upload a keystore or signing passwords into this repository.

Package details
---------------
Application ID: com.physicsbyazanaw.app
Display name: Physics by Azanaw
Version: 1.0.0 (versionCode 1)
Minimum Android API: 23
Target / compile API: 36
Content source: copy of the working Visual Language Enhanced Grade 9 HTML app tested by the owner in Chrome.
