TypeScript compiler fails type checks with Cypress in a yarn workspace.

Steps to reproduce and error output:

```bash
$ yarn install
$ cd packages/e2e
$ yarn tsc
yarn run v1.13.0
$ tsc
../../node_modules/cypress/types/cy-blob-util.d.ts:6:27 - error TS2307: Cannot find module './blob-util'.

6 import * as blobUtil from './blob-util'
                            ~~~~~~~~~~~~~

../../node_modules/cypress/types/cy-bluebird.d.ts:4:33 - error TS2307: Cannot find module './bluebird'.

4 import BluebirdStatic = require('./bluebird')
                                  ~~~~~~~~~~~~

../../node_modules/cypress/types/cy-moment.d.ts:1:25 - error TS2307: Cannot find module 'moment'.

1 import moment = require('moment')
                          ~~~~~~~~

../../node_modules/cypress/types/sinon-chai/index.d.ts:12:24 - error TS2307: Cannot find module '../sinon'.

12 import * as Sinon from '../sinon';
                          ~~~~~~~~~~


Found 4 errors.

error Command failed with exit code 2.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```
