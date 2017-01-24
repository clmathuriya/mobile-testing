# mobile-testing
##setup
- download android studio from here https://developer.android.com/studio/index.html
- add SDK/tools and SDK/platform-tools to path variable.
##testing android app
refer this doc for more details https://developer.android.com/studio/test/index.html
###code inspect
- right click on project > analyze> inspect code
###android monitor
-click on android monitor > logcat to see error messages and debug messages
- click on monitors  tab to view cpu,gpu,memory and network usage.

#to pull apk from device
1) Determine the package name of the app, e.g. "com.example.someapp". Skip this step if you already know the package name.

 adb shell pm list packages

Look through the list of package names and try to find a match between the app in question and the package name. This is usually easy, but note that the package name can be completely unrelated to the app name. If you can't recognize the app from the list of package names, try finding the app in Google Play using a browser. The URL for an app in Google Play contains the package name.

2) Get the full path name of the APK file for the desired package.

adb shell pm path com.example.someapp

The output will look something like this: package:/data/app/com.example.someapp-2.apk

3) Pull the APK file from the Android device to the development box.

adb pull /data/app/com.example.someapp-2.apk


