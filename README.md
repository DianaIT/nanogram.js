<!-- An easy-to-use and simple Instagram package that allow you to fetch media content without API and access token -->

<p align="center">
  <img width="50%" src="https://raw.githubusercontent.com/webistomin/nanogram.js/260d58af351d84606a75b32160f349c9a444691d/assets/logo.svg" alt="Nanogram">
</p>

---

<h4 align="center">An easy-to-use and simple Instagram package that allow you to fetch media content <strong>without API</strong> and <strong>access token</strong>.</h4>


<p align="center">
  <a href="https://travis-ci.org/webistomin/nanogram.js">
    <img src="https://travis-ci.org/webistomin/nanogram.js.svg?branch=master"
         alt="Travis CI">
  </a>
  <a href="https://codecov.io/gh/webistomin/nanogram.js">
    <img src="https://codecov.io/gh/webistomin/nanogram.js/branch/master/graph/badge.svg" alt="codecoverage" />
  </a>
  <a href="https://www.codefactor.io/repository/github/webistomin/nanogram.js"><img src="https://www.codefactor.io/repository/github/webistomin/nanogram.js/badge" alt="CodeFactor" /></a>
  <img alt="GitHub issues" src="https://img.shields.io/github/issues/webistomin/nanogram.js">
  <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/webistomin/nanogram.js">
  <img alt="npm type definitions" src="https://img.shields.io/npm/types/nanogram.js">
  <a href="https://bundlephobia.com/result?p=nanogram.js@0.1.0">
  <img alt="npm bundle size" src="https://img.shields.io/bundlephobia/minzip/nanogram.js">
  </a>
</p>

<p align="center">
<a href="https://www.npmjs.com/package/nanogram.js"><img alt="npm" src="https://img.shields.io/npm/v/nanogram.js"></a>
<a href="https://www.npmjs.com/package/nanogram.js"><img alt="downloads" src="https://img.shields.io/npm/dm/nanogram.js"></a>
<a href="https://cdn.jsdelivr.net/npm/nanogram.js">
<img src="https://data.jsdelivr.com/v1/package/npm/nanogram.js/badge?style=rounded" alt="jsdelivr">
</a>
</p>

<p align="center">
  <a href="#key-features-">Key Features</a> •
  <a href="#demo-">Demo</a> •
  <a href="#installation-">Installation</a> •
  <a href="#how-to-use-">How To Use</a> •
  <a href="#examples-">Examples</a> •
  <a href="#browser-support-">Browsers support</a> •
  <a href="#contributing-">Contributing</a> •
  <a href="#license-">License</a>
</p>

## Key Features ✨

* **Small.** 2.2KB (minified and gzipped). <a href="https://github.com/ai/size-limit">Size Limit</a> controls the size.
* **No dependencies.**
* No need for the **access token** secret.
* **Easy to use.**
* **Typescript** support
* **Tree shakeable**

## Demo 👀

TBD

## Installation ⚙

### Using package managers

#### npm
```npm
$ npm install nanogram.js --save
```

#### yarn
```yarn
$ yarn add nanogram.js
```

### via CDN

Add script right before closing `</body>` tag

```html
<script src="https://unpkg.com/nanogram.js@0.1.0/dist/nanogram.iife.js"></script>
or
<script src="https://cdn.jsdelivr.net/npm/nanogram.js"></script>
```

## How to use 🤔

### 1. Initialize Nanogram.js

**Option A: Using Webpack or Rollup:**
```js
import Nanogram from 'nanogram.js';

const instagramParser = new Nanogram();
```

**Option B: Using Node.js:**
```js
const Nanogram = require('nanogram.js');

const instagramParser = new Nanogram();
```

**Option C: Using CDN:**
```js
/* Nanogram is available from global namespace */
const instagramParser = new Nanogram();
```

### 2. Get your data

**Get media content by providing instagram username**

```js
instagramParser.getMediaByUsername('instagram').then((media) => {
  console.log(media);
});
```

