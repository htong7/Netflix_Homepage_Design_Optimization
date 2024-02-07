# Netflix Homepage Browsing Time Optimization

## Table of Contents
1. Executive Summary
2. Introduction
3. Experiments
4. Conclusion

## Executive Summary
This project aims to optimize the Netflix homepage browsing experience by minimizing the time users spend browsing. The optimal browsing time was found to be a match score of 75, a preview length of 75 seconds, and a preview type of Teaser Trailer (‘TT’). This results in a predicted average browsing time of 9.96 minutes, with a 95% confidence interval of 7.86 to 12.06 minutes. Interestingly, tile size does not significantly influence average browsing time.

## Introduction
The risk of losing user interest due to excessive viewing options is reduced by minimizing browsing time. Four factors that may influence time spent browsing the homepage are tile size, match score, preview length, and preview type for offerings in the “Top Pick For...” row of the homepage. Through multivariate experiments, an optimal combination of these factors can be found that minimizes average browsing time and elevates user experience.

## Experiments
### 2k + Center Point factorial design
The objective of this first experiment was to screen for significant factors and verify if the levels used for screening were in an area of curvature. Screening tests often do not occur over a design space that contains an optimum but in order to confidently rule out the screening levels, a 2k + center point design was implemented. Including a center point condition in the 2k factorial design allowed for a test of curvature around the screening values. The screening values can be found in their natural and coded units in Table 1. Eighteen total conditions were tested in this first experiment with 100 users randomly assigned to each condition.

Tile size and preview length were screened at their minimum and maximum values within their regions of operability, which maximized the chance of finding significant effects if they existed. Instead of using the minimum value of 0% for match score, we decided to use a 50% score based on the assumption that scores between 0% and 49% would likely not be put into practice. Testing with these values could also potentially negatively impact users’ attitudes toward recommendations, and therefore Netflix products.

After fitting a full Ordinary Least Squares (OLS) model and applying a 5% significance threshold, we found that tile size and its interactions did not have a statistically significant impact. Match score, preview type, and preview length were significant (p-value 0). The interaction between match score and preview length was also significant (p-value 0). The results of fitting a second order model with these significant effects plus the one significant interaction showed significant coefficients for the quadratic terms (both p-values 0), indicating curvature in the surface and that a possible optimum is nearby.

Based on these findings, subsequent experiments excluded tile size and all interaction terms except for the one between match score and preview length. Screening levels were also subsequently used to explore optimal factor levels of match score and preview length.

## Conclusion
Through a sequential set of experiments and analysis, our study examined four factors of the “Top Picks For...” row of the Netflix homepage in order to minimize average browsing time. Our results suggest that this row of the homepage should employ a match score of 75%, preview length of 75 seconds, and teaser/trailer content in order to keep average browsing time at 9.96 minutes with a 95% confidence interval of 7.86 minutes to 12.06 minutes. Tile size was shown to not significantly affect browse time, so can be selected to aesthetically complement the homepage within the range of a 0.1 to 0.5 ratio of tile height to screen height.

Despite our comprehensive approach, we acknowledge that limitations might affect our findings. One such limitation is that there are likely uncontrolled sources of variation in our designs that affect average browsing time.
