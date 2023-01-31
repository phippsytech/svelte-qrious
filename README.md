
# Svelte QRious Component
[Svelte QRious](https://github.com/phippsytech/svelte-qrious) is a wrapper around [QRious](https://github.com/neocotic/qrious), a pure JavaScript library for generating QR codes using HTML5 canvas.  It is  a Svelte Component.
* [Install](#install)
* [Usage](#usage)
* [Settings](#settings)
* [Bugs](#bugs)
* [License](#license)

## Install
``` bash
$ npm i @phippsytech/svelte-qrious
```

If you are using this in SvelteKit, check [this issue](https://github.com/phippsytech/svelte-qrious/issues/2#issuecomment-1410029003) about additional configuration required in your `vite.config.js`

## Usage
``` html
<script>
import {QRious} from  '@phippsytech/svelte-qrious';
</script>

<QRious  value="https://svelte.dev" />
```

## Settings
You can control many aspects of the QR code using the following attributes:

| Field | Type | Description | Default |
| --------------- | ------- | -------------------------------------------------- | ------------- |
| background | String | Background color of the QR code | `"white"` |
| backgroundAlpha | Number | Background alpha of the QR code | `1.0` |
| foreground | String | Foreground color of the QR code | `"black"` |
| foregroundAlpha | Number | Foreground alpha of the QR code | `1.0` |
| level | String | Error correction level of the QR code (L, M, Q, H) | `"H"` |
| padding | Number | Padding for the QR code (pixels) | `null` (auto) |
| size | Number | Size of the QR code (pixels) | `100` |
| value | String | Value encoded within the QR code | `""` |
```HTML
<QRious
	value="https://github.com/phippsytech/svelte-qrious"
	background="green"
	backgroundAlpha=0.8
	foreground="blue"
	foregroundAlpha=0.8
	level="H"
	padding=25
	size=500
/>
```

## Bugs
If you have any problems with the Svelte QRious component raise an issue [here](https://github.com/phippsytech/svelte-qrious/issues).

## License
**Svelte QRious**
Copyright © 2022 Phippsy Tech Pty Ltd

**QRious**
Copyright © 2017 Alasdair Mercer  
Copyright © 2010 Tom Zerucha

See LICENSE.md for more information on our GPLv3 license.
