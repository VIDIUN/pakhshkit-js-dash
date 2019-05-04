# PakhshKit JS DASH - [Shaka Player] Adapter for the [PakhshKit JS Player]

[![Build Status](https://travis-ci.org/vidiun/pakhshkit-js-dash.svg?branch=master)](https://travis-ci.org/vidiun/pakhshkit-js-dash)
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)](https://github.com/prettier/prettier)
[![](https://img.shields.io/npm/v/@pakhshkit-js/pakhshkit-js-dash/latest.svg)](https://www.npmjs.com/package/@pakhshkit-js/pakhshkit-js-dash)
[![](https://img.shields.io/npm/v/@pakhshkit-js/pakhshkit-js-dash/canary.svg)](https://www.npmjs.com/package/@pakhshkit-js/pakhshkit-js-dash/v/canary)

PakhshKit JS DASH adapter integrates [Shaka Player] with the [PakhshKit JS Player].

PakhshKit JS DASH is written in [ECMAScript6], statically analysed using [Flow] and transpiled in ECMAScript5 using [Babel].

[shaka player]: https://github.com/google/shaka-player
[shaka player api docs]: https://shaka-player-demo.appspot.com/docs/api/index.html
[flow]: https://flow.org/
[ecmascript6]: https://github.com/ericdouglas/ES6-Learning#articles--tutorials
[babel]: https://babeljs.io

## Getting Started

### Prerequisites

The adapter requires [PakhshKit JS Player] to be loaded first.

The adapter uses the [Shaka Player] javascript library.

[pakhshkit js player]: https://github.com/vidiun/pakhshkit-js

### Installing

First, clone and run [yarn] to install dependencies:

[yarn]: https://yarnpkg.com/lang/en/

```
git clone https://github.com/vidiun/pakhshkit-js-dash.git
cd pakhshkit-js-dash
yarn install
```

### Building

Then, build the player

```javascript
yarn run build
```

### Embed the library in your test page

Finally, add the bundle as a script tag in your page, and initialize the player

```html
<script type="text/javascript" src="/PATH/TO/FILE/pakhshkit.js"></script>
<script type="text/javascript" src="/PATH/TO/FILE/pakhshkit-dash.js"></script>
<div id="player-placeholder" style="height:360px; width:640px">
<script type="text/javascript">
var playerContainer = document.querySelector("#player-placeholder");
var config = {...};
var player = pakhshkit.core.loadPlayer(config);
playerContainer.appendChild(player.getView());
player.play();
</script>
```

## Configuration

[Shaka Player] configuration options, documented @[Shaka Player API docs], can be passed via the [PakhshKit JS Player] config.

The configuration is exposed via the playback section:

```javascript
{
  playback: {
    options: {
      html5: {
        dash: {
          // Shaka Player configuration options here
        }
      }
    }
  }
}
```

## Running the tests

Tests can be run locally via [Karma], which will run on Chrome, Firefox and Safari

[karma]: https://karma-runner.github.io/1.0/index.html

```
yarn run test
```

You can test individual browsers:

```
yarn run test:chrome
yarn run test:firefox
yarn run test:safari
```

### And coding style tests

We use ESLint [recommended set](http://eslint.org/docs/rules/) with some additions for enforcing [Flow] types and other rules.

See [ESLint config](.eslintrc.json) for full configuration.

We also use [.editorconfig](.editorconfig) to maintain consistent coding styles and settings, please make sure you comply with the styling.

## Compatibility

TBD

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/vidiun/pakhshkit-js-dash/tags).

## License

This project is licensed under the AGPL-3.0 License - see the [LICENSE.md](LICENSE.md) file for details
