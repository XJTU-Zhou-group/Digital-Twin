There are 7 files in data&code file:
1_Read_Data,
2_Output_BackgroundGrid,
3_IDW,
4_POD-encoder,
5_surrogate model,
6_POD-decoder-prediction,
7_Post_Processing.

In 1_Read_Data file:
The function "raed_sim.m" is a MATLAB function for reading calculation results, 
where "i" represents the index number of the simulation result.

In 2_Output_BackgroundGrid file:
The function "para.m" is a MATLAB function for outputting the background grid of the surge line, where "i" represents the index number of the simulation result.

In 3_IDW file:
The function (interpola.m) is used to project the result of the temperature field calculated by CFD onto the background grid.

In 4_POD-encoder file:
The function (pod_mode.m) is used to get POD modes and obtain the POD reduced state vectors.

In 5_surrogate model file:
This surrogate model mapping function (myNeuralNetworkFunction.m) was built by Deep Learning Toolbox.

In 6_POD-decoder-prediction:
The function (predict_T) is used to predict the surge line temperature distribution under parameters outside the initial range.

In 7_Post_Processing file:
"Sim_main.m" is the main program with two output modes: 
Mode 1（mode_switch=1） only outputs background grid files, "yyi.dat" (a Tecplot file) and "patch_mesh_i.mat" (a MATLAB file); 
Mode 2 (mode_switch=2)  reads the predicted results from the POD-ANN hybrid method and outputs post-processing files.
The function "para_write_sim.m" outputs post-processing files for simulation results, 
while "para_write_pre.m" outputs post-processing files for prediction results. 
The post-processing files can be opened with Tecplot.


