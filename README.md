# Neptune-API

API used for various routs such as YouTube and ShareX. Used in [Neptune-API-Wrapper](https://www.npmjs.com/package/neptune-api-wrapper)

### Getting Started

* Download the repository
* Install the dependencies via `npm i`

### Prerequisites

```
NodeJS version 8.x or higher
MySQL
```

### Installing


* Make a copy of `config.json.sample` and remove the `.sample` extension
* Fill in the MySQL details, and the Google API key, then run the app via `node server.js`, now follow as bellow

## Getting your API key
* Make sure you generate a good, long, random string and replace `secret` in `config.json` with this string
* Go to `localhost:8080/generateKeys?key=1&name=YOURNAME`


Once you have created a new key, copy `hash` and replace `adminKey` in `config.json` with this new key and change `firstTimeRun` to `"no"`.

You must now use this key for creating new keys in the future.

### Routes

*GET* `/api/generateKey`


* `?key=` the admin API key

* `&name=` the name of the new keyholder



*GET* `/api/ping`

*GET* `/api/yt_playlist`

* `?key=` API key
* `&maxVideos=` Max videos to get
* `&id=` Playlist ID

*GET* `/api/yt_video`

* `?key=` API key
* `&maxVideos=` Max videos to get
* `&search=` Video name

*POST* `/api/sharex`
* `key`
* `name`
* `file`

## Authors

* **AB0529** - *Initial work* - [Anish](https://github.com/MoistSenpai)

