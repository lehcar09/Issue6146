# Issue 5644

### Github Issue Link
- https://github.com/firebase/firebase-android-sdk/issues/6146

### Summary
- With AGP alpha version (8.7.0-alpha02) and `isMinifyEnabled = true` cause crash on app start

```agsl

Invalid component registrar : Could not instantiate com.google.firebase.installations.FirebaseInstallationsKtxRegistrar
Invalid component registrar : Could not instantiate com.google.firebase.crashlytics.CrashlyticsRegistrar
java.lang.NullPointerException: FirebaseCrashlytics component is not present.

```
### Prerequisite:
- add `google-services.json` file in app

### Workaround
#### Option 1
1. Use non-alpha version of Android Gradle Plugin (i.e. 8.5.1)

#### Option 2
1. Add `android.enableR8.fullMode=false` in gradle.properties
