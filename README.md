# React Native Essentials
![GitHub last commit](https://img.shields.io/github/last-commit/MamadTaheri/reactNative-todoList)

## 01- Beginning

Install expo :

    npm install --global expo-cli

Initial a new React-native project with expo  :

    expo init my-app

Start developement server :

    expo start


## 02- Building application Old-Fashion way


    expo build:android -t apk

## 03- Building application Recent way

First time: install eas-cli using

    npm install -g eas-cli

Then, every time we need build, we can use:

    eas build -p android

## 04- Building APKs for Android emulators and devices : [Link](https://docs.expo.dev/build-reference/apk/)

first, change  `eas.json` file like this:

    {
    "build": {
        "preview": {
        "android": {
            "buildType": "apk"
        }
        },
        "preview2": {
        "android": {
            "gradleCommand": ":app:assembleRelease"
        }
        },
        "preview3": {
        "developmentClient": true
        },
        "production": {}
    }
    }

then, use this command:
    
    eas build -p android --profile preview


## 05- Clearing bundler caches on Windows based on [expo website](https://docs.expo.dev/troubleshooting/clear-cache-windows)

### Expo CLI and npm
    del node_modules
    npm cache clean --force
    npm install
    watchman watch-del-all
    del %appdata%\Temp\haste-map-*     // File
    del %appdata%\Temp\metro-cache     //Folder
    expo start --clear
