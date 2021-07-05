# React-Native Command

## Windows  Commands
- rm node_modules/ 
- use ; for muti line commands
- rm $TMPDIR/react-* ; rm ios/build ; rm node_modules ; yarn cache clean ; npm cache verify

# React Native

- react-native --help
- react-native start 
- adb devices 
- react-native run-android or run-ios
- react-native run-android --deviceId XXxxxxx 
- react-native run-android --variant=release
- react-native log-android
- adb shell input keyevent 82
- adb reverse tcp:8081 tcp:8081 
- adb install APK_NAME.apk `Directely install in Device`
- adb logcat `// Native logs` 
- cd android && ./gradlew assembleRelease `Release Build`
- cd android && ./gradlew clean `Gradlew Clean`
- ./gradlew :app:dependencies `Check Project dependency `
- rm -rf node_modules/ `Remove Node_modules`
- react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res `used for making build`

- react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle `bundle only`

## GENERATING KEYSTORE
- keytool -genkeypair -v -keystore my-upload-key.keystore -alias my-key-alias -keyalg RSA -keysize 2048 -validity 10000

## Play Store to Upload .aab
- (Command) java -jar bundletool.jar build-apks --bundle=release/app.aab --output=outputapk/app.apks --connected-device --ks=ryderpassenger.keystore --ks-pass=pass:rydrpassenger --ks-key-alias=rydrpassenger --key-pass=pass:rydrpassenger

- bundletool should be at same folder [bundletool](https://developer.android.com/studio/command-line/bundletool)
- bundle `path of .aab file`
- output `destination path where apks zip folder should go`
- connected-device/ universal 
- ks  `keystore path `
- ks-pass `keystore password`
- ks-key-alias `keystore alias`

# Permission 
- chmod -R 777 folder_name/file_name
## adb Server ([no permissions](https://stackoverflow.com/questions/9210152/set-up-device-for-development-no-permissions))
- sudo adb kill-server
- sudo adb start-server

# Npm 
- npm install or yarn install
- watchman watch-del-all && rm -rf $TMPDIR/react-* && rm -rf ios/build && rm -rf node_modules && yarn cache clean && npm    cache verify
- yarn install && yarn start --reset-cache
- npm install && npm start --reset-cache

# NVM
- nvm install 9.11.1
- nvm use 9.11.1
# EsLint 
- ./node_modules/.bin/eslint --init

# POD 
- pod init
- pod install
## cocoapods update
- sudo gem install cocoapods

# Visual Studio Commands
- ctrl+p  for Searching files from Visual Studio 
- ctrl+J for getting Terminal on Visual Studio Code 
- ctrl+, for Setting in Visual Studio

# Kill port
- lsof -nP -i4TCP:8545 | grep LISTEN
- kill -9 [post_no]
- killall -9 node

## Kill LINIX port
- netstat -plten | grep LISTEN | grep 8081

# Truffle Commands
- truffle test
- truffle compile
- truffle migtate --reset --all
- truffle migtate --network=development --reset

# Git
- git log -n 1