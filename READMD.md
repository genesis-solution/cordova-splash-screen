# Cordova Splash Screen Setup Guide

This guide outlines the steps to configure a splash screen for a Cordova project and set up the necessary environment.

---

## Prerequisites

Ensure the following are installed on your system:
- **Cordova**: Globally installed via npm.
- **Java JDK**: Installed version 17 or compatible.
- **Android SDK**: Installed with API levels 33 and 34.
- **Gradle**: Version 7.6 installed.
- **Android Studio**: Optional, but useful for managing the SDK and debugging.

---

## Environment Variables

### Set the following environment variables:
1. **JAVA_HOME**: 
   - Path to your JDK 17 installation.
   - Example: `C:\Program Files\Java\jdk-17`

2. **ANDROID_HOME**:
   - Path to your Android SDK installation.
   - Example: `C:\Users\<your-username>\AppData\Local\Android\Sdk`

3. **Path Variables**:
   Ensure the following directories are added to your `Path` environment variable:
   - `${JAVA_HOME}\bin`
   - `${ANDROID_HOME}\cmdline-tools\latest\bin`
   - `${ANDROID_HOME}\platform-tools`
   - `${ANDROID_HOME}\build-tools\34.0.0`
   - `${ANDROID_HOME}\emulator`

### Verify Environment Variables:
To verify your setup, open a terminal and run:
```bash
java -version
adb --version
sdkmanager --list
gradle -v
```

---

## Installing Cordova

Install Cordova globally via npm:
```bash
npm install -g cordova
```

---

## Building the Project

To build the Android project:
```bash
cordova build android
```

If you encounter issues, ensure you’ve configured the environment variables and that Gradle is installed correctly.

---

## Troubleshooting

### Common Errors:
1. **`No installed version of Gradle found`**:
   - Ensure Gradle is installed and the path is set in `Path`.
   - Verify with:
     ```bash
     gradle -v
     ```

2. **`Android target not installed`**:
   - Install the required Android targets:
     ```bash
     sdkmanager "platforms;android-33" "platforms;android-34"
     ```

---

## References

- [Cordova Documentation](https://cordova.apache.org/docs/)
- [Android Developer Guide](https://developer.android.com/)
```
