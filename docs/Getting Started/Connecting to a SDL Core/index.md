## Connecting to a SDL Core

### Connect with an Emulator
To connect to a SDL Core emulator, make sure timplement a TCP connection. The emulator and app should be on the same network (i.e. remember to set the correct IP address and port number in the `SDLLifecycleConfiguration`). The IP will most likely be the IP address of the operating system running the SDL Core emulator. The port will most likely be `12345`.

!!! IMPORTANT
Known issues:

* When app is in the background mode, the app will be unable to communicate with SDL Core. This will work on IAP connections.
* Audio will not play on the SDL Core. Only IAP connections are currently able to play audio.
!!!

### Connect with a Vehicle Head Unit or a Technical Development Kit (TDK)
#### Production
To connect your iOS device directly to a vehicle head unit or TDK, make sure to implement an iAP (`default`) connection in the `SDLLifecycleConfiguration`. Then connect the iOS device to the head unit or TDK using a USB cord.

#### Debugging
If you are testing with a vehicle head unit or TDK  and want to see debug logs in Xcode while the app is running, you must use another app called the [relay app](https://github.com/smartdevicelink/relay_app_ios) to help you connect to the device. When using the relay app, make sure to implement a TCP connection. Please see the [guide](Developer Tools/Relay) for the relay app to learn how to setup the connection between the device, the relay app and your app.

!!! NOTE
The same issues apply when connecting the Relay app with a TDK or head unit as do when connecting to SDL Core. Please see the issues above, under the *Connect with an Emulator* heading.
!!!
