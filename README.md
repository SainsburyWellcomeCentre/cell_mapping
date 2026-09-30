# cell_mapping
Jupyter notebooks for the protocol: *Whole Brain Cell Mapping: A protocol for Cell Quantification and Atlas Registration*


Notebook `1_Preprocessing_for_QuickNII` takes whole-brain tiff images acquired from a confocal microscope and prepares them for atlas registration in the QUINT workflow. It projects all fluorescence channels into a single greyscale image, downsamples the image to a resolution compatible with QuickNII, and renames each file following the QuickNII naming convention. 

Notebook `2_Pynutil_cell_mapping` maps Imaris detected cells from high-resolution confocal images into the coordinate frame of the corresponding low-resolution whole brain images, and runs PyNutil to assign each cell to a brain region based on the QUINT registration output.

QUNIT workflow: https://quint-workflow.readthedocs.io/en/latest/index.html. 

Pynutil: https://github.com/Neural-Systems-at-UIO/PyNutil

## Installation

Require `PyNutil, nd2, limnd2, tifffile, brainglobe-atlasapi, brainglobe-heatmap`

Install the required packages using pip:

```bash
pip install PyNutil nd2 limnd2 tifffile brainglobe-atlasapi brainglobe-heatmap 
```

## How to use
Download the notebooks and open them in preferred IDEs. Update the configuration cell at the top of each notebook with the correct file paths and settings for your data, then run all cells in order.
