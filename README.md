paraunit
========

A parallel wrapper for PHPUnit. Run this file instead of PHPUnit and you can
pass in the number of parallel PHPUnit processes you want to use on your tests.

Tests are found by grepping files for test*() and run in individual processes,
up to the max concurrency you set, until all tests are finished. This means
_tests must be logically independent!_

Usage
-----
Install using composer. Then do this:

```vendor/bin/paraunit (-pPROCESSES|--processes=PROCESSES) --path=TEST_PATH/TEST_GLOB
--phpunit=PATH/TO/PHPUNIT```

Todo
----
* Handle more kinds of output from phpunit
* Try to use PHPUnit to get file list / test name list
* See if anything can be done about test dependencies
