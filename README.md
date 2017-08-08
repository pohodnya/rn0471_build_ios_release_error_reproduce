### Environment
1. react-native-cli: 2.0.1
react-native: 0.47.1
2. node: v8.2.1
3. npm: v5.3.0
4. yarn: 0.20.3

- Target Platform: iOS
- Development Operating System: MacOS

### Steps to Reproduce

1. react-native init rn0471_build_ios_release_error_reproduce
2. open .xcodeproj file
3. edit scheme -> select "release" build configuration
4. build & run in simulator

### Actual Behavior
Build failed error in XCode:

```
+ DEST=/Users/alekseypokhodnya/Library/Developer/Xcode/DerivedData/rn0471reproduce-fdeyxrhuiruhnzgprfosmoijckya/Build/Products/Release-iphonesimulator/rn0471reproduce.app
+ [[ Release = \D\e\b\u\g ]]
+ BUNDLE_FILE=/Users/alekseypokhodnya/Library/Developer/Xcode/DerivedData/rn0471reproduce-fdeyxrhuiruhnzgprfosmoijckya/Build/Products/Release-iphonesimulator/rn0471reproduce.app/main.jsbundle
+ node /Users/alekseypokhodnya/RubymineProjects/rn047-fail-test/rn0471reproduce/node_modules/react-native/local-cli/cli.js bundle --entry-file index.ios.js --platform ios --dev false --reset-cache --bundle-output /Users/alekseypokhodnya/Library/Developer/Xcode/DerivedData/rn0471reproduce-fdeyxrhuiruhnzgprfosmoijckya/Build/Products/Release-iphonesimulator/rn0471reproduce.app/main.jsbundle --assets-dest /Users/alekseypokhodnya/Library/Developer/Xcode/DerivedData/rn0471reproduce-fdeyxrhuiruhnzgprfosmoijckya/Build/Products/Release-iphonesimulator/rn0471reproduce.app
/Users/alekseypokhodnya/RubymineProjects/rn047-fail-test/rn0471reproduce/node_modules/metro-bundler/src/lib/Terminal.js:141
    this._nextStatusStr = util.format(format, ...args);
                                              ^^^

SyntaxError: Unexpected token ...
    at exports.runInThisContext (vm.js:53:16)
    at Module._compile (module.js:373:25)
    at Module._extensions..js (module.js:416:10)
    at Object.require.extensions.(anonymous function) [as .js] (/Users/alekseypokhodnya/RubymineProjects/rn047-fail-test/rn0471reproduce/node_modules/babel-register/lib/node.js:152:7)
    at Module.load (module.js:343:32)
    at Function.Module._load (module.js:300:12)
    at Module.require (module.js:353:17)
    at require (internal/module.js:12:17)
    at Object.<anonymous> (/Users/alekseypokhodnya/RubymineProjects/rn047-fail-test/rn0471reproduce/node_modules/react-native/local-cli/server/runServer.js:18:18)
    at Module._compile (module.js:409:26)
+ [[ false != true ]]
+ [[ ! -f /Users/alekseypokhodnya/Library/Developer/Xcode/DerivedData/rn0471reproduce-fdeyxrhuiruhnzgprfosmoijckya/Build/Products/Release-iphonesimulator/rn0471reproduce.app/main.jsbundle ]]
+ echo 'error: File /Users/alekseypokhodnya/Library/Developer/Xcode/DerivedData/rn0471reproduce-fdeyxrhuiruhnzgprfosmoijckya/Build/Products/Release-iphonesimulator/rn0471reproduce.app/main.jsbundle does not exist. This must be a bug with'
error: File /Users/alekseypokhodnya/Library/Developer/Xcode/DerivedData/rn0471reproduce-fdeyxrhuiruhnzgprfosmoijckya/Build/Products/Release-iphonesimulator/rn0471reproduce.app/main.jsbundle does not exist. This must be a bug with
+ echo 'React Native, please report it here: https://github.com/facebook/react-native/issues'
React Native, please report it here: https://github.com/facebook/react-native/issues
+ exit 2
```

### Reproducible Demo
https://github.com/pohodnya/rn0471_build_ios_release_error_reproduce
