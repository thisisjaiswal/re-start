# re-start :globe_with_meridians: :iphone: :computer:

[![npm version](https://badge.fury.io/js/react-native-template-everywhere.svg)](https://badge.fury.io/js/react-native-template-everywhere)
[![Greenkeeper badge](https://badges.greenkeeper.io/react-everywhere/re-start.svg)](https://greenkeeper.io/)

[![re-start (1).png](https://s4.postimg.org/4a0zw1egd/re-start_1.png)](https://postimg.org/image/6elcx4g2x/)


## This project  is an attempt to: 
* Target multiple platforms (Android, iOS, web, windows(UWP), osX(native) and ionic(osX, Ubuntu and Windows)) with react native' APIs and a single codebase.
* Follow best practices while doing the above.
* Cut out the time and effort it takes to setup the project (based on create-react-app).
* Achieve 'Write once use everywhere' with react-native (though react strictly says 'Learn once use anywhere').


## Current status: 
react-native-everywhere is now re-start (where re stands for react-everywhere).
Good news is that react-native-cli now supports [templates](https://github.com/facebook/react-native/pull/12548).
So, it makes makes much more sense if this project is a react-native-template, 
which will remove the need to update this project with every major release of react-native.
It just works as of now on all the platforms.
So, no more git cloning.

 
## Usage 

#### Pre-requisites:
Node.js & npm on your system([follow this](https://docs.npmjs.com/getting-started/installing-node))<br/>
react-native CLI (`npm install -g react-native-cli`)

All you have to do is:
- Create a new react-native project using react-native-cli and specify this project as a template:
```
react-native init <Your Project Name> --template everywhere --version="0.44.2"
```
- Since react-native-template does'nt support adding dev dependencies and custom scripts to package.json,
 so I have created a custom script to do that.
```
node scripts/addDevDependencies.js
```
##### Notes:
 - If the above script fails due to some reason, you can do it manually by copying the contents
 of devDependencies.json to your package.json's devDependencies object and adding following to the scripts object.
 ```
"web": "node scripts/start.js",
"build": "node scripts/build.js"
```
- react-native-web currently (20th of July, 2017) supports React/ReactDOM 15.4, 15.5, or 15.6, so make sure you do not upgrade if you want support for web.
- make sure that the version of react-native-windows is same as your react-native version, if you are targeting windows support.

---

## Run the project on a specific platform:

#### Android
`react-native run-android`

#### iOS
`react-native run-ios`

#### Web
`npm/yarn run web`

#### Windows
`react-native windows`
`react-native run-windows`

### Build for production:
#### Android/iOS
[This will help](https://facebook.github.io/react-native/docs/running-on-device.html)

#### Web
`npm/yarn run build` (this will build your production ready bundle)

-------
### Some very useful cross platform compatible libraries:
- [react-native-vector-icons](https://github.com/oblador/react-native-vector-icons)
- [re-render](https://github.com/amoghbanta/re-render) (this is experimental and a WIP)
- [axios](https://github.com/mzabriskie/axios)
- [react-navigation](https://github.com/react-community/react-navigation) (might be included in ReactNativeEverywhere soon)


-------
### Progress:
- [x] support for web ([react-native-web](https://github.com/necolas/react-native-web))<br/>
- [x] support for Windows ([react-native-windows](https://github.com/ReactWindows/react-native-windows))<br/>
- [ ] Support for electron<br/>
- [ ] Support for react-native-macOS<br/>

---
### Running demo on Web, Android, iOS and Windows(Universal):
<p align="center">
<img src="https://s28.postimg.org/gmgva9rrh/58961a12afcd1276062762.gif" height="450"  width="260">
<img src="https://s28.postimg.org/nbneqad3h/58961a2a030da447844552.gif" height="450"  width="260">
</p>
<p align="center">
<img src="https://s28.postimg.org/aa1q0fop9/589619ef1b623465256988.gif" height="450"  width="260">
<img src="https://s21.postimg.org/yuzzepj7b/ezgif_com_video_to_gif.gif" height="450"  width="260">
</p>

