# yak
A better Google Chat.

For now, all it does it display an alert dialog a few seconds after DOM document load.

## Yak Mac Desktop App Installation
Clone this repo, then build the electron app from source:
```
npm install -g nativefier
nativefier --name "Yak" --internal-urls ".*?\.google\.*?" --inject ./yak.js --icon ./yakyak.png "https://chat.google.com"
```
Run the generated `Yak.app` file under `Yak-darwin-x64`.

## Yak Browser Installation
Login to https://chat.google.com and run this in the Chrome Console:
```
var yak = document.createElement('script');
yak.setAttribute('src','https://rkuzsma.github.io/yak/dist/build.js');
document.head.appendChild(yak);
```

## How to debug the Desktop App
Chrome Dev Tools are enabled in the Yak desktop app menubar under View->Toggle Developer Tools. Use the Console to write your enhancements to Google Chat in real-time.

Edit `yak.js` to point to any JS URL you want, or change it locally.
