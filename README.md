# karma-threshold-reporter

> Fail the build if the coverage falls below a pre configured value

## Installation

The easiest way is to keep `karma-threshold-reporter` as a devDependency in your `package.json`.
```json
{
  "devDependencies": {
    "karma": "~0.10",
    "karma-threshold-reporter": "~0.1.6"
  }
}
```

You can simple do it by:
```bash
npm install karma-threshold-reporter --save-dev
```

## Configuration
```js
// karma.conf.js
module.exports = function(config) {
  config.set({
  
    plugins: ['karma-threshold-reporter'],
  
    reporters: ['progress', 'coverage','threshold'],

    // the default configuration
    thresholdReporter: {
      statements: 90,
      branches: 60,
      functions: 85,
      lines: 90
    }
  });
};
```

You can pass list of reporters as a CLI argument too:
```bash
karma start --reporters coverage,threshold
```

----

For more information on Karma see the [homepage].

[homepage]: http://karma-runner.github.com
