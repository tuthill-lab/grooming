# grooming
Analysis of grooming kinematics in *Drosophila melanogaster*

The contents of each script or notebook is briefly described below. Note that many of the scripts are dependent on functions within ```grooming_functions.ipynb```.

## dimensionality reduction analysis 

* ```dim_red_continuous.ipynb:``` 
* ```dim_red_discrete.ipynb```: Takes the files generated by ```merge_features.ipynb``` and runs PCA, UMAP, and t-SNE on grooming bouts. Colors each point in the 2d embeddings according to the discrete qualitative grooming labels (height, concentration, synchronicity, left/right bias, etc) I made from watching grooming videos.
* ```merge_features.ipynb: Combines grooming angles 3d coordinates from wild type flies to qualitative grooming observations that I made from watching grooming videos (height, concentration, synchronicity, left/right bias, etc)
* pca_umap_tsne.ipynb:
* umap_t1_grooming.ipynb:


## dynamic mode decomposition (DMD)

* dmd_grooming.ipynb: Contains functions for performing DMD on a single grooming bout and tests DMD on a couple examples.
* dmd_parameter_tuning.ipynb: Contains functions for performing DMD on a single grooming bout and explores the effect of the number of stacks, number of strides, and SVD rank on the ability of DMD to predict a single grooming bout.
* pydmd_grooming.ipynb: Uses PyDMD to determine the DMD modes and reconstruct a single grooming bout. Also fits DMD on multiple bouts from a single fly except for one, then tries to predict the remainder of the grooming sequence of the bout that was left out. 

## general quantifications

* coordinates.ipynb: Creates a 3d plot for each grooming bout showing the joint trajectories of T1. Helpful for visualizing the range of motion during grooming.

## processing

* combine_grooming_bouts: Concatenates T1 grooming data from all dates, assigns a unique bout number, and saves the angle and coordinate summaries to separate files.
* grooming_functions.ipynb: 
* manual_classifier: Plots average grooming positions and angles to determine what metrics can be used to distinguish T1 grooming from head grooming, since many head grooming bouts were classified as T1 grooming. Using 5 features (average range of L1B rotation angles, average range of L1A flexion angles, average range of L1E z-coordinates, average z-position of L1D, and average z-position of L1E), calculates a score for each bout. If the score is below a certain threshold, the bout was classified as T1-grooming.
   
