# grooming
Analysis of grooming kinematics in Drosophila melanogaster

The contents of each script or notebook is briefly described below. Note that many of the scripts are dependent on functions within ```grooming_functions.ipynb```.

## dimensionality reduction analysis 

* merge_features.ipynb: merge grooming angles and grooming coords from wt flies (5.22.19, 5.24.19, and 5.27.19)
# manual labels with qualitative grooming observations (height, concentration, 
# left/right bias, etc)


## dynamic mode decomposition (DMD)

* dmd_grooming.ipynb : contains functions for performing DMD on a single grooming bout and tests DMD on a couple examples.
* dmd_parameter_tuning.ipynb : contains functions for performing DMD on a single grooming bout and explores the effect of the number of stacks, number of strides, and SVD rank on the ability of DMD to predict a single grooming bout.
* pydmd_grooming.ipynb : Uses PyDMD to determine the DMD modes and reconstruct a single grooming bout. Also fits DMD on multiple bouts from a single fly except for one, then tries to predict the remainder of the grooming sequence of the bout that was left out. 

## general quantifications
