# Analysis Code for Savage et al 2026 eLife

## Multi-electrode Array Recording
This code classifies retinal spiking data into spontaneous retinal waves and quantifies wave behaviour. 
1. To run code please use `runWaveMaster.m` and follow instructions

## Microglia Quantification
This package has a number of scripts to help run microglia morphometry analysis (see https://github.com/embl-cba/microglia-morphometry). 
Initial microglia masks can be created using the morphometry plugin or something like Labkit in FIJI.

1. `trackMicrogliaMasksSingleIm` allows for modification of masks
2. `countYoPro_HMXO1` counts the occurrence of microglia and yo-pro positive cells
3. `calcuateYoPro_D1_2_3` produces D1/2 and D1/3 values for yopro or microglia cells in full retina IHC images. 


## Calcium Imaging
Complete Guide to Code Installation and Use

This toolbox is designed to allow the user to extract calcium imaging activity data. This toolbox also contains scripts to quantify retinal wave parameters and metrics. 

Software requirements:
1.	Download toolbox and add to Matlab path
3.	If you want to be able to use no rigid motion correction please clone the non-rigid motion correction toolkit (https://github.com/flatironinstitute/NoRMCorre) 
4.	Install an up to date version of FIJI (https://fiji.sc/) 
5.	Connect FIJI with matlab as explained here (http://bigwww.epfl.ch/sage/soft/mij/) NB, instead of using ij.jar, place the up to date version from your FIJI package (FIJI.app/jars), it will be named something like ij-1.52g.jar into the MATLAB folder.
6.	Install Cell Magic Wand into FIJI (https://www.maxplanckflorida.org/fitzpatricklab/software/cellMagicWand/) OR (https://github.com/GrimmSnark/Cell_Magic_Wand)
7.	Install CaImAn-MATLAB analysis package from github, this package uses some of their functions (https://github.com/flatironinstitute/CaImAn-MATLAB ).
8.	You may need to increase your java heap size for FIJI and matlab to work with large images see (https://www.mathworks.com/matlabcentral/answers/92813-how-do-i-increase-the-heap-space-for-the-java-vm-in-matlab-6-0-r12-and-later-versions) NB use the java.opts method. 
9.	You will need to modify the "intializeMIJ.m" to your local FIJI path.

To run the analysis:
1. Use prepCalciumData to run preprocessing
2. Use 
