# 1:10 Bitterness {#Bitter10}

This will be the data analysis and results of the 1:10 nose closed study run in December 2024 and the 1:10 nose open study run in September 2023.  

A 1:10 brew strength (coffee:water, w/w) is representative of a strong ratio used by everyday consumers. Our hypotheses was:  

> Milk will reduce the bitterness of cold brew coffee more than water  

This hypothesis is thought to be seen regardless of condition (nose closed or nose open). 

Some interpretations of expected data would be:

- In the nose closed condition a reduction in bitterness from the milky coffee would suggest a physicochemical interaction between the milk and coffee  
- Milk, being 86% water [@walstraDairyTechnologyPrinciples1999] could have a similar effect as water would when added to coffee   
- In the nose opened condition, a reduction in bitterness from the milky coffee could suggest a cross-modal interaction (particularly if no effect is seen in the nose closed condition) 

## Nose Closed Condition






### R Index  
In the paired comparisons between when skim milk or whole milk was added to the coffee, there is not enough evidence to suggest one will reduce the bitterness more than the other [cf. @keastModificationBitternessCaffeine2008].  

The critical value for a 2-tailed test is **0.62**.  



- discrimination seen between when 8% skim milk and 8% whole milk was added to coffee (R Index = 0.66, p $\leq$ **0.05**)  
    + interestingly, the skim milk sample (the "noise") was chosen more frequently than the whole milk sample (the "signal"): 20/30



- no discrimination between 17% skim milk or 17% whole milk added to coffee (R Index = 0.58, p > 0.05)  


