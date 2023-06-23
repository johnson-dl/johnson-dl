
# Hi, I’m Devin!

<!-- badges: start -->
<!-- badges: end -->

I’m a Data Scientist with experience working in academic, private, and
non-profit research. I work mostly in R but am comfortable with Python
and enjoy working in SQL. I’m currently pursuing a PhD in Experimental
Psychology, conducting experiments and learning how to leverage existing
data to understand human as well as organizational behavior.

I like writing code

``` r
#Simulation for power analysis

#Compute SD for medium effect (Cohen's D of .5)
sd_for_sim <- solve(0.5, 1)

#Generate number of simulations and n per group
n_sims <- 100
n_per_group = 80

#create empty vector of p values
p_vals <- c()



for(i in 1:n_sims){
  control_group <- rnorm(n = n_per_group, 
                         mean =  0, 
                         sd = sd_for_sim)
  
  experimental_group <- rnorm(n = n_per_group, 
                              mean = 1, 
                              sd = sd_for_sim)
  
  
  p_vals[i] <- t.test(control_group, experimental_group)$p.value
}

statistical_power <- mean(p_vals < .05)
statistical_power
#> [1] 0.81
```

and making plots

![](README_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->
