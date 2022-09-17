# Insta Fetcher

[![HitCount](http://hits.dwyl.com/Gimenz/insta-fetcher.svg)](http://hits.dwyl.com/Gimenz/insta-fetcher) [![GitHub license](https://img.shields.io/github/license/Gimenz/insta-fetcher)](https://github.com/Gimenz/insta-fetcher/blob/master/LICENSE) [![Npm package monthly downloads](https://badgen.net/npm/dm/insta-fetcher)](https://npmjs.com/package/insta-fetcher) ![GitHub repo size](https://img.shields.io/github/repo-size/Gimenz/insta-fetcher?style=flat) [![npm version](https://badge.fury.io/js/insta-fetcher.svg)](https://badge.fury.io/js/insta-fetcher)

Fetch instagram Api Di teruskan dan dikembangan bolaxd

Mohon dukung Yang punya repositori : [Saweria](https://saweria.co/masgimenz "Saweria")

# Features

- [x] fetchPost
- [x] fetchUser

# Usage

### Installation:

```bash
npm i github:bolaxd/insta-fetcher
```

### recommended to set the cookie before make call to all function

```js
let { igApi, getCookie } = require("insta-fetcher");
// using constructor
let ig = new igApi("your cookie");

// you can get sesion id by using getSessionId function, it requires username & password
(async () => {
  const session_id = await getCookie("username", "password");
  console.log(session_id);
})();
```

## Example

more example you can check at example.ts file

```js
let { igApi } = require("insta-fetcher");
let ig = new igApi("your cookie");

// Public post
ig.fetchPost("https://www.instagram.com/reel/CXhW_4sp32Z/").then((res) => {
  console.log(res);
});

// User data
ig.fetchUser("mg.creativestudio").then((res) => {
  console.log(res);
});

```

## TQ TO:

- https://github.com/Gimenz/nganu - simple multi-device base WhatsApp Bot
