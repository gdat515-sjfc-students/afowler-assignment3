``` r
data.table::fread("./o-ring-erosion-or-blowby.data") -> ring.data

# The space shuttle crashed landed but there were concerns before the flight that they shouldn't fly the shuttle. They didnt do a good job of data visualization and relaying their point so our job is to give god visualization of why they should fly.

ggplot(ring.data, aes(x = TEMPORDFLIGT, y = THERMALDIS, size = LAUNCHTEMP))+
  geom_point() +
  xlab("Temporal order of flight")+
  ylab("# of O-Rings experiencing thermal distress")
```

![](assignment3_files/figure-markdown_github/unnamed-chunk-1-1.png)

``` r
  ggtitle("Number of O-rings at risk", subtitle = "Number of O-rings that will experience thermal distress for a given flight when the launch temperature is below freezing")
```

    ## $title
    ## [1] "Number of O-rings at risk"
    ## 
    ## $subtitle
    ## [1] "Number of O-rings that will experience thermal distress for a given flight when the launch temperature is below freezing"
    ## 
    ## attr(,"class")
    ## [1] "labels"

``` r
# The cause of the disaster was traced to an O-ring, a circular gasket that sealed the right rocket booster. This had failed due to the low temperature (31°F / -0.5°C) at launch time – a risk that several engineers noted, but that NASA management dismissed. 
```
