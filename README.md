# EasyTools Complete v2.0

Included working tools:
- Image → PDF: multiple images, A4 PDF, saves to Downloads
- PDF → Image: renders every PDF page to JPG, saves to Downloads
- Compress Image: JPEG compression and save to Downloads
- Unit Converter: km→m, lb→kg, °F→°C, gallon→liter
- Notes: local saved note
- QR Scanner: live rear-camera scanning using CameraX + ML Kit
- Premium screen: ready for payment integration
- Clean EasyTools home UI

## Build
Open the folder in Android Studio, allow Gradle sync, then Run.
For an APK: Build → Generate App Bundles or APKs → Generate APKs.

Important before Play Store release:
1. Replace package/application ID if desired.
2. Add a real privacy policy URL.
3. Connect AdMob and Play Billing if monetization is desired.
4. Add proper QR camera preview/decoding flow.
5. Test on several Android phones.

## AdMob integration (v3)

Google Mobile Ads SDK (GMA Next-Gen) has been integrated into the Home screen. The project uses Google's banner test ad unit while you develop and test. Google recommends test ads during development to avoid accidental interaction with production ads. Before publishing, replace `BANNER_AD_UNIT_ID` in `MainActivity.kt` with the EasyTools banner ad unit you created in AdMob.

The AdMob App ID is configured in `AndroidManifest.xml`. Do not share passwords, OTPs, or payment credentials.

## Mobile-only GitHub build

This project includes `.github/workflows/build-apk.yml`.
After the project is uploaded to a GitHub repository, open **Actions**, run **Build EasyTools APK**, and download the generated `EasyTools-debug-apk` artifact.

The workflow uses JDK 17 and a specified Gradle version, so a PC or Android IDE is not required for the build itself.
