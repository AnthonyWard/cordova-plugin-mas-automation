# cordova-plugin-mas-automation

Automatically set up your project for CA MAS SDK 1.6.10 support

## Depends On

`cordova-plugin-mas-core` version 1.6.10

`cordova-plugin-cocoapod-support`

Cordova 8 CLI

## What It Does

- Adds the cordova plugin for the CA MAS SDK
- Pulls does the SDK for Android and iOS via PODs and Gradle
- Sets up the `NSLocationWhenInUseUsageDescription` for iOS
- Forces at least Java Version 1.8 for Android

More here: http://mas.ca.com/docs/cordova/1.6.10/guides/

## What It Doesn't Do

Copy in the required `msso_config.json`, to do that put something like this in your `config.xml`

```xml
    <platform name="android">
        <resource-file 
            src="www/android_msso_config.json"
            target="app/src/main/assets/msso_config.json" />
    </platform>
    <platform name="ios">
        <resource-file
            src="www/ios_msso_config.json"
            target="msso_config.json" />
    </platform>
```

## Install

`cordova plugin add https://github.com/AnthonyWard/cordova-plugin-mas-automation`