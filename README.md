# Steps to run

1. Install dependencies

```bash
yarn && cd ios && pod install && cd ..

```

2. Run in **metro**

```bash
yarn start --reset-cache
```

3. Run in simulator

```bash
yarn android
```

or

```bash
yarn ios
```

## Notes from Shockoe:

When we install and use the SDK in react native we get this error message (in all the version we install):

```bash
// ios error message
Invariant Violation: `new NativeEventEmitter()` requires a non-null argument.
```

```bash
// android error message
[TypeError: null is not an object (evaluating 'MedalliaDigitalModule.initialize')]
```

Things we have tried:

- We have followed the instructions they have in this [documentation](https://docs.medallia.com/digital/docs-v2/mobile-sdk-docs/index.html#pages/developers-portal/react-native/quick-start/react-native-quick-start.html).

- We added the types in the typescript modules of the app so that it would recognize the app.

- We allowed JavaScript in the `tsconfig.json` of the project.

- We try to add the types on the library

- We tried to create the `index.js` file that maps the native methods (from the sdk) for use in React Native to typescript.

- We installed the native libraries in project (android) and made the native module in typescript.

- We tried with several versions like: 3.3.0, 3.6.0, 3.9.3, 3.10.3 but none of them worked in Typescript project but when we installed in Javascript project worked.
