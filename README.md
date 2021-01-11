
<!-- README.md is generated from README.Rmd. Please edit that file -->

[English](README.md) | [日本語](README_JP.md)

# seq.geometric

<!-- badges: start -->

<!-- badges: end -->

`{seq.geometric}` is function to generate a sequence of equal ratios,
also known as a geometric sequence.

## Installation

You can install of `{seq.geometric}` from Github with:

``` r
install.packages("remotes")
remotes::install_github("indenkun/seq.geometric")
```

## Example

``` r
library(seq.geometric)
```

By specifying the first term in `from`, the last term or the closest
value to the last term in `to`, and the common ratio in `by.rate`, you
can obtain an geometric sequence of “first term \* common ratio ^ n”
from “from” to the closest value to “to”.

``` r
seq_geometric(from = 1, to = 128, by.ratio = 2)
#> [1]   1   2   4   8  16  32  64 128
```

Returns an error if the geometric sequence does not converge with the
specified argument.

``` r
seq_geometric(from = 1, to = 100, by.ratio = 0.1)
#> Error: The calculation results do not converge.
```

You can also specify the length of the sequence you want as an argument
to `lenght.out`.

``` r
seq_geometric(from = 1, to = 128, by.ratio = 2, length.out = 3)
#> [1] 1 2 4
```

## License

MIT.

## Notice

The email address listed in the DESCRIPTION is a dummy. If you have any
questions, please post them on ISSUE.
