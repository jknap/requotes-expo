# Build an iOS Simulator .app in Expo

- modify the build profile in [eas.json](https://docs.expo.dev/build/eas-json) and add the following **waldo-ios** profile:
```json
{
  "build": {
    "waldo-ios": {
      "ios": {
        "simulator": true
      }
    },
    "production": {}
  }
}
```
- make sure you are logged in to the Expo CLI with the same account you used to create the EAS project:
```bash
npx expo login
```
- now you can run the eas build command with that profile:
```bash
eas build -p ios --profile waldo-ios
# ✔ Build finished
# 🍎 iOS app:
# https://expo.dev/artifacts/eas/kYnbyzM6fHVmd9ytUZyN3b.tar.gz
```
- download the .tar.gz file, extract it and voilà, you have your .app file!



# Build an Android emulator .apk in Expo

- modify the build profile in [eas.json](https://docs.expo.dev/build/eas-json) and add the following **waldo-android** profile:
```json
{
  "build": {
    "waldo-android": {
      "android": {
        "buildType": "apk"
      }
    },
    "production": {}
  }
}
```
- now you can run the eas build command with that profile:
```bash
eas build -p android --profile waldo-android
# ✔ Build finished
# 🤖 Android app:
# https://expo.dev/artifacts/eas/mH8xyCMyaL8x8krS1eMexB.apk
```
- download the .apk file and voilà!


# Build an iOS Simulator .app in a React Native project
# Build an Android emulator .apk in a React Native project