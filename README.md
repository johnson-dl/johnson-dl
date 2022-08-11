
# Hi, I’m Devin

<!-- badges: start -->
<!-- badges: end -->

I work in Data Science and Research Psychology. I’m excited about
learning and teaching all things programming, statistics. I work mostly
in R but am comfortable with Python and enjoy working in SQL.

I like to write code - mostly in R

``` r
#Simulation for power analysis
set.seed(123)
n_sims <- 100

p_vals <- c()

for(i in 1:n_sims){
  control_group <- rnorm(15, 1,.5)
  experimental_group <- rnorm(15, 1.5,.5)
  p_vals[i] <- t.test(control_group, experimental_group, var.equal = TRUE, conf.int = .95)$p.value
}

statistical_power <- mean(p_vals < .05)
statistical_power
#> [1] 0.74
```

I’m also passionate about good science communication and finding the
most efficient ways to communicate to other data professionals as well
as non-techincal data consumers
![](README_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->
