# 1:5 Bitterness {#Bitter5}

This will be the data analysis and results of the 1:5 nose closed study run in March 2023 and the 1:5 nose open study run in September 2023.  

See the 1:10 brew strength bitter analysis [here](#Bitter10). 

A 1:5 brew strength (coffee:water, w/w) is representative of a cold brew concentrate. Our ~~**hypotheses**~~ (note 12-24-24: the following were not hypotheses, they are *interpretations*) were as follows:  

- In the nose closed condition a reduction in bitterness from the milky coffee would suggest a physicochemical interaction between the milk and coffee  
- Milk, being 86% water [@walstraDairyTechnologyPrinciples1999] could have a similar effect as water would when added to coffee   
- In the nose opened condition, a reduction in bitterness from the milky coffee could suggest a cross-modal interaction (particularly if no effect is seen in the nose closed condition) 

> Note 12-24-24: We had initially hypothesized that there would be a physicochemical interaction (such as protein-polyphenol interaction)  

Note 01-06-25: I think the hypothesis was that the addition of milk would reduce the bitterness of cold brew coffee.  

## Nose Closed Condition






### R Index  
In the paired comparisons between when skim milk or whole milk was added to the coffee, there is not enough evidence to suggest one will reduce the bitterness more than the other [cf. @keastModificationBitternessCaffeine2008].  
The critical value for a 2-tailed test is 0.62.  



- no discrimination seen between when 8% skim milk and 8% whole milk was added to coffee (R Index = 0.55, p > 0.05)  



- no discrimination between 17% skim milk or 17% whole milk added to coffee, (R Index = 0.56, p > 0.05)  


<div class="figure">
<img src="03-Bitter05_files/figure-html/study3ClosedMilkRViz-1.png" alt="R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose closed condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p &lt; 0.05)." width="672" />
<p class="caption">(\#fig:study3ClosedMilkRViz)R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose closed condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p < 0.05).</p>
</div>

For the paired comparisons between milk and water, we hypothesized that the addition of milk would reduce the bitterness, therefore making the water sample the more bitter. The critical value for a one tailed R-index calculation is 0.62.  




- no discrimination seen between when 8% skim milk and 8% water was added to coffee (R Index = 0.58, p > 0.05)  

- no discrimination seen between when 8% whole milk and 8% water was added to coffee (R Index = 0.53, p > 0.05)   



- no discrimination between the 17% skim milk and 17% water samples (R Index = 0.54, p > 0.05)  
- no discrimination between the 17% whole milk and 17% water samples (R Index = 0.54, p > 0.05)  


<div class="figure">
<img src="03-Bitter05_files/figure-html/study3ClosedWaterRViz-1.png" alt="R Index of paired comparison between skim milk and water at an 8% addition level and 17% addition level in a nose closed condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p &lt; 0.05)." width="672" />
<p class="caption">(\#fig:study3ClosedWaterRViz)R Index of paired comparison between skim milk and water at an 8% addition level and 17% addition level in a nose closed condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p < 0.05).</p>
</div>

- No discrimination was seen at either the 8% or 17% addition levels  
  + To me, this calls into question Figure (see \@ref(fig:study1ClosedWaterRViz))   

### Ratings  
The paired comparison will only show which sample is more bitter (or discriminated against), without showing a magnitude of the difference. Thus, bitterness intensity ratings were recorded as well. They will be analyzed by paired t-test with a Bonferroni correction against multiple comparisons.  




Table: (\#tab:study3KableClosedRatings)Bitterness intensities, standard deviation, and standard error of cold brew coffee samples. Each 2 rows represent the two samples presented in a paired comparison format.

|Sample        | Intensity|       sd|        se|
|:-------------|---------:|--------:|---------:|
|bitterness_1  |  5.625000| 1.995964| 0.3528399|
|bitterness_3  |  5.812500| 1.886924| 0.3335643|
|bitterness_2  |  5.929688| 2.133861| 0.3772170|
|bitterness_5  |  5.875000| 2.117515| 0.3743274|
|bitterness_4  |  5.612500| 2.389189| 0.4223530|
|bitterness_6  |  6.031250| 2.082715| 0.3681755|
|bitterness_7  |  6.562500| 2.143068| 0.3788445|
|bitterness_9  |  5.968750| 1.963118| 0.3470334|
|bitterness_8  |  6.312500| 1.929190| 0.3410358|
|bitterness_11 |  5.890625| 2.058556| 0.3639047|
|bitterness_10 |  5.945312| 2.111541| 0.3732713|
|bitterness_12 |  6.125000| 2.355501| 0.4163978|



The Bonferroni corrected $\alpha$ would be 0.0083.


``` r
t.test(df5closed$bitterness_7, df5closed$bitterness_9, 
       paired = TRUE, alternative = "two.sided") 

	Paired t-test

data:  df5closed$bitterness_7 and df5closed$bitterness_9
t = 1.7347, df = 31, p-value = 0.09273
alternative hypothesis: true mean difference is not equal to 0
95 percent confidence interval:
 -0.1043359  1.2918359
sample estimates:
mean difference 
        0.59375 
t.test(df5closed$bitterness_11, df5closed$bitterness_8, 
       paired = TRUE, alternative = "greater")

	Paired t-test

data:  df5closed$bitterness_11 and df5closed$bitterness_8
t = -1.2552, df = 31, p-value = 0.8906
alternative hypothesis: true mean difference is greater than 0
95 percent confidence interval:
 -0.9917266        Inf
sample estimates:
mean difference 
      -0.421875 
t.test(df5closed$bitterness_12, df5closed$bitterness_10, 
       paired = TRUE, alternative = "greater")

	Paired t-test

data:  df5closed$bitterness_12 and df5closed$bitterness_10
t = 0.49488, df = 31, p-value = 0.3121
alternative hypothesis: true mean difference is greater than 0
95 percent confidence interval:
 -0.4359375        Inf
sample estimates:
mean difference 
      0.1796875 

t.test(df5closed$bitterness_1, df5closed$bitterness_3, 
       paired = TRUE, alternative = "two.sided")

	Paired t-test

data:  df5closed$bitterness_1 and df5closed$bitterness_3
t = -0.5172, df = 31, p-value = 0.6087
alternative hypothesis: true mean difference is not equal to 0
95 percent confidence interval:
 -0.9268803  0.5518803
sample estimates:
mean difference 
        -0.1875 
t.test(df5closed$bitterness_5, df5closed$bitterness_2, 
       paired = TRUE, alternative = "greater")

	Paired t-test

data:  df5closed$bitterness_5 and df5closed$bitterness_2
t = -0.18853, df = 31, p-value = 0.5742
alternative hypothesis: true mean difference is greater than 0
95 percent confidence interval:
 -0.5465046        Inf
sample estimates:
mean difference 
     -0.0546875 
t.test(df5closed$bitterness_6, df5closed$bitterness_4, 
       paired = TRUE, alternative = "greater")

	Paired t-test

data:  df5closed$bitterness_6 and df5closed$bitterness_4
t = 1.0465, df = 31, p-value = 0.1517
alternative hypothesis: true mean difference is greater than 0
95 percent confidence interval:
 -0.2597325        Inf
sample estimates:
mean difference 
        0.41875 
```


- Marginal reduction in ratings between the 8% skim milk and 8% whole milk (t = 1.735, p = 0.09) 
- Ratings between the 8% skim milk and 8% water were NSD (t = -1.255, p = 0.89) 
- Ratings between the 8% whole milk and 8% water were NSD (t = 0.495, p = 0.31) 

- 17% milk comparisons were not significantly different in ratings (t = -0.517, p = 0.61)
- Ratings between the 17% skim milk and 17% water were NSD (t = -0.189, p = 0.57)  
- Ratings between the 17% whole milk and 17% water were NSD (t = 1.046, p = 0.15) 





<div class="figure">
<img src="03-Bitter05_files/figure-html/study3ClosedMilkRatingsViz-1.png" alt="R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose closed condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p &lt; 0.05). Bitterness intensity ratings (from 0 - 10) are represented as violin plots showing the distribution of scaling responses. Means are presented as black dots with standard error bars." width="672" />
<p class="caption">(\#fig:study3ClosedMilkRatingsViz)R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose closed condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p < 0.05). Bitterness intensity ratings (from 0 - 10) are represented as violin plots showing the distribution of scaling responses. Means are presented as black dots with standard error bars.</p>
</div>


<div class="figure">
<img src="03-Bitter05_files/figure-html/study3ClosedWaterRatingsViz-1.png" alt="R Index of paired comparison between skim milk and water at an 8% addition level and 17% addition level in a nose closed condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p &lt; 0.05). Bitterness intensity ratings (from 0 - 10) are represented as violin plots showing the distribution of scaling responses. Means are presented as black dots with standard error bars." width="672" />
<p class="caption">(\#fig:study3ClosedWaterRatingsViz)R Index of paired comparison between skim milk and water at an 8% addition level and 17% addition level in a nose closed condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p < 0.05). Bitterness intensity ratings (from 0 - 10) are represented as violin plots showing the distribution of scaling responses. Means are presented as black dots with standard error bars.</p>
</div>

## Nose Open Condition


### R Index
The R critical value for a 2-tailed test (milk comparisons) is: 0.63.  




- no discrimination seen between when 8% skim milk and 8% whole milk was added to coffee (R Index = 0.52, p > 0.05)  


- no discrimination seen between when 17% skim milk and 17% whole milk was added to coffee (R Index = 0.57, p > 0.05)  


<div class="figure">
<img src="03-Bitter05_files/figure-html/study3OpenMilkRViz-1.png" alt="R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose open condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p &lt; 0.05)." width="672" />
<p class="caption">(\#fig:study3OpenMilkRViz)R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose open condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p < 0.05).</p>
</div>

For the paired comparisons between milk and water, we hypothesized that the addition of milk would reduce the bitterness, therefore making the water sample the more bitter. The critical value for a one tailed R-index calculation is 0.61.  





- no discrimination seen between when 8% skim milk and 8% water was added to coffee (R Index = 0.51, p > 0.05)  
- no discrimination seen between when 8% whole milk and 8% water was added to coffee (R Index = 0.573, p > 0.1)   



- no discrimination between the 17% skim milk and 17% water samples (R Index = 0.51, p > 0.05)  
- discrimination seen between the 17% whole milk and 17% water samples (R Index = 0.74, p $\le$ 0.001)  


<div class="figure">
<img src="03-Bitter05_files/figure-html/study3OpenedWaterRViz-1.png" alt="R Index of paired comparison between skim milk and water at an 8% addition level and 17% addition level in a nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p &lt; 0.05)." width="672" />
<p class="caption">(\#fig:study3OpenedWaterRViz)R Index of paired comparison between skim milk and water at an 8% addition level and 17% addition level in a nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p < 0.05).</p>
</div>

- In the nose open condition, only the 17% water sample was discriminated against the 17% whole milk sample on bitterness.  
  + These two samples were not discriminated in the nose closed condition (see \@ref(fig:study3ClosedWaterRViz))  

### Ratings  



Table: (\#tab:study3KableOpenRatings)Bitterness intensities, standard deviation, and standard error of cold brew coffee samples evaluated in nose opened condition. Each 2 rows represent the two samples presented in a paired comparison format.

|Sample        | Intensity|       sd|        se|
|:-------------|---------:|--------:|---------:|
|bitterness_1  |  6.088235| 1.653603| 0.2835906|
|bitterness_3  |  5.808823| 1.992466| 0.3417051|
|bitterness_2  |  5.967647| 1.929629| 0.3309286|
|bitterness_5  |  6.088235| 1.908794| 0.3273554|
|bitterness_4  |  5.520588| 1.983077| 0.3400949|
|bitterness_6  |  6.426471| 1.950650| 0.3345337|
|bitterness_7  |  6.205882| 1.813742| 0.3110542|
|bitterness_9  |  6.220588| 1.771796| 0.3038605|
|bitterness_8  |  5.994118| 1.672766| 0.2868770|
|bitterness_11 |  5.911765| 1.802652| 0.3091523|
|bitterness_10 |  5.929412| 2.340620| 0.4014130|
|bitterness_12 |  6.352941| 1.920896| 0.3294309|



``` r
t.test(df5opened$bitterness_7, df5opened$bitterness_9, 
       paired = TRUE, alternative = "two.sided") 

	Paired t-test

data:  df5opened$bitterness_7 and df5opened$bitterness_9
t = -0.041302, df = 33, p-value = 0.9673
alternative hypothesis: true mean difference is not equal to 0
95 percent confidence interval:
 -0.7391076  0.7096958
sample estimates:
mean difference 
    -0.01470588 
t.test(df5opened$bitterness_11, df5opened$bitterness_8, 
       paired = TRUE, alternative = "greater")

	Paired t-test

data:  df5opened$bitterness_11 and df5opened$bitterness_8
t = -0.28868, df = 33, p-value = 0.6127
alternative hypothesis: true mean difference is greater than 0
95 percent confidence interval:
 -0.5651384        Inf
sample estimates:
mean difference 
    -0.08235294 
t.test(df5opened$bitterness_12, df5opened$bitterness_10, 
       paired = TRUE, alternative = "greater")

	Paired t-test

data:  df5opened$bitterness_12 and df5opened$bitterness_10
t = 1.3283, df = 33, p-value = 0.09659
alternative hypothesis: true mean difference is greater than 0
95 percent confidence interval:
 -0.1160624        Inf
sample estimates:
mean difference 
      0.4235294 

t.test(df5opened$bitterness_1, df5opened$bitterness_3, 
       paired = TRUE, alternative = "two.sided")

	Paired t-test

data:  df5opened$bitterness_1 and df5opened$bitterness_3
t = 0.84529, df = 33, p-value = 0.404
alternative hypothesis: true mean difference is not equal to 0
95 percent confidence interval:
 -0.3931032  0.9519267
sample estimates:
mean difference 
      0.2794118 
t.test(df5opened$bitterness_5, df5opened$bitterness_2, 
       paired = TRUE, alternative = "greater")

	Paired t-test

data:  df5opened$bitterness_5 and df5opened$bitterness_2
t = 0.31972, df = 33, p-value = 0.3756
alternative hypothesis: true mean difference is greater than 0
95 percent confidence interval:
 -0.5177253        Inf
sample estimates:
mean difference 
      0.1205882 
t.test(df5opened$bitterness_6, df5opened$bitterness_4, 
       paired = TRUE, alternative = "greater")

	Paired t-test

data:  df5opened$bitterness_6 and df5opened$bitterness_4
t = 2.3236, df = 33, p-value = 0.01323
alternative hypothesis: true mean difference is greater than 0
95 percent confidence interval:
 0.2460889       Inf
sample estimates:
mean difference 
      0.9058824 
```

- NSD between 8% skim and whole milk (t = -0.04, p = 0.967)
- NSD between 8% skim and 8% water ratings (t = -0.29, p = 0.61)  
- marginal reduction between 8% whole milk and 8% water ratings (t = -1.33, p = 0.097)  

- NSD between 17% skim and 17% whole milk ratings (t = 0.85, p = 0.4)  
- NSD between 17% skim and 17% water ratings (t = 0.32, p = 0.38)  
- significant reduction between 17% whole milk and 17% water ratings (t = 2.32, p = 0.013)  






<div class="figure">
<img src="03-Bitter05_files/figure-html/study3OpenedMilkRatingsViz-1.png" alt="R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p &lt; 0.05). Bitterness intensity ratings (from 0 - 10) are represented as violin plots showing the distribution of scaling responses. Means are presented as black dots with standard error bars." width="672" />
<p class="caption">(\#fig:study3OpenedMilkRatingsViz)R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p < 0.05). Bitterness intensity ratings (from 0 - 10) are represented as violin plots showing the distribution of scaling responses. Means are presented as black dots with standard error bars.</p>
</div>


<div class="figure">
<img src="03-Bitter05_files/figure-html/study3OpenedWaterRatingsViz-1.png" alt="R Index of paired comparison between skim milk and water at an 8% addition level and 17% addition level in a nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p &lt; 0.05). Bitterness intensity ratings (from 0 - 10) are represented as violin plots showing the distribution of scaling responses. Means are presented as black dots with standard error bars." width="672" />
<p class="caption">(\#fig:study3OpenedWaterRatingsViz)R Index of paired comparison between skim milk and water at an 8% addition level and 17% addition level in a nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample ('Signal') was significant; White bars indicate the milk sample ('Noise') was significant (p < 0.05). Bitterness intensity ratings (from 0 - 10) are represented as violin plots showing the distribution of scaling responses. Means are presented as black dots with standard error bars.</p>
</div>

### Comparison of Conditions (R-index) 


<div class="figure">
<img src="03-Bitter05_files/figure-html/study3MilkCombineRViz-1.png" alt="R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose closed and nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample (‘Signal’) was significant; White bars indicate the milk sample (‘Noise’) was significant (p &lt; 0.05)." width="672" />
<p class="caption">(\#fig:study3MilkCombineRViz)R Index of paired comparison between skim milk and whole milk at an 8% addition level and 17% addition level in a nose closed and nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample (‘Signal’) was significant; White bars indicate the milk sample (‘Noise’) was significant (p < 0.05).</p>
</div>

- Figure \@ref(fig:study3MilkCombineRViz) shows no discrimination in bitterness between when skim milk or whole milk was added to cold brew coffee concentrate  


<div class="figure">
<img src="03-Bitter05_files/figure-html/study3WaterCombineRViz-1.png" alt="R Index of paired comparison between skim milk, whole milk, and water at an 8% addition level and 17% addition level in a nose closed and nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p &gt; 0.05). Red bars indicate the water sample (‘Signal’) was significant; White bars indicate the milk sample (‘Noise’) was significant (p &lt; 0.05)." width="672" />
<p class="caption">(\#fig:study3WaterCombineRViz)R Index of paired comparison between skim milk, whole milk, and water at an 8% addition level and 17% addition level in a nose closed and nose opened condition. Dashed horizontal line represents the critical value, which denotes statistical significance, or discrimination between the samples on bitterness. Grey bars are not significant (p > 0.05). Red bars indicate the water sample (‘Signal’) was significant; White bars indicate the milk sample (‘Noise’) was significant (p < 0.05).</p>
</div>

- Figure \@ref(fig:study3WaterCombineRViz) shows that only the 17% whole milk was able to be discriminated from the 17% water addition.
  + how does this compare to Figure \@ref(fig:study1WaterCombineRViz)?

