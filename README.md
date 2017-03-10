# test-sharp-electron
Demo of Sharp with Electron, not working when packaged under Linux

To reproduce the error:
* I use:
  * Ubuntu 16.10;
  * Node 7.6.0;
  * npm 4.1.2;
  * electron 1.6.2;
* `npm install`
* `./node_modules/.bin/electron-rebuild -v 1.6.2`
* `electron .`: here, everything should work
* `npm run dist`
* `./dist/linux-unpacked/test-sharp`: this should fail
* `ldd dist/linux-unpacked/resources/app.asar.unpacked/node_modules/sharp/bin/linux-x64-53/sharp.node`: two libraries should be missing
