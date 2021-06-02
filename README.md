## Requirements

- To compile all the codes, R 4.0 or later is recommended.
- To get the latest R update:
  1. Install and load from R Gui: `install.packages("installr")` and `library(installr)`.
  2. Call `update(R)`.
  3. From within RStudio, run `R.version.string` to get detailed information about the version of R running.
- To easily run all the R scripts, use `PenalizedJQM.Rproj` in the main directory.
- Go to `"./codes/install.package.R"` and run the codes for installing all necessary packages.


## Simulation study

- To run the LQMM simulation, `LQMM_Function.R` and `LQMM_Sims.R` must be in a same local directory.
- The input files can be found in `"./data"` directory.
- Run `LQMM_Sims.R` for the LQMM simulation, the output of the results will be stored in `"./output/LQMM"` directory.
- To run the Penalized JQM simulation, `JQM_Function.R` and `JQM_Sims.R` must be in a same local directory.
- Run `JQM_Sims.R` by changing the seed, sample size *N* and *n*, and parameter scenarios *beta, a, b, psiu2* and *alpha*. The list of sample size and parameter scenarios with their corresponding seeds can be found in `"./data/PJQM_scenarios.csv"`. The number of simulation runs is indicated by variable *NSim*.
- The output of the results will be stored in `"./output/PJQM"` directory.

## Read simulation results

- To read the simulation results and produce the simulation figures and tables, run `read.sims.result.R` and `sim.plots.R`.

## Case Study: IAM Frontier Data

- To produce the real data results and figures, VITO IAM Frontier data is needed. The data is not provided in this repository because of confidentiality reason, please contact the authors for further information.
- Run `IAM.allpar.LQMM.R` and `IAM.allpar.JQM.R` to generate the results in Table 2.
- Run `IAM.IRI.plot.R` to produce the IRI plots in Figure 2, 3, 4, and 5 and also Figure S3 in the Supplementary Document. 
- Run `IAM.circos.plot.R` to produce the circos plot in Figure S1 and `IAM.cosine.similarity` to produce the cosine similarity matrix and Figure S2 in the Supplementary Document.
