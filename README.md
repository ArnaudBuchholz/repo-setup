# Repository setup

> This document summarizes the things to apply when creating / updating a node.js repo

## `README.md`

* Badges
  * Node.js CI (get badge from GitHub)
  * ![Mutation Testing](https://img.shields.io/badge/mutation%20testing-100%25-green) *(if any)*
    * if pages are used <br/>
      `[![Mutation Testing](https://img.shields.io/badge/mutation%20testing-100%25-green)](https://arnaudbuchholz.github.io/<PROJECT>/reports/mutation/mutation.html)`
    * otherwise <br />
      `![Mutation Testing](https://img.shields.io/badge/mutation%20testing-100%25-green)`
  * ![no dependencies](https://img.shields.io/badge/-no_dependencies-green) <br/>
    `![no dependencies](https://img.shields.io/badge/-no_dependencies-green)`
  * [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com) <br/>
    `[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)`
  * If published
    * `[![Package Quality](https://npm.packagequality.com/shield/<PACKAGE_NAME>.svg)](https://packagequality.com/#?package=<PACKAGE_NAME>)`
    * `[![Known Vulnerabilities](https://snyk.io/test/github/ArnaudBuchholz/<PROJECT>/badge.svg?targetFile=package.json)](https://snyk.io/test/github/ArnaudBuchholz/<PROJECT>?targetFile=package.json)`
    * `[![PACKAGE_NAME](https://badge.fury.io/js/PACKAGE_NAME.svg)](https://www.npmjs.org/package/PACKAGE_NAME)`
    * `[![PACKAGE_NAME](http://img.shields.io/npm/dm/PACKAGE_NAME.svg)](https://www.npmjs.org/package/PACKAGE_NAME)`
    * ` [![install size](https://packagephobia.now.sh/badge?p=PACKAGE_NAME)](https://packagephobia.now.sh/result?p=PACKAGE_NAME)`
  * [![MIT License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) <br/>
    `[![MIT License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)`
  * ![Documentation](https://img.shields.io/badge/-documentation-blueviolet) *(if not README)* <br/>
    `[![Documentation](https://img.shields.io/badge/-documentation-blueviolet)](https://github.com/ArnaudBuchholz/<PROJECT>/tree/master/README.md)`

* Sections
  * 📚 Documentation
  * 💿 How to install
  * 🖥️ How to demo
  * ⚖️ License
  * ⚠️ Breaking changes

## `package.json`

* expected scripts :
  * `build` *(if needed)*
  * `test`
  * `lint`
  * `mutate` (if `stryker` is used)

* Remove noise (remember that it is published)
  * Isolate jest settings in a [configuration file](https://jestjs.io/docs/configuration)
  * Pass linter settings in the command line (`standard --env jest`)
