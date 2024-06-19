# stbvorbis_sync.js

An ES6, synchronous port of [stbvorbis.js](https://github.com/hajimehoshi/stbvorbis.js).

Suitable for use in the `AudioWorkletGlobalScope`.

Ported for use with [SpessaSynth](https://github.com/spessasus/SpessaSynth)

## Usage

Download `stbvorbis_sync.js`. Copy `stbvorbis_sync.js`.

To use, import it like this:
```js
import { stbvorbis } from "./stbvorbis_sync.js"
```

## API

### `decode`

```js
stbvorbis.decode(buf: ArrayBuffer|Uint8Array)
```

`decode` decodes the given Ogg/Vorbis data.

The return value is an object, formatted like this

| name         | description                                                                 |
|--------------|-----------------------------------------------------------------------------|
| `data`       | An array of `Float32Array` that represents decoded stream for each channel. |
| `sampleRate` | The sample rate like 44100.                                                 |
| `eof`        | True if the stream ends, otherwise false. If this is true, `data` is null.  |
| `error`      | An error string if exists, otherwise null.                                  |