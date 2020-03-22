# Energy-Efficieny-prediction
What is my dataset?

We perform energy analysis using 12 different building shapes simulated in Ecotect. The buildings differ with respect to the glazing area, the glazing area distribution, and the orientation, amongst other parameters. We simulate various settings as functions of the afore-mentioned characteristics to obtain 768 building shapes. The dataset comprises 768 samples and 8 features, aiming to predict two real valued responses. It can also be used as a multi-class classification problem if the response is rounded to the nearest integer.

1.	Dataset description

The dataset contains eight attributes (or features, denoted by X1...X8) and two responses (or outcomes, denoted by y1 and y2). The aim is to use the eight features to predict each of the two responses.

Specifically:

•	X1 Relative Compactness
•	X2 Surface Area
•	X3 Wall Area
•	X4 Roof Area
•	X5 Overall Height
•	X6 Orientation
•	X7 Glazing Area
•	X8 Glazing Area Distribution
•	y1 Heating Load
•	y2 Cooling Load

Why my dataset?

	
	1) Relevant data although collected in 2012.
	2) Multivariate Data characteristics.
	3) Able to perform both classification or regression analysis.
	
What am I doing?
In terms of regression, this fact actually means that if we manage to develop a model that returns (predicts) relatively good values for one of the two response values, the same model should predict relatively good values for the other (with a small error differentiation of course).

Conclusion

1.By performing the data analysis of the Energy Effiency dataset, we learn that it is an estimation(prediction) problem where we determine the targets: Heating Load and Cooling Load.

2.We use linear regression to predict the values of Heating Load and Cooling Load since the data is continuously distributed in all the attributes. bold text

3. Reasons for not using other techniques

We do not use logistic regression because we are not classifying the data and logistic regression works well for classification problems(the target variables are not binary categorical 0's or 1's)
The dataset used is quite small with 768 instances and only 8 attributes, hence linear regression is preferred over neural networks. The possibility of overfitting the model in neural networks is eliminated by opting linear regression.

4.Although the data is continuous, it is sparse when correlated with the response variables. Therefore KNN is not used.(The dimensions of the data increases significantly).
The prediction of Heating Load and Cooling Load : Due to high correlation between them, the prediction of either value should lead to the other value. This Hypothesis is confirmed true when we could predict the values of both the Heating Load and Cooling Load with minor difference.

5.Significance of the negative difference:

prediction_difference_train = -0.012755235409825427

prediction_difference_test = -0.03932872623790673

This states that “Cooling Load” max value is about 5KW larger than “Heating Load” max value and “Heating Load” min value is about 4KW lower than “Cooling Load” min value. For this particular dataset we can say that the energy needed to cool the house is slightly greater than that required to heat it.


