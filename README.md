
# rstack

> Stack data type as an ‘R6’ class

[![Project Status: Active - The project has reached a stable, usable
state and is being actively
developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
[![R-CMD-check](https://github.com/gaborcsardi/rstack/actions/workflows/R-CMD-check.yaml/badge.svg)](https://github.com/gaborcsardi/rstack/actions/workflows/R-CMD-check.yaml)
[![](https://www.r-pkg.org/badges/version/rstack)](https://www.r-pkg.org/pkg/rstack)
[![CRAN RStudio mirror
downloads](https://cranlogs.r-pkg.org/badges/rstack)](https://www.r-pkg.org/pkg/rstack)
[![Coverage
Status](https://img.shields.io/codecov/c/github/gaborcsardi/rstack/main.svg)](https://app.codecov.io/github/gaborcsardi/rstack?branch=main)

An extremely simple stack data type, implemented with ‘R6’ classes. The
size of the stack increases as needed, and the amortized time complexity
is O(1). The stack may contain arbitrary objects.

## Installation

``` r
source("https://install-github.me/gaborcsardi/rstack")
```

## Usage

``` r
library(rstack)
S <- stack$new()
S$push(1L)
S$peek()
```

    #> [1] 1

``` r
S$pop()
```

    #> [1] 1

``` r
S$size()
```

    #> [1] 0

``` r
S$push(NULL)
S$push(iris)
colnames(S$pop())
```

    #> [1] "Sepal.Length" "Sepal.Width"  "Petal.Length" "Petal.Width"  "Species"

``` r
S$peek()
```

    #> NULL

## License

MIT © [Mango Solutions](https://github.com/mangothecat), [Gábor
Csárdi](https://github.com/gaborcsardi)
