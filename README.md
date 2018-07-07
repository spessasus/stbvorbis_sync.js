# stbvorbis.js

A JavaScript port of [stb_vorbis.c](https://github.com/nothings/stb).

## API

```
stbvorbis.initialize(): Promise
```

`initialize` initializes this library. `initialize` must be called once before the usage of this library.

`initialize` returns a promise that is resolved when initialization is done.

```
stbvorbis.decode(buf: ArrayBuffer|Uint8Array): {data: []Float32Array, sampleRate: number}
```

`decode` decodes the given Ogg/Vorbis data and returns the result.

The result includes `data` field and `sampleRate` field. `data` is an array of `Float32Array` that represents decoded stream for each channel. `sampleRate` represents the sample rate like 44100.

`decode` throws an exception when decoding fails.
