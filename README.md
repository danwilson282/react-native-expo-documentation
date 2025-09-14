# React native and expo notes
## Install
npx create-expo-app@latest ExpoTutorial-platform-specific --template blank-typescript
(in working directory, this gets emulators functioning)
npx expo install react-dom react-native-web @expo/metro-runtime

### (cache and storage)
npm install @react-native-async-storage/async-storage

### (file based router)
npx expo install expo-router react-native-safe-area-context react-native-screens expo-linking expo-constants expo-status-bar
add the following in the package.json
{
  "main": "expo-router/entry"
}

### (react navigation wrappers)
npx expo install @react-navigation/native-stack

### (device specific code)
npx expo install react-native-screens react-native-safe-area-context

## Notes
- npm run start then scan qr code or open on web
- Use EAS (Expo application services) to submit code to app stores (initial setup difficult but subsequent pushes look easier). Follow a tutorial
- Use expo go on mobile - if doesn't work rm -rf .expo
- View is like a div. Text must be in Text component
- const styles = Stylesheet.create({}) for CSS like. classes use camelCase instead of snake
- Platform lets you identify platform
- react-navigation lets you use contexts to create navigation bottom-tabs and native stack most common
- expo router allows file like routing but with _layout.tsx. Start in app folder. use context to save state. Stack and Tabs from expo-router in layout allow nav types. useLocalSearchParams allows you to access /app/route/[id] const { id } = useLocalSearchParams();
- Caching and persistent storage in kv store - check example carefully
- Look up tailwind for react native?
