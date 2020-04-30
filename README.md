[![XO code style](https://img.shields.io/badge/code_style-XO-5ed9c7.svg)](https://github.com/sindresorhus/xo)
[![Build Status](https://travis-ci.org/mrdotb/yifysubtitles.svg?branch=master)](https://travis-ci.org/mrdotb/yifysubtitles)

# yifysubtitles
> Download and convert subtitles in [VTT format](https://developer.mozilla.org/en/docs/Web/API/Web_Video_Text_Tracks_Format) for [YTS movies](https://yts.ag/)


## Install

```bash
$ npm i yifysubtitles-to-gs --save
```

## Usage

```js
const yifysubtitles2GS = require('yifysubtitles-to-gs');

const saveSubtitles = await yifysubtitles2GS({storage: 'storage', bucketName: 'bucketName'});
const results = await saveSubtitles('tt1156398', {
  langs: ['en', 'vi'],
  format: 'vtt' // Default: vtt (Only support vtt format)
})
console.log(results)
/*
[
  {
    lang: 'english',
    langShort: 'en',
    path: 'https://[bucket_name].storage.googleapis.com/[file_name]',
    fileName: 'Zombieland.2009.720p.BrRip.x264-YIFY.vtt'
  },
  ...
]
*/
```

## License

MIT © [Mrdotb](https://github.com/MRdotB)
