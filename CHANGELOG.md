# CHANGELOG

## 9.0.2 / 2021-03-16

* Handle null enums

## 9.0.0 / 2021-02-03

* Better naming for pluralized words

## 8.4.8 / 2022-01-10

* Mongoose 6 support

## 8.4.7 / 2021-12-10

* Parse JSDocs from Mongoose Schemas and copy into generated files.

## 8.4.0 / 2021-09-27

* Handle nested query population

## 8.3.3 / 2021-05-21

* Typesafe query population

## 8.3.0 / 2021-05-21

* Fix plural naming

## 8.2.0 / 2021-05-19

* Added `mongoose.Query.populate` overload to narrow query typings & `--no-populate-overload` flag to disable the behaviour
* Added new population helper types and type guards `PopulatedDocument`, `IsPopulated`
* Update to Mongoose 5.12.10

## 8.1.0 / 2021-05-17

* Added `--no-mongoose` flag to generate types without mongoose references. This option removes document types and replaces ObjectId with string #7

## 8.0.0 / 2021-04-29

* Removed need to typecast method, static and query objects (this was required to support function types)
* Query types can now be passed as a generic to the Mongoose model constructor. This greatly simplifies query typing
* Update to Mongoose 5.12.6
* remove CLI options:
  - `--js` (generator depends too much on TS compiler libraries now, so using this with JS has very limited functionality. Convert type files to TS before using mongoose-tsgen moving forward)
  - `--augment` (added much unnecessary complexity, functionality can be achieved using a simple user-created file)
  - `--no-func-types` (this was mainly used to avoid using TS compiler API when running the generator. These days the generator depends on the TS compiler API for all basic functions so this option has no use)
* Use [new Mongoose type updates & fixes](https://github.com/Automattic/mongoose/blob/master/History.md) ([5.11.13](https://github.com/Automattic/mongoose/blob/master/History.md#51113--2021-01-20) and on)
* Added `--debug` flag to print useful debug info
