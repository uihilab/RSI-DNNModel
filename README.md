# RSI DNN Model
## A DNN MODEL FOR ESTIMATING RESERVOIR CAPACITY LOSS

Welcome to the main repository for the RSI DNN Model for estimating reservoir capacity loss.  This model estimates reservoir capacity loss (acre-ft) from twelve input parameters using a progressively increasing deep neural network model.  It was developed using a dataset containing 467 records (sets of consecutive surveys) from 174 reservoirs located across the U.S. territory.  The model was developed based on a 70/30 training/testing split and once identified as the best-fit model, it was recalibrated using the full dataset.  This model includes the calibration from the full dataset which has the following performance metrics:  R2 = 0.81 and mean absolute percent error (MAPE) values = 48%.  Additional details on the model development and performance are provided by Cox et al., 2023 (https://doi.org/10.31223/X5PH3X).

## Code Files

Two files are provided for application of the DNN model: RSI_Capacity_Loss_Predictor.ipynb and calibrated_best_model.hdf5. The .ipynb file includes the python script for executing the model and the .hdf5 file is used as the calibrated input file for the script.

## Required Input Data

Twelve input parameters are required for the model which are developed based on the time period between two dates:  mean monthly precipitation (in/mo.), maximum monthly precipitation (in), cumulative precipitation (in), drainage basin area (mi2), average basin latitude (°), drainage basin relief (ft), channel slope (ft/ft), average drainage basin curve number (dimensionless), total upstream normal storage (acre-ft), total upstream dam height (ft), drainage basin hydraulic length (ft), initial reservoir capacity (acre-ft).  Additional details on how input parameters can be derived are provided by Cox et al. (2023).

## Example Set of Input Data

The following provides a sample set of input data:

mean monthly precipitation (in/mo.):  1.348
maximum monthly precipitation (in):  5.529
cumulative precipitation (in):  250.4
drainage basin area (mi2):  262,200
average basin latitude (°):  46.09
drainage basin relief (ft):  12,500
channel slope (ft/ft):  0.001035
average drainage basin curve number (dimensionless):  76.33 
total upstream normal storage (acre-ft):  108,800,000 
total upstream dam height (ft):  147,000
drainage basin hydraulic length (ft):  12090000 
initial reservoir capacity (acre-ft):  6,280,000    

## Citation

If you use the model, please cite the following publication:  

Cox, A.L., Meyer, D., Botero-Acosta, A., Sagan, V., Demir, I., Muste., M., Boyd., P., and Pathak., C. (2023). Estimating Reservoir Sedimentation Using Deep Learning. EarthArXiv. DOI:  https://doi.org/10.31223/X5PH3X

## Feedback
Feel free to send us feedback by filing an issue.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

This model was developed by Saint Louis University and the University of Iowa Hydroinformatics Lab (UIHI Lab, https://hydroinformatics.uiowa.edu) with input from the U.S. Army Corps of Engineers. This research was supported by the U.S. National Science Foundation (Award # 1948940) and the WATER Institute at Saint Louis University.
