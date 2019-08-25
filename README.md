
<!-- README.md is generated from README.Rmd. Please edit that file -->

# mod::ule

<!-- badges: start -->

[![AppVeyor build
status](https://ci.appveyor.com/api/projects/status/github/iqis/mod?branch=master&svg=true)](https://ci.appveyor.com/project/iqis/mod)
[![Travis build
status](https://travis-ci.org/iqis/mod.svg?branch=master)](https://travis-ci.org/iqis/mod)
[![codecov](https://codecov.io/gh/iqis/mod/branch/master/graph/badge.svg)](https://codecov.io/gh/iqis/mod)
[![Lifecycle:
maturing](https://img.shields.io/badge/lifecycle-maturing-blue.svg)](https://www.tidyverse.org/lifecycle/#maturing)
[![CRAN
status](https://www.r-pkg.org/badges/version/mod)](https://cran.r-project.org/package=mod)
![CRAN License](https://img.shields.io/cran/l/mod)

<!-- badges: end -->

The `mod` package provides a simple way to structure program and data
into flexible and independent units for programming and interactive use.
Modules indtroduced by the `mod` package offer the benefit of modules
from other languages, while keeping an authentic R flavor.

## Why?

Programs need to be oraganized into units.

A package is a very robust solution, but is formal and compliated;
packages require additional knowledge to R and must be installed in the
local library by `install.packages()`. On the other hand, simple R
scripts, often executed by `source()`, are brittle and may create
namespace conflict; They are unsuitable for building tools.

Modules fills the hollow middleground by allowing programs to live
separately and work together at the same time. Each module has its own
scope, host is own objects, an can attach different packages without
interefering with each other or the global search path. They can be
created either inline with other programs or from a standalone file, and
can be used in the user’s working environment, as a part of a package,
or in other modules.

## Installation

Install the published version from
[CRAN](https://CRAN.R-project.org/package=mod) with:

``` r
install.packages("mod")
```

Install the development version from [GitHub](https://github.com/) with:

``` r
devtools::install_github("iqis/mod")
```

## Vocabulary

The `mod` package has a simple UI:

  - Make a module:
      - Inline:`module()`/`mod::ule()`
      - From a file: `acquire()`
  - The search path:
      - Attach a module: `use()`
      - Detach a module: `drop()`
  - Inside a module:
      - Declare public objects: `provide()`
      - Attach a package locally: `require()`
      - Copy objects from another module: `refer()`
      - Name the module: `name()`

## Documentation

  - [Introduction to
    Modules](https://iqis.github.io/mod/articles/introduction.html)
