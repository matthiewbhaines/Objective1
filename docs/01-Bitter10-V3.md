---
output: html_document
editor_options: 
  chunk_output_type: console
---
# 1:10 Bitterness {#Bitter10}

This will be the data analysis and results of the 1:10 nose closed study run in December 2024 and the 1:10 nose open study run in September 2023.  

A 1:10 brew strength (coffee:water, w/w) is representative of a strong ratio used by everyday consumers. Our hypotheses was:  

> Milk will reduce the bitterness of cold brew coffee more than water  

This hypothesis is thought to be seen regardless of condition (nose closed or nose open). 

Some interpretations of expected data would be:

- In the nose closed condition a reduction in bitterness from the milky coffee would suggest a physicochemical interaction between the milk and coffee  
- Milk, being 86% water [@walstraDairyTechnologyPrinciples1999] could have a similar effect as water would when added to coffee   
- In the nose opened condition, a reduction in bitterness from the milky coffee could suggest a cross-modal interaction (particularly if no effect is seen in the nose closed condition) 

> Inclusion criteria included drinking coffee at least once a month.



## Nose Closed Condition
### Participant Data

``` r
Study1Meta <- read_xlsx(path = "Objective1CompiledDataWithIndex.xlsx", sheet = 4) %>% clean_names()
colnames(Study1Meta)
```

```
##  [1] "panelist_code"         "age"                   "gender"               
##  [4] "indian_alaskan"        "asian_indian_islander" "black"                
##  [7] "white"                 "hispanic_latino"       "other"                
## [10] "consumption"           "sweetener"             "whitener"             
## [13] "how_white"
```

``` r
Study1Meta %>% filter(consumption == "6") #osu27
```

```
## # A tibble: 1 × 13
##   panelist_code   age gender indian_alaskan asian_indian_islander black white
##   <chr>         <dbl>  <dbl>          <dbl>                 <dbl> <dbl> <dbl>
## 1 osu27            29      2              0                     1     0     0
## # ℹ 6 more variables: hispanic_latino <dbl>, other <dbl>, consumption <dbl>,
## #   sweetener <dbl>, whitener <dbl>, how_white <dbl>
```

``` r
# 1 - daily; 2 - 2-3/wk; 3- 1/wk
# 4 - 2-3/mo; 5 - 1/mo; 6 <1/mo

Study1MetaInc <- Study1Meta %>% filter(panelist_code != "osu27")
describe(Study1MetaInc)[2,] %>% select(mean, sd, median, min, max) #age
```

```
##      mean   sd median min max
## age 30.14 12.1     26  22  86
```

``` r
Study1MetaInc %>% count(gender) # 11 males, 18 females
```

```
## # A tibble: 2 × 2
##   gender     n
##    <dbl> <int>
## 1      1    11
## 2      2    18
```

``` r
Study1MetaInc %>% group_by(sweetener, whitener) %>% 
  tally() %>% 
  spread(whitener, n) %>% 
  replace(is.na(.), 0)
```

```
## # A tibble: 2 × 3
## # Groups:   sweetener [2]
##   sweetener   `1`   `2`
##       <dbl> <int> <int>
## 1         1    14     0
## 2         2    10     5
```

``` r
# 11 - whiten and sweeten
# 12 - whiten, no sweeten
# 21 - sweeten, no whiten
# 22 - black coffee drinker

Study1MetaInc %>% count(consumption)
```

```
## # A tibble: 5 × 2
##   consumption     n
##         <dbl> <int>
## 1           1    18
## 2           2     5
## 3           3     2
## 4           4     3
## 5           5     1
```

``` r
# 1 - daily; 2 - 2-3/wk; 3- 1/wk
# 4 - 2-3/mo; 5 - 1/mo; 6 <1/mo
```

- one participant (F) drank coffee less frequently than once a month. therefore they will be removed






### R Index  
In the paired comparisons between when skim milk or whole milk was added to the coffee, there is not enough evidence to suggest one will reduce the bitterness more than the other [cf. @keastModificationBitternessCaffeine2008].  

