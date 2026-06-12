# Hare_Escape
Assessing behavioral plasticity in antipredator behavior in a wild polymorphic snowshoe hare population. Using field experiments with putative predators including a hunting dog and falconry goshawks, we test effects of camouflage mismatch and predator type on hare FID, concealment, and discrete escape decisions.

## STUDY SUMMARY
This repository contains code and data for the project:

### Behavioral Plasticity in Snowshoe Hares Reflects Predator Recognition But Not Camouflage Mismatch

**Citation**: 

**Authors**: XXX

In this study, we assessed behavioral plasticity in antipredator behavior in a wild polymorphic snowshoe hare population. Using field experiments with putative predators including a hunting dog and falconry goshawks, we test effects of camouflage mismatch and predator type on hare FID, concealment, and discrete escape decisions.

### Analysis Summary

**hare_FID.Rmd**
We used linear mixed-effects models to test the effects of color morph and camouflage mismatch on hare escape behaviors. We modeled FID or concealment as a function of color morph, color contrast, and an interaction between the two. We included a square-root transformation of FID to normalize its distribution and reduce mild heteroscedasticity in the residuals. All models also included hare identity as a random effect accounting for variation between individuals.

**escape_pred.Rmd**
To test whether hares adjust escape decisions in response to predator type, we used generalized linear and linear models. These models did not include a random effect for individual. For the generalized linear model, we created a binary response variable indicating whether a hare used a subsurface refuge in either the initial or subsequent predator approach. We then modeled the probability of using subsurface refugia as a function of predator type using the glm function with a binomial error distribution and a logit link. From this model, we estimated pairs of odds and their 95% confidence intervals. Finally, we fit linear models to test the effect of predator type on hare FID.


## ACCESS INFORMATION
1. MIT License
2. Recommended citation for this data/code archive
xxx

## DATA & CODE FILE OVERVIEW
This data repository consist of 2 data files, 2 code scripts, 1 license, and this README document, with the following data and code filenames and variables

Data files and variables
    1. OR_FIDs.csv 
    2. escape.csv
    
### Variables

***hare_FID variables***
**Eartag**: Eartag number idenfitying individual hare

**Concealment**: Estimated percent of the hare’s body obscured by vegetation at a 2 m radius from all sides in four categories (1:0-25%, 2: 25-50%, 3: 50-75%, and 4: 75-100%)

**conc**: Concealment converted to numeric values (median value of each of the 4 categories)

**WCC**: Hare winter coat color

**P_White**: Hare percent coat whiteness, visually estimated at time of approach

**snow_1m**: Percent snow cover within 1m radius of hare at initial resting spot

**snow_10m**: Percent snow cover within 10m radius of hare at initial resting spot

**FID_m**: Hare flight initiation distance (FID) recorded as the distance in meters between hare and observer at the moment the hare moved from its resting spot

**rep**: Repetitions, or ordered number of approaches on the individual hare throughout the duration of the study

**m_contrast**: Hare color contrast (mismatch) at 1m, or the difference between hare percent white and percent snow cover within a 1m radius 

**tenm_contrast**: Hare color contrast (mismatch) at 10m, or the difference between hare percent white and percent snow cover within a 10m radius

**mm1m**: Absolute value of hare color contrast (mismatch) at 1m, or the difference between hare percent white and percent snow cover within a 1m radius

**mm10m**: Absolute value of hare color contrast (mismatch) at 10m, or the difference between hare percent white and percent snow cover within a 10m radius


**escape variables**
**Threat**: Predator type (Avian, Canine, or Human)

**Hare.ET**: Eartag number identifying individual hare

**rep**: Repetitions, or ordered number of approaches on the individual hare throughout the duration of the study

**choice1**: Discrete escape decision (F = Flight, V = Vegetation Refuge, X = Subsurface Refuge) on initial approach by predator

**choice2**: Discrete escape decision (F = Flight, V = Vegetation Refuge, X = Subsurface Refuge) on subsequent approach by predator

**hole**: Binary (Y or N) variable representing subsurface refuge use (**choice1** or **choice2** = X) on either initial or subsequent approach

**conc**: Estimated percent of the hare’s body obscured by vegetation at a 1 m radius from all sides at initial resting spot

**conc2**: Estimated percent of the hare’s body obscured by vegetation at a 1 m radius from all sides at subsequent resting spot (after initial predator chase)

**FID**:  Hare flight initiation distance (FID) recorded as the distance in meters between hare and predator at the moment the hare moved from its initial resting spot

**FID2**:  Hare flight initiation distance (FID) recorded as the distance in meters between hare and predator at the moment the hare moved from its subsequent resting spot (after initial predator chase)



## Code scripts and workflow

 1. hare_FID.Rmd
    
    Data formatting and analysis using linear mixed effects models to assess snowshoe hare behavioral       plasticity to camouflage mismatch

 2. escape_pred.Rmd
    
    Data formatting and analysis using linear mixed effects models to assess snowshoe hare behavioral       plasticity to predator type
    

**SOFTWARE VERSIONS**

R version 4.5.2 (2025-10-31) -- "[Not] Part in a Rumble" 
Packages:  
 lme4           1.1-38 
 lmerTest       3.2-0
 MASS           7.3-65 
 Matrix         1.7-4 
 nlme           3.1-168
 minqa          1.2.8 
 nloptr         2.2.1
 boot           1.3-32
 cli            3.6.5   
 digest         0.6.37  
 dplyr          1.1.4   
 evaluate       1.0.5   
 farver         2.1.2   
 fastmap        1.2.0   
 generics       0.1.4   
 ggplot2        4.0.0   
 glue           1.8.0   
 gtable         0.3.6   
 htmltools      0.5.8.1 
 knitr          1.50    
 lifecycle      1.0.4   
 magrittr       2.0.3   
 patchwork      1.3.2   
 pillar         1.11.0  
 pkgconfig      2.0.3   
 R6             2.6.1   
 rbibutils      2.3 
 RColorBrewer   1.1-3   
 Rcpp           1.1.0  
 Rdpack         2.6.4   
 reformulas     0.4.1 
 rlang          1.1.6   
 rmarkdown      2.29    
 rstudioapi     0.17.1  
 S7             0.2.0   
 scales         1.4.0   
 sessioninfo    1.2.4  
 tibble         3.3.0   
 tidyselect     1.2.1   
 vctrs          0.6.5   
 xfun           0.53   
 yaml           2.3.10 
 numDeriv       2016.8-1.1 

**PERMITTING**

All experimental protocols were approved through the XXX Institutional Care and Use Committee (Protocols No. 041-19SMRCS-071819, 028-21SMRCS-051121). Hare trapping was conducted under permission of Oregon Department of Fish and Wildlife (Permits 060-20, 060-21, 060-22, 060-23). Participating dog and falconry goshawks were privately owned and cared for.

**FUNDING**

Funding for this work provided by National Science Foundation Division of Environmental Biology Grant 1907022 to XXX
