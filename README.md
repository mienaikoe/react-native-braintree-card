# react-native-braintree-card

A react native interface for adding Braintree card payment methods.

## Usage

### Setup
```js
var BTClient = require('react-native-braintree-card');
BTClient.setup(<token>);
```

## Installation
1. Run `npm install react-native-braintree-tree --save` to add the package
2. Inside the ``ios/`` directory, create a Podfile:

  ```ruby
  # Podfile for cocoapods 1.0
  source 'https://github.com/CocoaPods/Specs.git'
  target 'yourAppTarget' do
    pod 'React', :path => '../node_modules/react-native', :subspecs => [
      'Core',
      'RCTImage',
      'RCTNetwork',
      'RCTText',
      'RCTWebSocket'
    ]
    pod 'react-native-braintree-card', :path => '../node_modules/react-native-braintree-card'
  end
  ```

  Or if you use an older CocoaPods version:
  ```ruby
  source 'https://github.com/CocoaPods/Specs.git'
  pod 'React', :path => '../node_modules/react-native', :subspecs => [
    'Core',
    'RCTImage',
    'RCTNetwork',
    'RCTText',
    'RCTWebSocket'
  ]
  pod 'react-native-braintree-card', :path => '../node_modules/react-native-braintree-card'
  ```

3. Run `pod install`.  This installs the Braintree iOS SDK and a new workspace is created.

4. Open your workspace.

5. Under your app target -> build settings, look for `Other Linker Flags` and add `$(inherited)`

  <!--![Accepts Credit/Debit Cards](/Screenshots/linker.png)-->

6. Build and run project!  If it fails the first time, clean and rebuild.

Because React Native's iOS code is now pulled in via CocoaPods, you also need to remove the ``React``, ``RCTImage``, etc. subprojects from your app's Xcode project.

![Remove Libraries](/Screenshots/removeLibraries.png)


## Requirements

Tested with:
* Node 4.1.0
* npm 2.14.3
* react-native 0.8.0
