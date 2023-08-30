


# rstack

> Stack data type as an 'R6' class

[![Project Status: Active - The project has reached a stable, usable state and is being actively developed.](http://www.repostatus.org/badges/latest/active.svg)](http://www.repostatus.org/#active)
[![Linux Build Status](https://travis-ci.org/gaborcsardi/rstack.svg?branch=main)](https://travis-ci.org/gaborcsardi/rstack)
[![Windows Build status](https://ci.appveyor.com/api/projects/status/github/gaborcsardi/rstack?svg=true)](https://ci.appveyor.com/project/gaborcsardi/rstack)
[![](http://www.r-pkg.org/badges/version/rstack)](http://www.r-pkg.org/pkg/rstack)
[![CRAN RStudio mirror downloads](http://cranlogs.r-pkg.org/badges/rstack)](http://www.r-pkg.org/pkg/rstack)
[![Coverage Status](https://img.shields.io/codecov/c/github/gaborcsardi/rstack/main.svg)](https://codecov.io/github/gaborcsardi/rstack?branch=main)

An extremely simple stack data type, implemented with 'R6' classes. The size
of the stack increases as needed, and the amortized time complexity is O(1).
The stack may contain arbitrary objects.

## Installation


```r
source("https://install-github.me/gaborcsardi/rstack")
```

## Usage


```r
library(rstack)
S <- stack$new()
S$push(1L)
S$peek()
```

```
#> [1] 1
```

```r
S$pop()
```

```
#> [1] 1
```

```r
S$size()
```

```
#> [1] 0
```


```r
S$push(NULL)
S$push(iris)
colnames(S$pop())
```

```
#> [1] "Sepal.Length" "Sepal.Width"  "Petal.Length" "Petal.Width" 
#> [5] "Species"
```

```r
S$peek()
```

```
#> NULL
```

## License

MIT © [Mango Solutions](https://github.com/mangothecat), [Gábor Csárdi](https://github.com/gaborcsardi)
