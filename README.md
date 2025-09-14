# React native and expo notes
## Install
npx create-expo-app@latest ExpoTutorial-platform-specific --template blank-typescript
(in working directory, this gets emulators functioning)
npx expo install react-dom react-native-web @expo/metro-runtime

(cache and storage)
npm install @react-native-async-storage/async-storage

(file based router)
npx expo install expo-router react-native-safe-area-context react-native-screens expo-linking expo-constants expo-status-bar
add the following in the package.json
{
  "main": "expo-router/entry"
}

(react navigation wrappers)
npx expo install @react-navigation/native-stack

(device specific code)
npx expo install react-native-screens react-native-safe-area-context
