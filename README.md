# The (holy) structure of an R package

Want to get started quickly? Fork this repository, rename the package, and off you go.

You could also start by creating a very basic setup running `devtools::create("packageName")`, and adding other folders as required.

## Folders 

In order of importance.

### R

All your wonderful code nicely organized into various scripts.

Should contain a `packageName.R` file which has the info about your package and built-in datasets.

Should contain a `utils.R` file with utility functions used within your code, but typically not exported. To make your life easier and the code cleaner.

### tests

Your unit tests. Your testing workflow is best managed with the package **`testthat`**. 

### man

Your documentation is automatically put here when you run `devtools::document()`.

### data & data-raw

In case your package ships one or more built-in datasets, they should be put in **data**. The scripts to create them, if any, can be put in **data-raw**.

### .github

Where you define your GitHub Actions for CI/CD pipelines.

### src

A storage for your C++ or other low-level source code.

### inst

Files (such as how to cite your package) that become available when the package is installed go here.

## Auxiliary files 

- README.md

Your cool marketing material!

<!-- badges: start -->
<!--
[![CRAN](https://www.r-pkg.org/badges/version/packageName)](https://cran.r-project.org/package=packageName)
[![Downloads](https://cranlogs.r-pkg.org/badges/last-day/packageName?color=ff69b4)](https://www.r-pkg.org/pkg/packageName)
[![Downloads](https://cranlogs.r-pkg.org/badges/packageName?color=ff69b4)](https://www.r-pkg.org/pkg/packageName)
[![Downloads](https://cranlogs.r-pkg.org/badges/grand-total/packageName?color=ff69b4)](https://www.r-pkg.org/pkg/packageName)
-->
<!-- badges: end -->

- DESCRIPTION

Your boring marketing material!

- .gitignore

What files to "ghost" when you push to Git(Hub).

- .Rbuildignore

What files not to consider when you build your package, and upload it to CRAN.

## Workflow

### Develop

- `devtools::load_all()`

- `devtools::document()`

Generates a NAMESPACE file.

- `devtools::test()`

#### Tips

Collaborate making use of the Issues tracker and a branching strategy. Doing your work out in the open is strongly encouraged!

Use the package **`usethis`** throughout when needed.

### Release

- `devtools::check()`

- `devtools::check_win_devel()`

- `devtools::release()`

## Coding style

Whatever you like, as long as it is consistent within the same package. As the main developer, don't be afraid to gently remind contributors of what the preferred style is.

## Reference material

Hadley Wickham's book [R packages](https://r-pkgs.org/). This [blog post](https://gontcharov.be/blog/analysis-r-package) is also a good and simple breakdown, more focused on "analysis-as-a-package".
