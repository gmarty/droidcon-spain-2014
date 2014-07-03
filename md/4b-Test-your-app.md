### Test your **web app** on **Android**

---

mozilla-apk-cli

[github.com/mozilla/apk-cli](https://github.com/mozilla/apk-cli)

---

Command line tool for the **APK Factory Service**

---

#### Install

```bash
npm install -g mozilla-apk-cli
```

---

#### Usage

1. Build the APK
2. Install it

---

Build the APK

```bash
# The app lives in myApp/www/ folder
cd myApp
mozilla-apk-cli www my_app.apk
```

---

Works with **hosted apps**

```bash
mozilla-apk-cli http://localhost/manifest.webapp my_app.apk
```

---

And with **packaged apps** too

```bash
mozilla-apk-cli my_app.zip my_app.apk
```

---

Install the APK

```bash
adb install my_app.apk
```

---

Happy testing!

---

But don't distribute the APK
