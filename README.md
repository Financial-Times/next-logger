# Next Logger [![Build Status](https://travis-ci.org/Financial-Times/next-logger.svg)](https://travis-ci.org/Financial-Times/next-logger)

Logging utility

## Usage

```
var loggerInit = require('ft-next-logger').init;
# init first, setting the app's name
loggerInit({ appName: 'ft-next-front-page' });
var logger = require('ft-next-logger').logger;

logger.info('Saying hello');
logger.warn('Everything’s mostly cool');
logger.error('Uh-oh', { field: 'some value' });
```

or if you're living in the wonderful world of JavaScript modules,

```
import {init as loggerInit, logger} from 'ft-next-logger';
# init first, setting the app's name
loggerInit({ appName: 'ft-next-front-page' });

logger.info('Saying hello');
...
```

(Uses Winston, so see [here](https://github.com/winstonjs/winston) for full api)

## Releasing

    $ make release version=patch

Version also accepts `minor`, `major`, etc. See the [release-it docs](https://www.npmjs.com/package/release-it#user-content-examples)
