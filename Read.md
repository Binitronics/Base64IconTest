# Ionic native map test project
1. ### [Issue description](##1-Issue-description)
2. ### [Error Log](##2-Error-Log)
3. ### [Notes](###3-Notes)

## 1. Issue description
The issue occurs when adding a marker on the map. The icon property of the MarkerOptions class accepts different format (.png, color name, base64 ...etc.). When the icon is set with “blue” or .png format the marker is drawn on the map without any problem. When the icon is set with Base64 format, the marker is drawn on the map as expected but an error is thrown (see Error Log section). 

## 2. Error Log
```
Unhandled Promise rejection: Cannot read property 'width' of undefined ; Zone: <root> ; Task: Promise.then ; Value:
TypeError: Cannot read property 'width' of undefined
zone.js:690
message:"Cannot read property 'width' of undefined"
stack:"TypeError: Cannot read property 'width' of undefined
    at Map.<anonymous> (http://localhost/plugins/cordova-plugin-googlemaps/www/Map.js:1487:63)
    at http://localhost/plugins/cordova-plugin-googlemaps/www/commandQueueExecutor.js:63:21
    at ZoneDelegate.invoke (http://localhost/polyfills.js:3553:160)
    at Zone.run (http://localhost/polyfills.js:3279:37)
    at http://localhost/polyfills.js:4204:28
    at ZoneDelegate.invokeTask (http://localhost/polyfills.js:3586:173)
    at Zone.runTask (http://localhost/polyfills.js:3336:39)
    at drainMicroTaskQueue (http://localhost/polyfills.js:3802:25)"
  ```
### 3-Notes
Please don't forget to add your Google map android API key on both config.xml and home.ts files. 