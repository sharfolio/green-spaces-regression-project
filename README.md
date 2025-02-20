# green-spaces-regression-project

# Introduction

This project explores the correlation between proximity to green spaces and the prevalence of chronic diseases across various states in the United States. The hypothesis is that closer proximity to green spaces is associated with lower rates of chronic diseases. This study utilizes data from multiple sources, including CDC, EPA, and the National Park Service, and employs regression models to analyze the impact of green spaces on public health.

# Data Sources

Chronic Diseases Dataset: CDC PLACES Local Data for Better Health (2020 & 2021), including conditions such as Teethlost, Obesity, Arthritis, Asthma, and Diabetes.

Parks Dataset: National Park Service API, containing geographical coordinates of parks and recreational areas.

Air Quality Data: EPA air quality data, focusing on Sulfur Dioxide and Carbon Monoxide levels.

State Name-Abbreviation Mapping Dataset

# Methodology

# Distance Calculation:

The nearest park to each chronic disease reporting location was identified using the "distm" function from the "geosphere" library.

The "Vincenty Ellipsoid" method was applied to compute distances.

# Remote Score Computation:

A normalized "remote score" was assigned to each location, where a score of 1 represents high remoteness and 0 indicates close proximity to parks.

# Statistical Analysis:

Linear Regression Models: To examine the relationship between remote score and chronic disease prevalence.

Bayesian Regression Models: Poisson regression was used due to count-based data, employing the "brms" function.

Air Quality Integration: Sulfur Dioxide and Carbon Monoxide data were incorporated to analyze the combined effect of pollution and green space proximity.

# Results & Discussion

# Linear Regression Findings:

An increase in remoteness correlates with a rise in chronic disease prevalence.

Chronic diseases such as Asthma and Diabetes show varying degrees of association with proximity to parks.

Model comparisons suggest a high explanatory power (Adjusted R-squared ~ 83.93%).

# Bayesian Regression Findings:

A unit increase in remoteness leads to a 21% rise in chronic disease prevalence.

Interaction terms highlight disease-specific variations in prevalence trends.

The predictive power follows: Model 3 > Model 2 > Model 1.

# Air Quality Impact:

Higher CO levels exacerbate obesity-related conditions in remote areas.

Model comparison suggests that including air quality variables improves predictive performance (Model 4a > Model 4b > Model 3).

# Conclusion

This study confirms the beneficial effects of green spaces on public health, with a notable reduction in chronic disease prevalence in areas closer to parks. However, factors such as air quality and disease-specific characteristics influence the extent of this relationship. Future research could integrate genetic predisposition and other socio-economic variables for a more comprehensive analysis.

# References

CDC PLACES Data: PLACES Local Data for Better Health

National Park Service API: NPS Developer Information

EPA Air Quality Data: Annual Summary Data

Related Research: Gianfredi et al., "Association between Urban Greenspace and Health," 2021.

# How to Use

Clone the repository.

Install required libraries: geosphere, brms, ggplot2, and standard R data manipulation packages.

Run the scripts sequentially to reproduce the analysis.

