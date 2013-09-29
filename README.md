# grunt-protractor-runner

> A grunt task to run [Protractor](https://github.com/angular/protractor).

## Getting Started
This plugin requires Grunt `~0.4.1`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-protractor-runner --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-protractor-runner');
```

## The "protractor" task

### Overview
In your project's Gruntfile, add a section named `protractor` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  protractor: {
    options: {
      configFile: "node_modules/protractor/referenceConf.js"
      args: {
        // Arguments passed to the command
      }
    },
    your_target: {
      // Target-specific file lists and/or options go here.
    },
  },
})
```

### Options

#### options.configFile
Type: `String`
Default value: `node_modules/protractor/referenceConf.js`

A protractor config file.

#### options.args
Type: `Object`
Default value: `{}`

Arguments passed to the command. Supported arguments are below.

* seleniumAddress <string>: A running selenium address to use
* seleniumServerJar <string>: Location of the standalone selenium server .jar file
* seleniumPort <string>: Optional port for the standalone selenium server
* baseUrl <string>: URL to prepend to all relative paths
* rootElement <string>: Element housing ng-app, if not html or body
* specs <array>: Array of spec files to test. Ex. ["spec1.js","spec2.js"]
* includeStackTrace <boolean>: Print stack trace on error
* verbose <boolean>: Print full spec names

## Tests

After `npm install`, you need to run script `node_modules/protractor/bin/install_selenium_standalone` to download
selenium to `selenium/`. 

Then run `grunt` to test the module. If it runs fine and open chrome a couple of times without warning or errors, it means success although it prints `0 tests, 0 assertions, 0 failures`.

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

