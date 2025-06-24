# Analysis-of-Away-Goals-Average-in-the-Serie-A-Championship

This project was developed as the final assignment for the **STATISTICAL METHODS IN DATA SCIENCE AND LABORATORY** course, part of the **Data Science** degree program at **La Sapienza, University of Rome**, during the **2024/2025** academic year.

Football analytics has transformed how we understand team performance, with away goals representing one of the most strategically significant metrics in modern football.
This project presents a comprehensive Bayesian analysis of away goals performance in Italy's Serie A championship, leveraging 17 seasons of match data (1993/1994 to 2015/2016) to uncover fundamental patterns in offensive performance during away matches.

## Context and Motivation

The ability to score away from home is a critical determinant of success in elite football competitions.
Serie A's reputation for tactical complexity and defensive solidity makes it an ideal laboratory for studying away performance dynamics.
By focusing specifically on away goals - a metric that eliminates home advantage effects - we gain clearer insights into teams' inherent offensive capabilities under challenging conditions.

## Analytical Approach

Our investigation employs a rigorous Bayesian framework to model the average away goals per match:\
- **Statistical Foundation**: We establish the Gamma distribution as the optimal parametric model for this positive, right-skewed variable through extensive exploratory analysis and goodness-of-fit testing\
- **Bayesian Inference**: Using JAGS for MCMC sampling, we implement a mean-precision parametrized Gamma model with weakly informative priors derived from maximum likelihood estimates\
- **Robust Validation**: Convergence diagnostics (Gelman-Rubin, trace plots, ESS), parameter recovery simulations, and frequentist comparisons ensure methodological rigor\
- **Model Comparison**: We formally contrast Gamma and Log-Normal alternatives using DIC and Bayes factors to justify distributional choice

## Key Objectives

1.  Quantify the fundamental characteristics of away scoring in Serie A through posterior distributions of mean, variance, and precision parameters\
2.  Assess temporal stability of away performance across seasons\
3.  Establish a statistically robust framework for team performance evaluation\
4.  Compare Bayesian and frequentist inferences for sports analytics applications

## Report Structure

1.  **Dataset Illustration**: Construction of the key metric, exploratory analysis, and distributional assessment\
2.  **Statistical Modeling**: Bayesian specification, prior selection, and inferential goals\
3.  **Main Findings**: Posterior estimates, hypothesis testing, and prior-posterior comparison\
4.  **Model Comparison**: Formal comparison of Gamma and Log-Normal alternatives\
5.  **Validation**: MCMC diagnostics, parameter recovery, and frequentist benchmarking

 ## Repository Contents

- `Sorrentini_2023085.Rmd` – Scripts for the analysis.
- `SerieA.RData` – Original file used.
- `progetto.pdf` – Final report including description, analysis.
- `README.md` – This file.


## Conclusion

This comprehensive analysis of away goals performance in Serie A has yielded robust insights through a Bayesian statistical framework.
The Gamma distribution emerged as the optimal model for characterizing away goals per match, outperforming the Log-Normal alternative based on both DIC (ΔDIC = 13.58) and Bayes Factor (BF = 698.53) metrics.
Our findings establish that the expected number of away goals per match is 1.08 (95% CI: 1.05-1.12), with a precision parameter of 9.76 (95% CI: 8.52-11.09) indicating moderate consistency in team performances away from home.

The convergence diagnostics and parameter recovery studies confirmed the reliability of our inferences, with all R hat statistics ≤ 1.0015 and Monte Carlo errors \< 0.06%.
Notably, the comparison with frequentist methods revealed remarkable consistency in point estimates while highlighting Bayesian advantages in uncertainty quantification.
The stability of away goals performance across seasons suggests fundamental characteristics of Serie A's competitive structure, though the exclusion of the anomalous 2016/2017 season was justified by our sensitivity analysis.

## Contact

**Author**: [Matteo Sorrentini]  
📧 [sorrentini.2023085@studenti.uniroma1.it](mailto:sorrentini.2023085@studenti.uniroma1.it)

##  License

This project is released under the **MIT License**.  
See the `LICENSE` file for more details.

This study demonstrates the value of Bayesian approaches for sports analytics, providing not only point estimates but complete posterior distributions that properly quantify uncertainty.
Future research could extend this framework to model home advantage dynamics, investigate temporal trends more granularly, or incorporate team-level hierarchical effects.
The methodological rigor established here serves as a foundation for more sophisticated models of football performance that account for tactical evolution and competitive balance in one of Europe's most strategically complex leagues.
