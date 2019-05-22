## Electrode Native Realm Demo MiniApp

Simple MiniApp to demo [Realm](https://realm.io/) support in Electrode Native and help  testing future versions.

Electrode Native only currently supports this native module on Android.   
We are actively working on iOS support which should be released soon.

The demo code used in [App.js](App.js) is a copy/paste of the [official demo code from Realm](https://realm.io/docs/javascript/latest/).

### Prerequisites

[Electrode Native](https://github.com/electrode-io/electrode-native) >= 0.32.2

### To run this demo on Android

- `yarn install`
- `ern run-android`

### To add realm to your own MiniApp

- `ern add realm`

### Important Remarks

- As of Electrode Native 0.32, it is necessary to manually add the native Realm libraries (.so) files to a `jniLibs` directory in the Runner application (or your own application), as can be seen in [this commit](https://github.com/belemaire/ern-realm-demo-miniapp/commit/a599e5c7eb7ad969dd9482e12678217e962f1f7a). This won't be necessary anymore starting with Electrode Native 0.33.

- It is necessary to remove 64 bit support in the Runner project (or your own application if 64 bit support is enabled), as can be seen in [this commit](https://github.com/belemaire/ern-realm-demo-miniapp/commit/148169ad37713b080aa9afec34807080d0169184). 64 bit support was introduced in React Native 0.59, but Realm is [not providing 64 bit library yet](https://github.com/realm/realm-js/issues/2221). As soon as Realm ships 64 bits libraries, this won't be needed anylonger.