# expo-config-plugin-ios-appclip

Expo Config Plugin that generates an App Clip for iOS apps built with Expo.

## Installation

Install it in your project:

```
expo install expo-config-plugin-ios-appclip
```

In your app's Expo config (app.json, or app.config.js), add expo-config-plugin-ios-appclip to the list of plugins:

```app.json
"name": "my app",
"plugins": [
    ["expo-config-plugin-ios-appclip", {
        "entryPoint": "index.appclip"
    }]
]
```

## Configuration

Specifying the entryPoint parameter is optional, it defaults to "index.appclip". This means that the App Clip expects a file called index.appclip.ts (or index.appclip.js) in the project's root directory. You can change this value to "index" in order to reuse the existing entrypoint of the Expo app which basically means the App Clip experience will be exactly the same as the full app experience. In most cases however it will make sense to have a separate entrypoint which only renders a subset of the app's capabilities as the App Cip experience.

## Before building for the App Store

Please note that you need to add App Clip as a capability in your Apple Developer profile. Under "Certificates, Identifiers & Profiles", select the identifier of your app, check the box that says "On Demand Install Capable for App Clip Extensions" and save.