# Neural_Network_Charity_Analysis
# MEMORANDUM
#
# To: Grant Department
# From: Bob
# Re: Update on Neural Network-Based Projections for Funding Decisions
#
# Overview of Project
## We initiated the development a neural network model in the hope of increasing the favorable outcome of our grants. This model, which leverages all data from our existing project database, has provided only moderately accurate results so far. Alternate model structures should be considered to increase its accuracy to an appropriate level.
#
# Methodology and Results
# Data Preprocessing
## Our work has focused on developing a complex neural network model to help predict the likeliness of successful projects funded by our organization. As such, the “IS_SUCCESSFUL” rating which is assigned at the end of each project has been the target for our model.
#
## Based on our qualitative examination of the dataset, we decided to initially include most available information into our analysis. Our neural network model reflected input values for APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS and ASK_AMT. As neural network models can only use numerical values, we converted certain text data (e.g. ORGANIZATION) into four binary (i.e. yes/no) variables based on potential organization choices (Association, Co-Operation, Corporation, Trust). 
#
## We appreciate having access to all parameters for all projects. However, arbitrary values (e.g. EIN) and other descriptive information (e.g. NAME) were not considered as factors in this analysis.
#
# Compiling, Training and Evaluating the Model
## We relied on typical rules of thumb for our initial model design. Since we had 43 variables (aka features) and wanted the neuron count between two and three times the number of features, we choose 110 as our neuron count and divided them between two hidden layers. We chose the “relu” activation function for the hidden layers due to their anticipated non-linear behavior and “sigmoid” activation for the output since we sought results of either 0 (not successful) or 1 (successful).
#
## Our initial model performance only reached 53% accuracy, far below our accuracy threshold of 75%. 
#
## Repeated efforts to improve our neural network model did not substantially increase its accuracy. We undertook numerous modifications to the initial model including (1) reducing the number of features considered in the calculations, (2) converting INCOME_AMT from inconsistent quantitative data to consistent categorical data, (3) bucketing several minor AFFILIATIONS into an “other” category, (4) increasing the number of neurons to 150 and (5) changing activation function in the hidden layer. None of these modifications brought our model close to the 75% accuracy target.
#
# Summary – The results of our initial work suggest that a neural network model may not offer the best option for meeting our prediction needs. Based on the categorical nature of our data, we suggest a new effort to develop a machine learning model based on logistic regression algorithm to meet our needs.
