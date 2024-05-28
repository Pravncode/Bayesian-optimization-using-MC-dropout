# Bayesian-optimization-using-MC-dropout
# Application of Bayesian Optimization on Patch Antenna Dataset using Monte Carlo Dropout
Goal is to find (label) those antenna geometry which gives the minimum of return loss over a given frequency range
Bayesian optimization is employed to achieve this objective
Input data consists of X and Y coordinates of antenna geometry (in mm)
Output (labelled) data consists of return loss of the corresponding antenna
geometry over a frequency range of 2 to 3 GHz
Full wave electromagnetic solver (CST-MWS) is used to label the dataset. Labelling the data is both time and computationally expensive

# Bayesian optimization methodology

➢ A surrogate model (using conv1D anddense layer) is trained over some labelled dataset
➢ Monte Carlo dropout is used during inferencing to get mean and standard deviations of the predictions
➢ Different acquisition functions (PI,LCB and UCB) are deployed in bayesian optimization loop to optimize the exploration and exploitation of unlabelled dataset
➢ Acquisition functions are benchmarked with random search and grid search
