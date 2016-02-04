karma-jasmine-style-specrunner-reporter
=======================

## A karma plugin for exporting unit test results as styled HTML file

This is a plugin for the [Karma Test Runner]. By adding this reporter to your karma configuration, unit test results will be exported as a styled HTML file. For each test browser, a separate table is generated. The plugin is  based on the [karma-junit-reporter plugin].

## Installation

The easiest way is to keep `karma-jasmine-style-specrunner-reporter` as a devDependency in your `package.json`.
```json
{
  "devDependencies": {
    "karma": "~0.10",
    "karma-htmlfile-reporter": "latest"
  }
}
```

You can simple do it by:
```bash
npm install karma-jasmine-style-specrunner-reporter --save-dev
```

It may also be necessary to install globally:
```bash
npm install -g karma-jasmine-style-specrunner-reporter
```

## Configuration
```js
// karma.conf.js
module.exports = function(config) {
  config.set({
    reporters: ['progress', 'html'],

    htmlReporter: {
      outputFile: 'tests/units.html',
			
      // Optional
      pageTitle: 'Unit Tests',
      subPageTitle: 'A sample project description'
    }
  });
};
```

You can pass list of reporters as a CLI argument too:
```bash
karma start --reporters html
```

----

For more information on Karma see the [homepage].

[Karma Test Runner]: https://github.com/karma-runner/karma
[karma-junit-reporter plugin]: https://github.com/karma-runner/karma-junit-reporter
[homepage]: http://karma-runner.github.com
