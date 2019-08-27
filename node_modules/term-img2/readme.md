# term-img2

> Display images in your terminal

![](screenshot.jpg)

Even [animated gifs](https://github.com/vdemedes/gifi)!

*Currently only supported on [iTerm >=2.9](https://www.iterm2.com/downloads.html).*


## Install

```
$ npm install --save term-img2
```


## Usage

```js
const termImg = require('term-img2');

termImg('unicorn.jpg', {log: true});
```


## API

### termImg(input, [options])

#### input

Type: `string` `buffer`

Filepath to an image or an image as a buffer.

#### options

##### width
##### height

Type: `string` `number`

The width and height are given as a number followed by a unit, or the word "auto".

- `N`: N character cells.
- `Npx`: N pixels.
- `N%`: N percent of the session's width or height.
- `auto`: The image's inherent size will be used to determine an appropriate dimension.

##### preserveAspectRatio

Type: `boolean`<br>
Default: `true`

##### log

Type: `boolean`<br>

Log image in terminal, `false` by default.

##### fallback

Type: `function`<br>
Default: `() => throw new UnsupportedTerminal()`

Enables you to do something else when the terminal doesn't support images.

#### return

Type: `string`<br>
The image string that can be displayed in terminal.

## Related

- [imgcat](https://github.com/egoist/imgcat) - CLI for this module


## License

MIT © [EGOIST](https://github.com/egoist)
