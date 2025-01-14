# Changelog

## [0.4.0.0] - 2021-09-02

### Added

* The `--debug` option.

### Changed

* Redid the entire flags parsing.
  This should be backward compatible, and result in a nicer `--help` overview.

## [0.3.0.3] - 2021-08-07

### Changed

* Show the total number of examples in the output as well

## [0.3.0.2] - 2021-07-06

### Changed

* Accept options using American spelling as well.

## [0.3.0.1] - 2021-06-20

### Changed

* Turned off shrinking when using `around` and friends. See https://github.com/nick8325/quickcheck/issues/331.

## [0.3.0.0] - 2021-06-17

### Added

* An `IsTest (ReaderT env IO a)` instance.

### Deleted

* `Test.Syd.Def.Env`, which contained `eit` and `withTestEnv`
  Now that `ReaderT env IO a` is also in `IsTest`, you can just use `it` for this.

## [0.2.0.0] - 2021-06-03

### Added

* `beforeWith` and `beforeWith'`
* `scenarioDir` and `scenarioDirRecur` for scenario testing.
* `bracketSetupFunc`

### Changed

* The `SetupFunc` has been simplified to only take one type parameter.

### Deleted

* `composeSetupFunc`, now obsolete: use `<=<` instead.
* `connectSetupFunc`, now obsolete: use `>=>` instead.
* `wrapSetupFunc`, now entirely obsolete.
* `unwrapSetupFunc`, now entirely obsolete.
* `makeSimpleSetupFunc`, now obsolete: Use the `SetupFunc` constructor directly.
* `useSimpleSetupFunc`, now obsolete: Use the `unSetupFunc` function directly.

## [0.1.0.0] - 2021-03-07

Various fixes

## [0.0.0.0] - 2020-12-26

Initial release
