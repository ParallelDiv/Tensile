# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Tensile is an offline-first, minimalist workout tracker app built with Flutter for Android.

### Prerequisites
- Flutter 3.38.6 (stable channel)
- Dart 3.10.7
- Android SDK 36.1.0
- JDK 21 (bundled with Android Studio)

## Build Commands

### Run on Emulator
```bash
flutter emulators --launch Medium_Phone_API_36.1  # Start emulator
flutter run                                        # Build and run app
```

### Build APK
```bash
flutter build apk                    # Release APK
flutter build apk --debug            # Debug APK
```

### Testing
```bash
flutter test                         # Run all tests
flutter test test/widget_test.dart   # Run specific test
```

### Other Useful Commands
```bash
flutter devices                      # List connected devices/emulators
flutter clean                        # Clean build artifacts
flutter pub get                      # Fetch dependencies
flutter doctor                       # Check environment setup
```

## Project Structure

```
lib/
  main.dart              # App entry point
android/                 # Android-specific configuration
  app/
    src/main/
      kotlin/            # MainActivity.kt (native entry point)
      AndroidManifest.xml
test/                    # Widget and unit tests
pubspec.yaml            # Dependencies and metadata
analysis_options.yaml   # Linting rules
```

## Development Notes

- Main app code is in `lib/main.dart`
- Android package: `com.paralleldiv.tensile`
- First build may take several minutes as Gradle downloads dependencies
- `pubspec.lock` is committed (standard for Flutter apps)
- Hot reload available when running with `flutter run` (press `r`)
