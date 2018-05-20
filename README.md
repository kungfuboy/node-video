# node-video

If your website can 't play video in Safari, you may need that.

## Install

```shell
yarn add node-video -S

or 

npm i -S node-video
```

## Options

* `root` 视频或者音频的根目录, 默认是 `process.cwd()`.
* `extMatch` 请求路径的匹配规则，可以是 数组、正则(匹配资源的后缀名)，默认是 `['.mp4', '.flv', '.webm', '.ogv', '.mpg', ".mpg", '.wav', '.ogg']`

## Example

```javascript
const Koa = require('koa')
const nodeVideo = require('node-video')

const app = new Koa()

app.use(nodeVideo({
    extMatch: /\.mp[3-4]$/i
}))
```
