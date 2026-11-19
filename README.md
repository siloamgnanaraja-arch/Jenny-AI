# Jenny AI — Native Android starter project

## What this first version does
- Native Android app (not an HTML page).
- Dark purple/pink assistant screen with a professional female assistant portrait.
- Tap-to-talk speech recognition in English (India) or Tamil (India).
- Spoken replies using the phone's installed Android Text-to-Speech voice.
- Opens WhatsApp, YouTube, Instagram and Spotify; opens their website if the app is not installed.
- Searches saved contacts by name and opens the dialer for you to confirm a call.
- Accepts typed commands too.

## Limitations in version 1
- "Hey Jenny" is **not** an always-on wake word yet. Tap the microphone while the app is open.
- It cannot listen while the app is closed or bypass Android lock-screen restrictions.
- It cannot unlock the phone, bypass app locks, force shutdown/reboot, or silently place calls.
- Calls open the dialer for confirmation.
- Replies use the phone's installed TTS voice, not a cloned human voice.
- Speech recognition quality and Tamil/English availability depend on the phone's speech service and network.

## Build using your Android phone
1. Download and extract `JennyAI_Android_Project.zip` using your file manager (Files or ZArchiver).
2. Install a trusted Android IDE that supports Kotlin, Android Gradle Plugin 8.7.3, JDK 17 and Jetpack Compose. AndroidIDE may be an option if a compatible release is available for your Android version.
3. Open the extracted `JennyAI_Android_Project` folder in that IDE. Select the folder containing `settings.gradle.kts`.
4. Let the IDE download Gradle and Android dependencies. This needs internet and may take time.
5. Choose the `app` run configuration and build/run the project.
6. Install the generated APK when Android prompts you.
7. Open Jenny AI and allow Microphone. Allow Contacts only when you want contact lookup.
8. Tap the microphone and test:
   - open WhatsApp
   - open YouTube
   - open Instagram
   - call [a saved contact name]
   - what time is it
   - what is today's date

## Alternative: build APK using GitHub Actions
The project includes `.github/workflows/build-apk.yml`.
1. Create a private repository on GitHub using your phone browser.
2. Upload the extracted project files and folders (not the ZIP itself) to the repository.
3. Open the repository's Actions tab and run **Build Jenny AI APK**.
4. When the workflow finishes, open the run and download the `JennyAI-debug-apk` artifact.
5. Download the APK on your phone and install it. Android may ask you to allow installs from your browser or file manager.

## Project details
- Application ID: `com.jennyai.assistant`
- Minimum Android: 8.0 (API 26)
- Compile SDK / target SDK: 35
- Version: 1.0

## Next stage
Add Android assistant-role integration and a visible, user-controlled foreground wake-word service. Continuous microphone access is restricted by Android and must be tested on the specific phone.
