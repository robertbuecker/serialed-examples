# Serial Electron Diffraction Data Processing
Notebooks and scripts for serial electron diffraction analysis using diffractem (https://github.com/robertbuecker/diffractem) and CrystFEL (https://www.desy.de/~twhite/crystfel/). For the latter, you will need a recent version from the master branch at https://gitlab.desy.de/thomas.white/crystfel -- the 0.9.1. release is too old!

Get the required raw data from MPDL EDMOND at https://dx.doi.org/10.17617/3.53.

The example Jupyter notebooks include:
* `preprocessing.ipynb` - Sorting, movie summation, data viewing, center and peak finding, image artifact correction, background subtraction, creation of intermediate files for indexing.
* `peak_processing.ipynb` - Refinement of experiment geometry and crystal unit cell using the found positions of Bragg peaks.
* `indexing.ipynb` - Crystal orientation finding (indexing), using CrystFELs `indexamajig` tool, some data mangling, and Bragg spot integration (again using `indexamajig`)
* `dose_fractionation.ipynb` - Preprocessing and integration of dose-fractionation movies, using the obtained indexing results.
* `merging.ipynbg` - Merging of Bragg spot observations from all indexed crystals using CrystFELs `partialator`, including pre- and post-processing of data, and validation. Also creates nice figures for validation.
* `merging_fractionated.ipynb` - Another merging script, this time looking at dose fractionated results/radiation damage. Its result may guide the way to optimize which dose fractionation to use in the end.
