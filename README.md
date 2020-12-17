# CalibrationOfLabMachines
Steps:
1) The normalized data was then imported to Machine Learning Workplace. In the Jupyter Notebook, we used the co-relation plots to understand how different attributes affected the Calibration value. We tried to reduce the attributes to be used in the algorithm by wavering off those which impacted the Calibration in the same way as another.
2) Finally, we determined that ACCEPTABLE_CV_HIGH, LOW_CAL_DEV_TARGET, RATIO and ACCEPTABLE_CV_LOW could be used as inputs/feature attributes to predict the CURVE_SLOPE (target attribute) which is necessary for Calibration calculation.
3) We used SVR model to perform predictive analysis, this involved splitting the data for data modeling/training and testing. Later using the test data to predict the future values. We were successful as the SVR ML model gave us mean absolute error of 0.14795 and explained_variance_score of -0.0107 which is very much below 1, hence proving the model to be more accurate.
4) This predictive analysis would help find the Curve Slope for the future values of inputs and thereby help save the time spent on frequent Calibration Calculations done every day.


Neural Network model:
1) I used Neural Network-Keras MLP Regressor to improve the SVR ML model accuracy through multiple iterations. This gave me an accuracy of 0.9449 upon 100 iterations from initial 0.5524 accuracy of the MLP model. Hence letting me predict the Curve_Slope values more precisely than before.
2) I also generated a subplot to show the Measured vs Predicted values and the test data vs predicted values. 
