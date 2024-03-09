
# Flutter Animated Splash Screen: A Step-by-Step Guide with Code Examples

Are you looking to create an animated splash screen for your Flutter app? Look no further! we’ll walk you through the process of creating a beautiful and engaging splash screen that will leave your users impressed.

### What is a Splash Screen?
A splash screen is a screen that appears when an app is launched. It usually displays the app’s logo or branding and is designed to give the user a sense of what the app is about. A well-designed splash screen can help set the tone for the rest of the app and make a great first impression on users.

### Why Use an Animated Splash Screen?
While a static splash screen can be effective, an animated splash screen can take things to the next level. An animated splash screen can help grab the user’s attention and make the app feel more dynamic and engaging. It can also help set the tone for the rest of the app and give the user a sense of what to expect.

## Steps to Create an Animated Splash Screen with Flutter.
1. Create a new Flutter project if you didn't have already running app.

2. For the first time we need to change the native splash screen and the launcher icon for our app. add flutter_native_splash using terminal.
#### command:

```https
 $ flutter pub add flutter_native_splash 
```
at pubspec.yaml file add this lines to change the launcher icon which is located in "assets/logo.png" or create flutter_launcher_icons.yaml file and add these code.

```
flutter_launcher_icons:
  android: "launcher_icon"
  ios: true
  image_path: "assets/logo.png"
  adaptive_icon_foreground: "assets/logo.png"
  adaptive_icon_background: "#0C58E5"
  remove_alpha_ios: true
  min_sdk_android: 21 # android min sdk min:16, default 21
  web:
    generate: true
    image_path: "path/to/logo.png"
    background_color: "#hexcode"
    theme_color: "#hexcode"
  windows:
    generate: true
    image_path: "path/to/logo.png"
    icon_size: 48 # min:48, max:256, default: 48
  macos:
    generate: true
    image_path: "path/to/logo.png"
```
then run this command in terminal :
```https
$ flutter pub run flutter_launcher_icons  
```
at the same pubspec.yaml file add this lines to change the native splash screen which is located in "assets/logo.png" or create flutter_native_splash.yaml file and add these code.
```
flutter_native_splash:
  color: "#ffffff"
  image: assets/logo.png
  color_dark: "#000000"
  android_12:
    image: assets/logo.png
  android: true
  ios: true     
```
then run this command in terminal
```https
to add: $ dart run flutter_native_splash:create   
to remove : $ dart run flutter_native_splash:remove 
```
3. Add animated_splash_screen.
