# Handlebars Layouts [![Build Status](https://travis-ci.org/shannonmoeller/handlebars-layouts.png)](https://travis-ci.org/shannonmoeller/handlebars-layouts)

> Allows additional command line options to be registered using [nopt](https://github.com/isaacs/nopt) along with those natively supported by [grunt](http://gruntjs.org).

## Installation

```sh
$ npm install handlebars-layouts
```

## Example

```js
// Gruntfile.js
module.exports = function(grunt) {
    // require it at the top and pass in the grunt instance
    require('nopt-grunt')(grunt);

    // new method now available
    grunt.initOptions({
        // longhand
        foo: {
            info: 'Some flag of interest.',
            type: Boolean
        },

        // shorthand
        bar: [Number, null]
    });

    // reference values as before
    grunt.option('no-foo');

    grunt.initConfig({});
    grunt.registerTask('default', []);
};
```

## License

MIT

[![githalytics.com alpha](https://cruel-carlota.pagodabox.com/ae3a06cc73fded765f8492d78c66ad30 "githalytics.com")](http://githalytics.com/shannonmoeller/handlebars-layouts)
