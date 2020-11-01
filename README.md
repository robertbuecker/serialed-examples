# Serial Electron Diffraction Data Processing
Notebooks and scripts for serial electron diffraction analysis using diffractem (https://github.org/robertbuecker/diffractem) and CrystFEL (https://www.desy.de/~twhite/crystfel/ or https://stash.desy.de/projects/CRYS/repos/crystfel/). Both are mandatory dependenices to make any sense out of this.

Get the required raw data at https://empiar.org via the accession code `EMPIAR-10542`

The example Jupyter notebooks include:
* `preprocessing.ipynb` - Sorting, movie summation, data viewing, center and peak finding, image artifact correction, background subtraction, creation of intermediate files for indexing.
* `peak_processing.ipynb` - Refinement of experiment geometry and crystal unit cell using the found positions of Bragg peaks.
* `indexing.ipynb` - Crystal orientation finding (indexing), using CrystFELs `indexamajig` tool, some data mangling, and Bragg spot integration (again using `indexamajig`)
* `merging.ipynbg` - Merging of Bragg spot observations from all indexed crystals using CrystFELs `partialator`, including pre- and post-processing of data, and validation. Also creates nice figures for validation.
