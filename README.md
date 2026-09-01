# Artha — cloud-build Android project

This project packages the Artha HTML app in an Android WebView and includes a GitHub Actions workflow so the APK can be built in the cloud without Android Studio.

## Phone-only build

1. Create/sign in to a GitHub account.
2. Create a new repository, e.g. `artha-android`.
3. Upload the contents of this folder to the repository. Keep the `.github/workflows/build-apk.yml` file.
4. Open the repository's **Actions** tab.
5. Select **Build Artha APK**.
6. Tap **Run workflow**.
7. When it finishes, open the completed workflow run.
8. Under **Artifacts**, download **Artha-debug-apk**.
9. Extract the downloaded artifact and install the APK on your Android phone.

GitHub Actions provides hosted runners that can execute Gradle builds; the workflow uses the official Gradle setup action and uploads the generated APK as a build artifact.

For a Play Store release later, a signed release build and keystore should be added separately. Do not put a private signing key directly into the repository.