_Note:_ get content from [userpage](https://www.instagram.com/instagram/)

**Get media content by providing instagram tag**

```js
instagramParser.getMediaByTag('sunset').then((media) => {
  console.log(media);
});
```

_Note:_ get content from [tag page](https://www.instagram.com/explore/tags/sunset/)

---

**Get media content by providing location id and place name**

```js
instagramParser.getMediaByLocation(6264386, 'highbridge-park').then((media) => {
  console.log(media);
});
```

_Note:_ get content from [location page](https://www.instagram.com/explore/locations/6264386/highbridge-park)

---

**Get all available countries**

```js
instagramParser.getCountries().then((countries) => {
  console.log(countries);
});
```

_Note:_ get countries from [location page](https://www.instagram.com/explore/locations/)

---

**Get all cities by providing country id**

```js
instagramParser.getCitiesByCountryId('US').then((cities) => {
  console.log(cities);
});
```

_Note:_ get cities from [country page](https://www.instagram.com/explore/locations/US/)

---

**Get all places by providing city id**

```js
instagramParser.getPlacesByCityId('c2728325').then((places) => {
  console.log(places);
});
```

_Note:_ get places from [city page](https://www.instagram.com/explore/locations/c2728325/)

---

**Get media content by providing place id**

```js
instagramParser.getMediaByPlaceId(2999512).then((media) => {
  console.log(media);
});
```

_Note:_ get content from [place page](https://www.instagram.com/explore/locations/2999512/)

---

**Get media content by providing search query**

```js
instagramParser.getMediaBySearchQuery('sunset').then((media) => {
  console.log(media);
});
```

_Note:_ get content from searchbar on the top of the page

---

## Examples ☺

<details>
    <summary>TBD</summary>
    Something small enough to escape casual notice.
</details>

## Browsers support 🌎

| [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png" alt="IE / Edge" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br/>IE / Edge | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png" alt="Firefox" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br/>Firefox | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png" alt="Chrome" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br/>Chrome | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png" alt="Safari" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br/>Safari | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari-ios/safari-ios_48x48.png" alt="iOS Safari" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br/>iOS Safari | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png" alt="Opera" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br/>Opera | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/yandex/yandex_48x48.png" alt="Yandex" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br/>Yandex |
| --------- | --------- | --------- | --------- | --------- | --------- | --------- |
| IE11*, Edge 12+| 40+ | 42+ | 10.1+| 10.3+ | 29+| 15.6+

`*` – For IE11 you need to install **fetch** polyfill. Because of how `fetch()` works, you’ll also need a **Promise** polyfill.

If you want maximum browser compatibility, please use polyfills.

See caniuse for [fetch](https://caniuse.com/#search=fetch) and [promise](https://caniuse.com/#search=promise).

### Browsers polyfills

If you want to send a polyfill only to browsers that need it, there's a handy service called [Polyfill.io](https://polyfill.io/v3/url-builder/) which does just that, it offers a wide array of polyfills.

Here's an example of using [polyfill.io](https://polyfill.io/v3/url-builder/) to polyfill only the `Fetch` and `Promise` feature, so if we put this right before closing `</body>` tag of `index.html` and `Nanogram.js` script, Polyfill.io will read the user agent and use that information to determine if the browser requires a polyfill for the feature or features listed. Since I'm using Chrome it will send back an empty response since my browser doesn't need it, pretty slick.

```html
<script src="https://polyfill.io/v3/polyfill.min.js?features=fetch%2CPromise></script>
```

Alternatively, you can install packages like [es6-promise](https://github.com/stefanpenner/es6-promise) and [whatwg-fetch](https://github.com/github/fetch).

### Node.js

Node.js doesn't have a built-in implementation of the `Fetch API`, but you can use any library with a compatible interface, such [node-fetch](https://github.com/node-fetch/node-fetch).


## Contributing 🎉

Found a bug? Missing a specific feature?
Your contributions are always welcome! Please have a look at the [contribution guidelines](https://github.com/webistomin/nanogram.js/blob/master/CONTRIBUTING.md) first.

## License 📄

### [MIT](https://github.com/webistomin/nanogram.js/blob/master/LICENSE)



