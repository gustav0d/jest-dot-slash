1. `yarn`
1. `yarn jest --config singular.config.js`
1. `yarn jest --config plural.config.js`

The singular config with `testPathPattern` logs this warning:

```
● Deprecation Warning:

  Option "testPathPattern" was replaced by "testPathPatterns".

  Please update your configuration.

  Configuration Documentation:
  https://jestjs.io/docs/configuration

● Deprecation Warning:

  Option "testPathPattern" was replaced by "testPathPatterns".

  Please update your configuration.

  Configuration Documentation:
  https://jestjs.io/docs/configuration
```

The plural config with `testPathPatterns` logs this warning:

```
● Validation Warning:

  Unknown option "testPathPatterns" with value [/\.test\.js$/] was found.
  This is probably a typing mistake. Fixing it will remove this message.

  Configuration Documentation:
  https://jestjs.io/docs/configuration

● Validation Warning:

  Unknown option "testPathPatterns" with value [/\.test\.js$/] was found.
  This is probably a typing mistake. Fixing it will remove this message.

  Configuration Documentation:
  https://jestjs.io/docs/configuration
```

Both configs run the helper file.

The `--testPathPatterns` CLI flag works without any validation warnings and it does not run the helper file:

```
yarn jest --testPathPatterns=".*\.test\.js$"
```
