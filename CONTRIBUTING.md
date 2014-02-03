# How to contribute

Please follow the general instruction on LoopBack's 
[How To Contribute](https://github.com/strongloop/loopback/wiki/How-To-Contribute) 
wiki.

## Code style

We use JSHint to ensure our coding style stays consistent. You can check
the conformance by running the following command:

    $ jshint .

## Automated tests

loopback-angular comes with two kinds of tests:

### End-to-end test in Karma

We are using [karma](http://karma-runner.github.io/) to test the generated
Angular services. See
[test.e2e/](https://github.com/strongloop/loopback-angular/tree/master/test.e2e)
and
[test.e2e/spec/services.spec.js](https://github.com/strongloop/loopback-angular/blob/master/test.e2e/spec/services.spec.js).

Use the following setup while working on a new feature:

 1. Start a test server in the background:

        $ node test.e2e/test-server

  The test server provides HTTP API for building a temporary loopback 
  application, generating Angular services file for this application
  and finally exposing the application on an URL accessible from
  karma tests.

 2. Start the karma runner in the background:

        $ karma run

  Karma will continually monitor project files and re-run tests every time
  you make a change.

### Tests for CLI tools in Mocha

CLI tools like `bin/lb-ng` are tested using plain Mocha tests. See
[test/](https://github.com/strongloop/loopback-angular/tree/master/test)
and
[test/lb-ng.test.js](https://github.com/strongloop/loopback-angular/blob/master/test/lb-ng.test.js).
