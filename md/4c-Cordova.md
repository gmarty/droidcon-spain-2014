### **Cordova**

---

<img src="img/Cordova.png" style="height: 10rem;" alt="Cordova" title="Cordova">

Build cross-platform apps

[cordova.apache.org](https://cordova.apache.org/)

---

Powers PhoneGap by Adobe

[phonegap.com](http://phonegap.com/)

---

Support

* Firefox OS
* Android
* iOS
* Windows Phone
* Many more...

---

#### APIs

* Battery Status
* Camera
* Contacts
* Device
* Device Motion (Accelerometer)
* Device Orientation (Compass)
* Dialogs (Notifications)
* Geolocation
* Network Information (Connection)
* Vibration

---

#### Install

```bash
npm install -g cordova
```

---

#### Create an app with **Cordova**

<pre>
<code class="bash fragment" data-fragment-index="2">cordova create myApp com.example.hello HelloWorld</code>
<code class="bash fragment" data-fragment-index="3">cd myApp</code>
<code class="bash fragment" data-fragment-index="4">cordova platform add firefoxos</code>
<code class="bash fragment" data-fragment-index="5">cordova platform add android</code>
</pre>

---

#### Develop your app in **HTML5**

---

Edit `myApp/config.xml`, update:

* name
* description
* author

---

The code lives in `myApp/www/` folder

---

`www/` default organisation

* css/
* img/
* js/
* index.html

---

#### Add plugins

---

##### Geolocation

First, add the plugin

```bash
cordova plugin add org.apache.cordova.geolocation
```

---

Then, in JavaScript

```javascript
function onSuccess(position) {
  console.log(position.coords);
}

navigator.geolocation.getCurrentPosition(onSuccess);
```

---

##### Notifications

```bash
cordova plugin add org.apache.cordova.dialogs
```

---

```javascript
function onDismiss() {
  console.log('Notification was dismissed');
}

navigator.notification.alert('Notified message', onDismiss);
```

---

Plugins registry

[plugins.cordova.io](http://plugins.cordova.io/)

---

#### Build your app

---

Firefox OS packaged app and Android

```bash
cordova build
```

Firefox OS hosted app

```bash
cordova prepare
```

---

##### What's next?

* Integration in Firefox dev tools
* Default icons