<div class="figure">
<img src="01-Bitter10_files/figure-html/study1ClosedMilkRViz-1.png" alt="R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose closed condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p &lt; 0.05)." width="672" />
<p class="caption">(\#fig:study1ClosedMilkRViz)R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose closed condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p < 0.05).</p>
</div>

For the paired comparisons between milk and water, we hypothesized that the addition of milk would reduce the bitterness, therefore making the water sample the more bitter sample. The critical value for a one tailed R-index calculation is **0.62**.  




- discrimination seen between when 8% skim milk and 8% water was added to coffee (R Index = 0.63, 0.05 $\ge$ p $\ge$ 0.01)  

   + interestingly, the skim milk sample (the "noise") was chosen more frequently than the water sample (the "signal"): 19/30

- discrimination seen between when 8% whole milk and 8% water was added to coffee (R Index = 0.65, 0.05 $\ge$ p $\ge$ 0.01)   


- no discrimination between the 17% skim milk and 17% water samples (R Index = 0.52, p > 0.05)  
- no discrimination between the 17% whole milk and 17% water samples (R Index = 0.53, p > 0.05)  


<div class="figure">
<img src="01-Bitter10_files/figure-html/study1ClosedWaterRViz-1.png" alt="R Index of paired comparison between skim milk and water at an 8% addition level and 17% addition level in a nose closed condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p &lt; 0.05)." width="672" />
<p class="caption">(\#fig:study1ClosedWaterRViz)R Index of paired comparison between skim milk and water at an 8% addition level and 17% addition level in a nose closed condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p < 0.05).</p>
</div>

- Interestingly, only comparisons at the 8% addition level reached significance
    + the skim milk sample was chosen as more bitter compared to the whole milk sample (Figure \@ref(fig:study1ClosedMilkRViz))  
    + the skim milk sample was chosen as more bitter compared to the water sample (Figure \@ref(fig:study1ClosedWaterRViz), white bar)
    + the water sample was chosen as more bitter compared to the whole milk sample (Figure \@ref(fig:study1ClosedWaterRViz), red bar)
    
- This is somewhat counter intuitive to what we had hypothesized, as adding more milk (the 17% samples) should have also shown discrimination  
    + what are alternative interpretations/explanations?
      + *01092025*: could fat be creating an inhibitive coating on the tongue where bitter compounds can't connect to the receptors?

### Ratings  
The paired comparison will only show which sample is more bitter (or discriminated against), without showing a magnitude of the difference. Thus, bitterness intensity ratings were recorded as well. They will be analyzed by paired t-test with a Bonferroni correction against multiple comparisons.  




Table: (\#tab:study1-kable-closed-ratings)Bitterness intensities and standard error of cold brew coffee samples. Each 2 rows represent the two samples presented in a paired comparison format.

|Sample        | Intensity|        se|
|:-------------|---------:|---------:|
|bitterness_13 |  5.583333| 0.3903162|
|bitterness_15 |  5.666667| 0.4257065|
|bitterness_14 |  5.190000| 0.4044394|
|bitterness_17 |  5.416667| 0.3374033|
|bitterness_16 |  5.100000| 0.3763100|
|bitterness_18 |  5.383333| 0.3454826|
|bitterness_19 |  6.400000| 0.3890749|
|bitterness_21 |  5.616667| 0.3958719|
|bitterness_20 |  5.933333| 0.3249521|
|bitterness_23 |  5.416667| 0.3968868|
|bitterness_22 |  5.550000| 0.3493426|
|bitterness_24 |  5.800000| 0.3870014|



The Bonferroni corrected $\alpha$ would be **0.0167**.


``` r
t.test(df10closed$bitterness_19, df10closed$bitterness_21, 
       paired = TRUE, alternative = "two.sided") 

	Paired t-test

data:  df10closed$bitterness_19 and df10closed$bitterness_21
t = 1.9067, df = 29, p-value = 0.06651
alternative hypothesis: true mean difference is not equal to 0
95 percent confidence interval:
 -0.05691393  1.62358059
sample estimates:
mean difference 
      0.7833333 
t.test(df10closed$bitterness_23, df10closed$bitterness_20, 
       paired = TRUE, alternative = "greater")

	Paired t-test

data:  df10closed$bitterness_23 and df10closed$bitterness_20
t = -1.168, df = 29, p-value = 0.8738
alternative hypothesis: true mean difference is greater than 0
95 percent confidence interval:
 -1.268288       Inf
sample estimates:
mean difference 
     -0.5166667 
t.test(df10closed$bitterness_24, df10closed$bitterness_22, 
       paired = TRUE, alternative = "greater")

	Paired t-test

data:  df10closed$bitterness_24 and df10closed$bitterness_22
t = 0.54603, df = 29, p-value = 0.2946
alternative hypothesis: true mean difference is greater than 0
95 percent confidence interval:
 -0.527945       Inf
sample estimates:
mean difference 
           0.25 


t.test(df10closed$bitterness_13, df10closed$bitterness_15, 
       paired = TRUE, alternative = "two.sided")

	Paired t-test

data:  df10closed$bitterness_13 and df10closed$bitterness_15
t = -0.24636, df = 29, p-value = 0.8071
alternative hypothesis: true mean difference is not equal to 0
95 percent confidence interval:
 -0.7751403  0.6084736
sample estimates:
mean difference 
    -0.08333333 
t.test(df10closed$bitterness_17, df10closed$bitterness_14, 
       paired = TRUE, alternative = "greater")

	Paired t-test

data:  df10closed$bitterness_17 and df10closed$bitterness_14
t = 0.60283, df = 29, p-value = 0.2757
alternative hypothesis: true mean difference is greater than 0
95 percent confidence interval:
 -0.4122091        Inf
sample estimates:
mean difference 
      0.2266667 
t.test(df10closed$bitterness_18, df10closed$bitterness_16, 
       paired = TRUE, alternative = "greater")

	Paired t-test

data:  df10closed$bitterness_18 and df10closed$bitterness_16
t = 0.68386, df = 29, p-value = 0.2497
alternative hypothesis: true mean difference is greater than 0
95 percent confidence interval:
 -0.4206408        Inf
sample estimates:
mean difference 
      0.2833333 
```

- Ratings between the 8% skim milk and 8% water were NSD (t = 1.907, p = 0.067) 
- Ratings between the 8% skim milk and 8% water were NSD (t = -1.168, p = 0.87)
- Ratings between the 8% whole milk and 8% water were NSD (t = 0.546, p = 0.29) 

- Ratings between the 17% whole milk and 17% water were NSD (t = -0.246, p = 0.81)  
- Ratings between the 17% skim milk and 17% water were NSD (t = 0.603, p = 0.87)
- Ratings between the 17% whole milk and 17% water were NSD (t = 0.684, p = 0.29) 





<div class="figure">
<img src="01-Bitter10_files/figure-html/study1ClosedMilkRatingsViz-1.png" alt="R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose closed condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p &lt; 0.05). Bitterness intensity ratings (from 0 - 10) are represented as violin plots showing the distribution of scaling responses. Means are presented as black dots with standard error bars." width="672" />
<p class="caption">(\#fig:study1ClosedMilkRatingsViz)R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose closed condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p < 0.05). Bitterness intensity ratings (from 0 - 10) are represented as violin plots showing the distribution of scaling responses. Means are presented as black dots with standard error bars.</p>
</div>


<div class="figure">
<img src="01-Bitter10_files/figure-html/study1ClosedWaterRatingsViz-1.png" alt="R Index of paired comparison between skim milk and water at an 8% addition level and 17% addition level in a nose closed condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p &lt; 0.05). Bitterness intensity ratings (from 0 - 10) are represented as violin plots showing the distribution of scaling responses. Means are presented as black dots with standard error bars." width="672" />
<p class="caption">(\#fig:study1ClosedWaterRatingsViz)R Index of paired comparison between skim milk and water at an 8% addition level and 17% addition level in a nose closed condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p < 0.05). Bitterness intensity ratings (from 0 - 10) are represented as violin plots showing the distribution of scaling responses. Means are presented as black dots with standard error bars.</p>
</div>

## Nose Open Condition


### R Index
The R critical value for a 2-tailed test (milk comparisons) is **0.63**.  




- no discrimination seen between when 8% skim milk and 8% whole milk was added to coffee (R Index = 0.52, p > 0.05)  


- no discrimination seen between when 17% skim milk and 17% whole milk was added to coffee (R Index = 0.57, p > 0.05)  


<div class="figure">
<img src="01-Bitter10_files/figure-html/study1OpenMilkRViz-1.png" alt="R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose open condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p &lt; 0.05)." width="672" />
<p class="caption">(\#fig:study1OpenMilkRViz)R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose open condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p < 0.05).</p>
</div>

For the paired comparisons between milk and water, we hypothesized that the addition of milk would reduce the bitterness, therefore making the water sample the more bitter. The critical value for a one tailed R-index calculation is **0.61**.  





- no discrimination seen between when 8% skim milk and 8% water was added to coffee (R Index = 0.52, p > 0.05)  
- no discrimination seen between when 8% whole milk and 8% water was added to coffee (R Index = 0.596, p > 0.05)   



- no discrimination between the 17% skim milk and 17% water samples (R Index = 0.58, p > 0.05)  
- discrimination seen between the 17% whole milk and 17% water samples (R Index = 0.74, p $\le$ 0.001)  


<div class="figure">
<img src="01-Bitter10_files/figure-html/study1OpenedWaterRViz-1.png" alt="R Index of paired comparison between skim milk and water at an 8% addition level and 17% addition level in a nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p &lt; 0.05)." width="672" />
<p class="caption">(\#fig:study1OpenedWaterRViz)R Index of paired comparison between skim milk and water at an 8% addition level and 17% addition level in a nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p < 0.05).</p>
</div>

- In the nose open condition, only the 17% water sample was discriminated against the 17% whole milk sample on bitterness.

### Ratings  



Table: (\#tab:study1KableOpenRatings)Bitterness intensities, and standard error of cold brew coffee samples evaluated in nose opened condition. Each 2 rows represent the two samples presented in a paired comparison format.

|Sample        | Intensity|        se|
|:-------------|---------:|---------:|
|bitterness_13 |  4.711765| 0.3855862|
|bitterness_15 |  4.382353| 0.3764803|
|bitterness_14 |  4.758824| 0.3446334|
|bitterness_17 |  5.117647| 0.3243386|
|bitterness_16 |  4.220588| 0.3639205|
|bitterness_18 |  5.361765| 0.3609014|
|bitterness_19 |  5.079412| 0.3245394|
|bitterness_21 |  5.235294| 0.3910971|
|bitterness_20 |  5.150000| 0.3255942|
|bitterness_23 |  5.205882| 0.3650981|
|bitterness_22 |  4.994118| 0.3599104|
|bitterness_24 |  5.455882| 0.3363904|



``` r
t.test(df10opened$bitterness_19, df10opened$bitterness_21, 
       paired = TRUE, alternative = "two.sided") 

	Paired t-test

data:  df10opened$bitterness_19 and df10opened$bitterness_21
t = -0.48976, df = 33, p-value = 0.6275
alternative hypothesis: true mean difference is not equal to 0
95 percent confidence interval:
 -0.8034359  0.4916712
sample estimates:
mean difference 
     -0.1558824 
t.test(df10opened$bitterness_23, df10opened$bitterness_20, 
       paired = TRUE, alternative = "greater")

	Paired t-test

data:  df10opened$bitterness_23 and df10opened$bitterness_20
t = 0.20927, df = 33, p-value = 0.4178
alternative hypothesis: true mean difference is greater than 0
95 percent confidence interval:
 -0.3960275        Inf
sample estimates:
mean difference 
     0.05588235 
t.test(df10opened$bitterness_24, df10opened$bitterness_22, 
       paired = TRUE, alternative = "greater")

	Paired t-test

data:  df10opened$bitterness_24 and df10opened$bitterness_22
t = 1.455, df = 33, p-value = 0.07755
alternative hypothesis: true mean difference is greater than 0
95 percent confidence interval:
 -0.07531184         Inf
sample estimates:
mean difference 
      0.4617647 

t.test(df10opened$bitterness_13, df10opened$bitterness_15, 
       paired = TRUE, alternative = "two.sided")

	Paired t-test

data:  df10opened$bitterness_13 and df10opened$bitterness_15
t = 1.3597, df = 33, p-value = 0.1831
alternative hypothesis: true mean difference is not equal to 0
95 percent confidence interval:
 -0.1634718  0.8222954
sample estimates:
mean difference 
      0.3294118 
t.test(df10opened$bitterness_17, df10opened$bitterness_14, 
       paired = TRUE, alternative = "greater")

	Paired t-test

data:  df10opened$bitterness_17 and df10opened$bitterness_14
t = 1.1682, df = 33, p-value = 0.1256
alternative hypothesis: true mean difference is greater than 0
95 percent confidence interval:
 -0.1610135        Inf
sample estimates:
mean difference 
      0.3588235 
t.test(df10opened$bitterness_18, df10opened$bitterness_16, 
       paired = TRUE, alternative = "greater")

	Paired t-test

data:  df10opened$bitterness_18 and df10opened$bitterness_16
t = 3.8213, df = 33, p-value = 0.0002785
alternative hypothesis: true mean difference is greater than 0
95 percent confidence interval:
 0.6357805       Inf
sample estimates:
mean difference 
       1.141176 
  t.test(df10opened$bitterness_18, df10opened$bitterness_16, 
         paired = TRUE, alternative = "greater")$p.value <= (0.05/3)
[1] TRUE
```

- NSD between 8% skim and whole milk (t = -0.49, p = 0.63)
- NSD between 8% skim and 8% water ratings (t = -0.08, p = 0.53)  
- NSD between 8% whole milk and 8% water ratings (t = 1.46, p = 0.078)  

- NSD between 17% skim and 17% whole milk ratings (t = 1.36, p = 0.18)  
- NSD between 17% skim and 17% water ratings (t = 1.17, p = 0.13)  
- Significant reduction between 17% whole milk and 17% water ratings (t = 3.82, p = **2.8\times 10^{-4}**)  





<div class="figure">
<img src="01-Bitter10_files/figure-html/study1OpenedMilkRatingsViz-1.png" alt="R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p &lt; 0.05). Bitterness intensity ratings (from 0 - 10) are represented as violin plots showing the distribution of scaling responses. Means are presented as black dots with standard error bars." width="672" />
<p class="caption">(\#fig:study1OpenedMilkRatingsViz)R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p < 0.05). Bitterness intensity ratings (from 0 - 10) are represented as violin plots showing the distribution of scaling responses. Means are presented as black dots with standard error bars.</p>
</div>


<div class="figure">
<img src="01-Bitter10_files/figure-html/study1OpenedWaterRatingsViz-1.png" alt="R Index of paired comparison between skim milk and water at an 8% addition level and 17% addition level in a nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p &lt; 0.05). Bitterness intensity ratings (from 0 - 10) are represented as violin plots showing the distribution of scaling responses. Means are presented as black dots with standard error bars." width="672" />
<p class="caption">(\#fig:study1OpenedWaterRatingsViz)R Index of paired comparison between skim milk and water at an 8% addition level and 17% addition level in a nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p < 0.05). Bitterness intensity ratings (from 0 - 10) are represented as violin plots showing the distribution of scaling responses. Means are presented as black dots with standard error bars.</p>
</div>

## Comparison of Conditions


<div class="figure">
<img src="01-Bitter10_files/figure-html/study1MilkCombineRViz-1.png" alt="R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose closed and nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample (‘Signal’) was significant; White bars indicate the milk sample (‘Noise’) was significant (p &lt; 0.05)." width="672" />
<p class="caption">(\#fig:study1MilkCombineRViz)R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose closed and nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample (‘Signal’) was significant; White bars indicate the milk sample (‘Noise’) was significant (p < 0.05).</p>
</div>

- Figure \@ref(fig:study1MilkCombineRViz), where the 8% skim milk sample was discriminated against the 8% whole milk sample in the nose closed condition only presents an interesting piece to this puzzle.  
    + @keastModificationBitternessCaffeine2008 suggested that skim milk would reduce the bitterness of caffeine more than whole milk  
    + @bennettUsingMilkFat2012 found that whole milk reduced the bitterness of ibuprofen marginally compared to skim milk (p = 0.1), but not compared to half-and-half  


<div class="figure">
<img src="01-Bitter10_files/figure-html/study1WaterCombineRViz-1.png" alt="R Index of paired comparison between skim milk, whole milk, and water at an 8% addition level and 17% addition level in a nose closed and nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample (‘Signal’) was significant; White bars indicate the milk sample (‘Noise’) was significant (p &lt; 0.05)." width="672" />
<p class="caption">(\#fig:study1WaterCombineRViz)R Index of paired comparison between skim milk, whole milk, and water at an 8% addition level and 17% addition level in a nose closed and nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample (‘Signal’) was significant; White bars indicate the milk sample (‘Noise’) was significant (p < 0.05).</p>
</div>

- Figure \@ref(fig:study1WaterCombineRViz) continues to present interesting data in the nose closed condition when testing the 8% Addition comparisons (cf. Figure \@ref(fig:study1MilkCombineRViz))  
    + the skim milk sample was chosen as the more bitter sample compared to the same amount (8%) of water (white bar)  
    + the whole milk sample was chosen as the less bitter sample compared to water (red bar)  
- Neither of these effects are seen in the nose opened condition
    + this data does not look at the possibility of removing panelists in the nose closed condition that responded that they were not regular coffee drinkers in the demographic questions. It may be of interest to see how/if the data changes when removing them (or segmenting them).  

## Notes {-}
<input type="checkbox"> examine the participant data  
  - do panelists need to be excluded because they do not meet inclusion criteria?  
<input type="checkbox"> update Rindex figures like Chris described  
<input type="checkbox"> resolve `warnings()`?

## References {-}
