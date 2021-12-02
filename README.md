## Template for successfully creating and managing an R package

Very basic set-up created with `devtools::create("packageName")`.

## Folder structure 

In order of importance.

### README.md

xyz.

<!-- badges: start -->
<!--
[![CRAN](https://www.r-pkg.org/badges/version/packageName)](https://cran.r-project.org/package=packageName)
[![Downloads](https://cranlogs.r-pkg.org/badges/last-day/packageName?color=ff69b4)](https://www.r-pkg.org/pkg/packageName)
[![Downloads](https://cranlogs.r-pkg.org/badges/packageName?color=ff69b4)](https://www.r-pkg.org/pkg/packageName)
[![Downloads](https://cranlogs.r-pkg.org/badges/grand-total/packageName?color=ff69b4)](https://www.r-pkg.org/pkg/packageName)
-->
<!-- badges: end -->

### R

xyz.

Should contain a `packageName.R` file which has the info about your package and built-in datasets.

Should contain a `utils.R` file with utility functions used within your code, but typically not exported. To make your life easier and the code clearer.

### tests

xyz.

### man

xyz.

### data & data-raw

xyz.

### src

xyz.

### inst

xyz.

## Workflow

### Develop

- `devtools::load_all()`

- `devtools::document()`

### Release

- `devtools::check_win_devel()`

- `devtools::release()`

## Coding style

Whatever you like, as long as it is consistent within the same package. As the main developer, don't be afraid to gently remind contributors of what the preferred style is.
