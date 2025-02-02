These notebooks and files form supplemetary code for the paper Clarke et al. (2020).
Written in Python 3 (v.3.7.1), and presented in Jupyter notebooks (v.5.7.4).

The notebooks go step-by-step through the process of calculating the probability of 
inundation by pyroclastic density currents (PDCs) from and around Aluto volcano.

These notebooks need to be run in order, as they sequentially produce outputs used by the
next notebook.

Step 1. vent_opening_notebook or input_weight_notebook
Step 2. vent_opening_notebook or input_weight_notebook
Step 3. Importance sampling notebook

--------------------------------------

Alongside these notebooks are all the supporting files required to run them:

/source_files
	/aluto_vents 	<-- UTM coordinates of exisitng vents at Aluto
	/grid_x 	<-- UTM values of columns of desired output .tiff file
	/grid_y 	<-- UTM values of rows of desired output .tiff file
	/importance_sampling_overview 	<-- image file used in notebook
	/initial_input_weights 		<-- containing the $\phi$-$H_0$ parameter pairs used for energy cone simulations. Provided in the 'source_files' folder
	/input_weight_calculation	<-- image file used in notebook 
	/vent_loc 	<-- UTM coordinate grid of potential vent locations to investigate
	
	/example_results <-- example subset of output data from the energy cone model

Through using these notebooks, you will populate the 'notebook_output_files_folder' with the follwoing files:

/notebook_output_files
	/input_weights	<-- Generated by the 'input_weight_notebook'. Contains the weights associated with the input parameters for importance sampling
	/inundation_map <-- Generated by the 'Importance_sampling_notebook'. This is the final result, a map of P(PDC|eruption) - georeferenced .tif (EPSG:32637)
	/vent_opening_probabilites <-- Generated by the 'vent_opening_probability' notebook. This has the UTM coordinates of a grid of potential vents used in energy cone modelling, each with a value of P(vent|eruption)

	/processed1_outputs <-- Generated by the 'Importance_sampling_notebook'. These are the partially processed outputs form the energy cone model, required for final compilation and generation of the 'inundation_map.tif'

----------------------------------------

The methodologies presented in these notebooks are adapted by the notebook authors, and are 
approptiately referenced in each notebook. For further information, see Clarke et al. (submitted).

----------------------------------------

These notebooks contain code developed for PVHA at Aluto volcano in Ethiopia. The notebooks themselves are
intended for explanatory use only. Any use or reproduction of this code should be appropriately referenced.
For information surrounding the assumptions and metholodogies employed here, users are directed to our paper:

Ben Clarke, Pablo Tierz, Eliza Calder, Gezahegn Yirgu (2020). Probabilistic volcanic hazard assessment for pyroclastic density currents from pumice cone 	eruptions at Aluto volcano, Ethiopia. Frontiers in Earth Science. doi: 10.3389/feart.2020.00348 
