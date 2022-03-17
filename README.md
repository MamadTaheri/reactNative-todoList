# React Native Essentials

## Beginning

Install expo :

    npm install --global expo-cli

Initial a new React-native project with expo  :

    expo init my-app

Start developement server :

    expo start


## Building application Old-Fashion way


    expo build:android -t apk

## Building application Recent way

First time: install eas-cli using

    npm install -g eas-cli

Then, every time we need build, we can use:

    eas build -p android
