*DEPRECATED*: There is now an easier and better way to bring back those buttons: https://www.xda-developers.com/bring-back-wifi-mobile-data-quick-settings-tiles-android-12-adb/
Just execute in adb shell:
```
settings put global settings_provider_model false
settings put secure sysui_qs_tiles "wifi,cell,$(settings get secure sysui_qs_tiles)"
```



Google has removed *Wi-Fi* from QS in Android 12 replacing it with useless *Internet* button
This tiny project brings it back

Target API 28 is required to allow this app to turn Wi-Fi on and off.
Location permission is optional, if you want to show connected Wi-Fi SSID and currently must be granted manually.

I can't publish this in Google Play, since it requires minimum target API 29.
It's possible to use higher API if user grants this app a Device Admin role.
Not implemented currently, but I may do that in spare time.
