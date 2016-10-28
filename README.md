# yarn-install [![NPM version](https://img.shields.io/npm/v/yarn-install.svg?style=flat-square)](https://npmjs.com/package/yarn-install) [![NPM downloads](https://img.shields.io/npm/dm/yarn-install.svg?style=flat-square)](https://npmjs.com/package/yarn-install) [![Build Status](https://img.shields.io/circleci/project/egoist/yarn-install/master.svg?style=flat-square)](https://circleci.com/gh/egoist/yarn-install)

If command `yarn` exists it uses Yarn to install, otherwise fallbacks to npm.

## Install

```bash
$ npm install --save yarn-install
```

## Usage

```js
const install = require('yarn-install')

const result = npmOrYarn(['webpack', 'mocha'])
//=> result, returned by child_process.spawnSync
```

## API

### install(dependencies, [options])

#### dependencies

Type: `array`

An array of dependencies to install, you can omit it to install dependencies in `package.json`. If `dependencies` is present, it defaults to `--save` mode.

```js
install(['ava', 'koa'], options)
// or
install(options)
```

#### options

##### registry

Type: `string`  

Specfic a custom npm registry to use.

##### saveDev

Type: `boolean`

Use `--dev` for Yarn and `--save-dev` for npm.

##### global

Type: `boolean`

Install globally, stands for `--global`.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## License

[MIT](https://egoist.mit-license.org/) © [EGOIST](https://github.com/egoist)