02032025: I guess, according to @keastModificationBitternessCaffeine2008, the whole milk would be the signal, as it would be expected to be more bitter than the skim milk (again, based solely on this paper). 

The critical value for a 2-tailed test is **0.62**.  



- discrimination seen between when 8% skim milk and 8% whole milk was added to coffee (R Index = 0.35, p $\leq$ **0.05**)  
    + interestingly, the skim milk sample (the "noise") was chosen more frequently than the whole milk sample (the "signal"): 19/29



- no discrimination between 17% skim milk or 17% whole milk added to coffee (R Index (*_S*) = 0.57, p > 0.05)  


<div class="figure">
<img src="01-Bitter10-V3_files/figure-html/study1ClosedMilkRViz-1.png" alt="R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose closed condition. The Skim Milk R-index is positioned above the thick horizontal line; the Whole Milk R-index is positioned below. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the skim milk sample ('Signal') was significant; White bars indicate the whole milk sample ('Noise') was significant (p &lt; 0.05). All significance at alpha = 0.10 is noted." width="672" />
<p class="caption">(\#fig:study1ClosedMilkRViz)R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose closed condition. The Skim Milk R-index is positioned above the thick horizontal line; the Whole Milk R-index is positioned below. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the skim milk sample ('Signal') was significant; White bars indicate the whole milk sample ('Noise') was significant (p < 0.05). All significance at alpha = 0.10 is noted.</p>
</div>

For the paired comparisons between milk and water, we hypothesized that the addition of milk would reduce the bitterness, therefore making the water sample the more bitter sample. The critical value for a one tailed R-index calculation is **0.62**.  





- marginal discrimination seen between when 8% skim milk and 8% water was added to coffee (R Index = 0.61, p < *0.10*)  

   + interestingly, the skim milk sample (the "noise") was chosen more frequently than the water sample (the "signal"): 18/29

- discrimination seen between when 8% whole milk and 8% water was added to coffee (R Index = 0.63, p $\le$ **0.05**)   


- no discrimination between the 17% skim milk and 17% water samples (R Index = 0.5, p > 0.05)  
- no discrimination between the 17% whole milk and 17% water samples (R Index = 0.44, p > 0.05)  


<div class="figure">
<img src="01-Bitter10-V3_files/figure-html/study1ClosedWaterRViz-1.png" alt="R Index of paired comparison between skim milk, whole milk, and water at an 8% addition level and 17% addition level in a nose closed condition. The Milk R-indices are positioned above the thick horizontal line; the water R-index is positioned below. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p &lt; 0.05). All significance at alpha = 0.10 is noted." width="672" />
<p class="caption">(\#fig:study1ClosedWaterRViz)R Index of paired comparison between skim milk, whole milk, and water at an 8% addition level and 17% addition level in a nose closed condition. The Milk R-indices are positioned above the thick horizontal line; the water R-index is positioned below. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p < 0.05). All significance at alpha = 0.10 is noted.</p>
</div>

- Interestingly, only comparisons at the 8% addition level reached significance
    + the skim milk sample was chosen as more bitter compared to the whole milk sample (Figure \@ref(fig:study1ClosedMilkRViz))  
    + the water sample was chosen as more bitter compared to the whole milk sample (Figure \@ref(fig:study1ClosedWaterRViz), red bar)
    
- This is somewhat counter intuitive to what we had hypothesized, as adding more milk (the 17% samples) should have also shown discrimination  
    + what are alternative interpretations/explanations?
      + *01092025*: could fat be creating an inhibitive coating on the tongue where bitter compounds can't connect to the receptors?
      +*01142025*: the skim milk being perceived as more bitter could be a type I error, a false positive  
      + *02032025*: it is counter to a physicochemical-based hypothesis, it is also unintuitive why significance is only seen at an 8% level (marginal with skim milk being more bitter than water (cf. @keastModificationBitternessCaffeine2008), the whole milk being less bitter than water)
