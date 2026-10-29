# pMC-SIMEX

This repository contains code to implement the pMC-SIMEX methodology developed in the manuscript entitled "Adapting misclassification simulation-extrapolation to correct for errors in binary time-varying exposures in prescription-based pharmacoepidemiologic studies".

This code takes as input a dataset containing longitudinal daily drug exposure indicators based on prescription fillings (in long format), as typical of pharmacoepidemiologic studies using prescriptions claims databased to infer observed drug usage. In addition, the dataset must contain prescription information (filling date and duration) to be able to compute the Medication Possession Ratio for each prescription. An example of such a dataset can be found here: https://github.com/steveferreiraguerra/Rcode-ME-in-TV-precription-based-exposures.

The code separates the simulation and extrapolation steps of the proposed pMC-SIMEX. 
In the simulation step, two alternatives to generate missclassified X** data are proposed: one according to the algorithm of section 2.2.2 and one according to Appendix B. Note that these are not to be employed simultaneously. Guidance on the choice can be obtained in the manuscript. 
The extrapolation step then employs a linear extrapolant to extrapolate the relation between estimates and average MPR to the case of no error.
The code also provides the jackknife variance estimator for the pMC-SIMEX estimator.
