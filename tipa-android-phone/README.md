# Tipa Barber Shop — Android phone build

This is a minimal Android WebView wrapper around the existing Tipa Barber Shop HTML demo. It is intended for **installing and testing on an Android phone**, not as a production-ready booking service.

## What works
- The included HTML demo opens as an Android app.
- JavaScript and browser local storage are enabled so demo interactions can run and persist locally on that device.
- No Android Studio or computer is required if you use GitHub Actions to build the APK in the cloud.

## Important limits
- The current UI is a local demo. Login is not real Google sign-in, and accounts/appointments do not sync between customers and barbers.
- Do not use it for real customer bookings until a secure backend, real authentication, server-side roles, availability conflict checks, and a privacy policy are implemented.
- The APK from the workflow is a **debug APK** for personal testing. It is not the signed release bundle for Google Play.

## Build from an Android phone using GitHub Actions
1. Download `tipa_barber_shop_android_phone_project.zip` and extract it with a file manager such as ZArchiver.
2. In your phone browser, sign in to GitHub and create a **new public or private repository** named `tipa-barber-shop`. Keep it empty when creating it.
3. Upload the extracted project's files and folders to the repository, preserving the folder structure. Make sure `.github/workflows/build-apk.yml` is included. If GitHub's mobile upload screen hides dot-folders, switch the browser to Desktop site or use GitHub's web editor to create `.github/workflows/build-apk.yml` from the copy in the ZIP.
4. Open the repository's **Actions** tab. If asked, enable workflows.
5. Choose **Build Tipa Barber Shop APK** → **Run workflow** → **Run workflow**.
6. Wait for the run to finish with a green check. Open that run, scroll to **Artifacts**, and download `tipa-barber-shop-debug-apk`.
7. Extract the downloaded artifact ZIP. Tap `app-debug.apk` and allow your browser/file manager to install apps from that source if Android asks. Only install the APK you built from your own repository.

## If the Actions tab is missing
- Confirm `.github/workflows/build-apk.yml` is committed to the repository on the default branch.
- Open the repository in the browser's Desktop site mode and refresh.

## App details
- Display name: Tipa Barber Shop
- Android package: `com.tipabarbershop.app`
- Version: `1.0.0` (versionCode 1)
- Minimum Android: Android 6.0 (API 23)
- Target SDK: API 36
