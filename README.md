# react-native

- React Native allows us to use the React library to create mobile apps (Android & iOS)
- It's best to understand core principles of React first
  - Functional components
  - State
  - Props
  - React hooks (useState hook) https://reactjs.org/docs/hooks-reference.html#usestate
- Works similar to React for web
  - Create an app by building a component tree
  - React Native takes components and compiles them into native code and widgets that work on Android and iOS
- Install node https://nodejs.org/en/download/
- Command Line Interface
  - Expo CLI
    - A wrapper that is better for beginners, allows for easy access to certain features
    - Less flexibility
  - React Native CLI
    - More fine-grain control, more complex
    - Can switch to RN CLI by ejecting project from Expo
- Install Expo CLI https://expo.io/learn
  ```sh
  npm install expo-cli --global
  ```
- Create your project
  ```sh
  expo init myproject
  ```
- Choose blank project
- Install with npm
- Move into directory
  ```sh
  cd myproject
  ```
- Open in Microsoft Visual Studio Code
  ```sh
  code .
  ```
- Get started (opens tab in browser with expo's debug tools)
  ```sh
  npm start
  ```
- Download expo client on phone and use QR code to preview app https://play.google.com/store/apps/details?id=host.exp.exponent
- Install Android Studio https://developer.android.com/studio
  - Click Configure and select AVD Manager
  - Select your phone
  - Download Pie (API level 28)
  - Click Next
  - Click Finish
  - Click Play button icon
- Project files overview
  - .expo - expo configuration/settings
  - .expo-shared - expo configuration/settings
  - assets - images
  - node_modules - dependencies
  - .gitignore - which files not to track for version control
  - App.js - kickstarts the app
  - app.json - information about project
  - babel.config.js - configuring how babel (compiler) works
  - package-lock.json - track dependencies
  - package.json - track dependencies

### Other resources

- https://www.youtube.com/watch?v=OxIDLw0M-m0&list=PL4cUxeGkcC9ij8CfkAY2RAGb-tmkNwQHG
- https://www.youtube.com/watch?v=ur6I5m2nTvk&list=PL4cUxeGkcC9ixPU-QkScoRBVxtPPzVjrQ
  - https://github.com/iamshaunjp/react-native-tutorial
- https://github.com/hsavit1/Awesome-React-Native-Education
- https://expo.io/
- https://youtu.be/PuRIMFWVZ1M?t=259
- https://facebook.github.io/react-native/docs/getting-started
- https://facebook.github.io/react-native/docs/tutorial
- https://github.com/facebook/create-react-app
