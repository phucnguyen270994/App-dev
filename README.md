# stair

[![pipeline status](https://gitlab.com/ConnectivCorporation/contract/stair-lab/stair-app/badges/develop/pipeline.svg)](https://gitlab.com/ConnectivCorporation/contract/stair-lab/stair-app/commits/develop)
[![coverage report](https://gitlab.com/ConnectivCorporation/contract/stair-lab/stair-app/badges/develop/coverage.svg)](https://gitlab.com/ConnectivCorporation/contract/stair-lab/stair-app/commits/develop)

#### This is the mobile application source repository for the stair project.

## Installation

### Prerequisites

- With android: Android Studio - SDK - Gradle - JDK
- With IOS: Xcode
- React native cli
- yarn/npm

### For both IOS/Android

Create a folder `envs` and then create file `development.json` | `local.json` | `production.json` | `staging.json` with format

```json
{
    "REACT_APP_BACKEND_API_URL": [REACT_APP_BACKEND_API_URL],
    "SOCKET_URL": [socket_url],
    "BACK_URL": [back_url],
    "VERSION": [version],
    "AWS_COGNITO_IDENTITY_POOL_ID": [AWS_COGNITO_IDENTITY_POOL_ID],
    "AWS_USER_POOLS_ID": [AWS_USER_POOLS_ID],
    "AWS_USER_POOLS_WEB_CLIENT_ID": [AWS_USER_POOLS_WEB_CLIENT_ID],
    "AWS_DOMAIN": [AWS_DOMAIN],
    "AWS_LINE": [AWS_LINE],
    "ENV": [ENV]
}
```

#### ANDROID

Go to `android/app` folder to generate `debug.keystore` with command:

```command
keytool -genkey -v -keystore debug.keystore -storepass android -alias androiddebugkey -keypass android -keyalg RSA -keysize 2048 -validity 10000
```

#### IOS

Go to `ios` folder to install pod library with command:
```
pod install
```

### Install

- Run with command `yarn android:staging`/ `yarn ios:staging`
- Run `yarn start` to start metro server.
- Modify [analytics.js](./node_modules/expo-analytics/analytics.js) in line 36

```
an: "Stair",
aid: "Stair",
av: "1.1",
```

> Optionals, You can run project with `Android studio`/ `Xcode` by open ios/android folder base on platform

## Documentation:

This project is using [UI Kitten components][link:ui-kitten], [here you can find documentation and other useful articles][link:doc-ui-kitten].


## License

[MIT](LICENSE.txt) license.

[link:doc-ui-kitten]: https://akveo.github.io/react-native-ui-kitten
[link:ui-kitten]: https://github.com/akveo/react-native-ui-kitten
