## Develop Apps<br> on **Firefox OS**

---

### What's an **open web app**?

---

Minimal app:

* A HTML page
* A manifest
* Icons

---

Web apps have access to device features through WebAPI.

---

Web app types

* Hosted
* Packaged
* Certified

---

#### Hosted app

Stored on a server, easy to upgrade, limited access

---

#### Packaged app

Reviewed by the Marketplace, packaged and signed

Note:
As the name implies!

---

#### Certified app

Part of the OS, only by Mozilla and partners

---

### `manifest.webapp`

```json
{
  "name": "My App",
  "description": "My elevator pitch goes here",
  "launch_path": "/index.html",
  "icons": { "128": "/img/icon-128.png" },
  "developer": {
    "name": "Your name or organization",
    "url": "http://your-homepage-here.org"
  }
}
```

---

Proper HTTP header

`Content-Type: application/x-web-app-manifest+json`

---

More about manifest files

[developer.mozilla.org/Apps/Build/Manifest](https://developer.mozilla.org/Apps/Build/Manifest)

---

#### How to deliver your app?

---

##### Firefox Marketplace

The official app store

---

##### Self-publishing

---

```javascript
var manifestUrl = '//my-server.com/myApp/manifest.webapp';
var req = navigator.mozApps.installPackage(manifestUrl);
req.onsuccess = function() {
  // App is installed.
};
req.onerror = function() {
  // App wasn't installed, info is in 
  // installapp.error.name
};
```

---

Self-publishing allows to turn any website into an app store!

---

### Develop your own app

---

#### From scratch

1. Create a HTML file
2. Add JavaScript
3. Add a manifest and an icon
4. Ready to play!

---

No devices? No problem!

Use Firefox

---

#### Install

1. Install Firefox nightly
2. Go to `about:config`
3. Set `devtools.webide.enabled` to `true`

---

#### Usage

Tools > Web developer > App Manager

---

WebIDE (formerly App Manager)

<img src="img/WebIDE.png" style="height: 10em; vertical-align: middle; margin-bottom: 25px;" alt="Web IDE" title="Web IDE">

---

### Develop app using **templates**
