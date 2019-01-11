# Minimum Standards for Adaptive Trials

Just a summary from a paper of the same name.

+ pre-specify planned adaptions and primary analysis
+ evaluate statistical properties
+ standards for using bayesian methods in adaptive randomised trials
+ communication/vetting trial design with stakeholders
+ adequate infrastructure
+ consider operational bias
+ oversight
+ reporting following CONSORT

## Prespecification and primary analysis

Simple trials are those that can be computed analytically. Everything else is complex (RAR, arm dropping, enrichment) and needs simulations. Complexity can arise from a combination of simple adaptations (obviously).

When can the adaptions occur? At interims? If so, when do these occur? 

+ num enrolled
+ num evaluated
+ num of events
+ calendar time 
+ composite of the above?

Specify the adaptive criteria.

+ "accrual terminated early if predictive probability of success is greater than 0.95"
+ define the population whose results trigger the adaptation, e.g. all randomised

Specify how the primary analysis proceeds including the statistical model to be used.

E.g. If a trial stops early, how do you treat those enrolled but lacking primary outcome in final analysis?

### Example trials with prespecification/primary analysis

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3195898/
https://www.nejm.org/doi/full/10.1056/NEJMoa0810266
https://www.ncbi.nlm.nih.gov/pubmed/22172433
https://www.ncbi.nlm.nih.gov/pubmed/15863204


## Evaluate statistical properties

Goldilocks approach to sample size selection explains some concepts:
https://www.ncbi.nlm.nih.gov/pubmed/24697532

Evaluate:

+ type I error 
+ power
+ sample size

Null hypothesis is normally multidimensional, e.g. there are many ways for two treatments to be equally effective. Type I error varies over the null hyp parameter space.

For sample size compute median, mean, probability that reaches predetermined maximum, variance etc.

Compute precision and bias in estimation of treatment effect.

Look at accrual rate, dropout, missing data, delays in data updates, subgroup treatment interactions, violations of distributional assumptions. Possibly consider the effects of drift in participant characteristics over time.

Consider a range of baseline and treatment effects.

Other metrics may include frequency with which specific adaptations occur, probability of covariate imbalance, adequacy for subgroup and safety analyses.

Simulation methods should be described in sap and results summarised in sap appendix. Include the following sections:

1. description of the adpative structure
2. all adaptations and populations they are based on
3. statistical models - include software used
4. statistical models and thresholds for primary 
5. operating characteristics of design
6. example of simulated trial(s)
7. method of calculating operating characteristics:
	+ if simulations - assumptions used
	+ creation of virtual participants
	+ assumptions on accrual, dropout, missing, time to info

Retain programs under version control.

### Example trials with evaluated statistical properties

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3195898/
https://www.ncbi.nlm.nih.gov/pubmed/22172433
https://www.ncbi.nlm.nih.gov/pubmed/15911469

CRAN Lib: 
https://www.ncbi.nlm.nih.gov/pubmed/20798135
https://cran.r-project.org/web/packages/asd/index.html

Book: https://www.springer.com/gp/book/9780387951690

Bayesian example: 
https://www.nejm.org/doi/full/10.1056/NEJMoa1105243

Bayesian example:
https://www.ncbi.nlm.nih.gov/pubmed/14563972
https://www.ncbi.nlm.nih.gov/pubmed/16281432

## Standards for using bayesian methods in adaptive randomised trials

Need to specify statistical models used for trial including prior elicitation and assumptions regarding exchangeability. Rationale for priors required. Using different (e.g. informative) priors in the design phase but not in the final analysis should be made clear. Utility functions need to be made clear when applicable.

### Example bayesian trials

https://www.ncbi.nlm.nih.gov/pubmed/14563972
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3195898/

Hierarchical:
https://www.ncbi.nlm.nih.gov/pubmed/12587104

Don Berry:
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2913209/

https://www.ncbi.nlm.nih.gov/pubmed/17602081

