# SYNOPSIS  
[![Build Status](https://img.shields.io/travis/vaporyjs/vaporyjs-testing.svg?branch=master&style=flat-square)](https://travis-ci.org/vaporyjs/vaporyjs-testing)
[![Gitter](https://img.shields.io/gitter/room/vapory/vaporyjs-lib.svg?style=flat-square)]() or #vaporyjs on freenode  

[![js-standard-style](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/feross/standard)

Testing utilities for the vaporyjs stack.

Uses the offical [Vapory Tests](https://github.com/vaporyco/tests).

To fetch the latest tests:
```
git submodule init
git submodule update
cd tests
git pull origin develop
```

## API

```
const testing = require('vaporyjs-testing')
```

#### `testing.getTestsFromArgs(testType, onFile, args = {})`
Reads tests of a certain test type from several folders and files
- `testType` - Type of the test (``GeneralStateTests``, ``BlockchainTests``, ``VMTests``)
- `onFile` - Function to run the tests (see example)
- `args`
  - `forkConfig` - Run tests for selected fork (``BlockchainTests`` only)
  - `dir` - Only run tests from subdirectory
  - `file` - File filter to apply
  - `excludeDir` - Exclude directory filter to apply
  - `test` - Only run a single test case
  - `testsPath` - Path to the tests repository (without the ``tests`` dir)
  - `skipTests` - List of tests to skip
  - `skipVM` - List of VM tests to skip

#### `testing.getTestFromSource(file, onFile)`
Reads custom test from a relative path or file
- `file` - Relative path or filename
- `onFile` - Function to run the tests (see example)

#### `testing.getSingleFile(file)`
Reads a single test file
- `file` - Path to the file


Examples how to read tests with the API methods above can be found in 
the [./examples](./examples/) directory.
  
