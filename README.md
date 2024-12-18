# Molecular Dynamics MMPBSA Analysis

## Overview
	This is a program written to compare molecular dynamics methods used to determine the MMPBSA of a set of protein complexes. The sample data included compares data obtained through molecular dynamics simulations. One set has been obtained using 'Standard' molecular dynamics protocols with a timestep of 2fs. The other set has been obtained similarly but with the implementation of hydrogen mass repartitioning ('HMR'). Both are compared to the experimentally obtained values. The program can be altered to compare a number of different methods to obtain measurements beyond molecular dynamics and MMPBSA.

## Requirements
	To run you will need to have python installed, including the following necessary modules:
		numpy
		pandas
		matplotlib
		sklearn
		scipy
	The code is written in a Jupyter Notebook, which can be run through your preferred development environment. Alternatively you can install Jupyter using pip or conda and run it from the command line using the following command:

		jupyter nbconvert --execute Simulation_Analysis.ipynb --output Simulation_Analysis.ipynb

	Edit the output file name if not wanting to overwrite the original.

## Execution
	To run:

	1. Download the Simulation_Analysis python notebook as well as all your raw data / sample data sets in this repository into a single directory.
	
	2. Install the necessary python modules and jupyter if necessary.
	
	3. Edit file and data names as needed. The notebook is currently set up to process the sample data provided. Note if using raw data that does not follow the formatting conventions of the sample data the data processing function will need to be edited accordingly. If testing more than two methods then edit the subplot number and add in plot commands as needed.

	4. Run the notebook within your development environment or by using the command provided above.
		The 1st cell collects and organises the datasets into one combined dataframe.
		The 2nd cell plots the MMGBSA values for each computational method against the experimental values, including linear regression.
		The 3rd cell calculates statistics metrics for both computational datasets.

## Output
	The combined data is found in MMPBSA_avg.csv.
	Visualisation of the computational vs experimental data is found in MMPBSA_avg.csv.
	Statistical analysis metrics are found in MMPBSA_metrics.csv. 
