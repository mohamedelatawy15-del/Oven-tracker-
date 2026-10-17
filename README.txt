OVEN TRACKER - build the Android APK (about 10 minutes, one time)

You need on your computer:
  1. Node.js 18 or newer      https://nodejs.org
  2. Android Studio           https://developer.android.com/studio
     (open it once so it installs the Android SDK)

Steps (in a terminal, inside this folder):
  npm install
  npx cap add android
  npx cap sync
  npx cap open android

In Android Studio, wait for Gradle to finish, then:
  Build > Build Bundle(s) / APK(s) > Build APK(s)
Click "locate" in the pop-up. The file is app-debug.apk.
Copy it to your phone and open it (allow "install unknown apps" if asked).

First launch: tap Allow on the notification question.
Then tap "Send test alert" and close the app. You should get an alert in 5 seconds.

Notes
  - Alerts fire at 09:00 the day before pull-out, on pull-out day and on check days.
  - On Android 12 and newer, if alerts arrive late, open Settings > Apps > Oven Tracker
    > Alarms & reminders and allow it. Also set battery to "Unrestricted" for this app.
  - Your log is stored on the phone only. Uninstalling the app deletes it.
  - To change the alert time, edit at9() in www/index.html (hour 9), then run: npx cap sync
