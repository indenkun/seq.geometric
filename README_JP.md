
<!-- README.md is generated from README.Rmd. Please edit that file -->

[English](README.md) | [日本語](README_JP.md)

# seq.geometric

<!-- badges: start -->

<!-- badges: end -->

`{seq.geometric}`は等比数列を求めるための関数を提供するパッケージです。

## Installation

`{seq.geometric}`はGithubからインストールできます。

``` r
install.packages("remotes")
remotes::install_github("indenkun/seq.geometric")
```

## Example

``` r
library(seq.geometric)
```

`from`で初項を指定し、`to`で最終項か最終項に最も近い値を指定し、`by.rate`で公比を指定することで、"初項\*公比^n“の等比数列を”from“から”to"に最も近い値まで求めることができます。

``` r
seq_geometric(from = 1, to = 128, by.ratio = 2)
#> [1]   1   2   4   8  16  32  64 128
```

求める数列の解が収束しない場合はエラーが出ます。

``` r
seq_geometric(from = 1, to = 100, by.ratio = 0.1)
#> Error: The calculation results do not converge.
```

求める数列の長さを`length.out`で指定することもできます。

``` r
seq_geometric(from = 1, to = 128, by.ratio = 2, length.out = 3)
#> [1] 1 2 4
```

## License

MIT.

## Notice

DESCRIPTIONに記載しているメールアドレスはダミーです。なにかあればISSUEに記載してください。
