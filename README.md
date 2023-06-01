# DeepLearning-21
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special considerations for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

## Overview 
The overall purpose of this analysis is to prepare the dataset for a machine learning model by performing data preprocessing steps, splitting the data into training and testing sets, and scaling the features appropriately. These steps are crucial for building and evaluating machine learning models effectively.

## Results

# Data Processing 
- The target variable in this model is the "IS_SUCCESSFUL" column.
- The feature variables in the final model were:
* NAME
* APPLICATION_TYPE
* AFFILIATION
* CLASSIFICATION
* USE_CASE
* ORGANIZATION
* INCOME_AMT
* ASK_AMT
-The variables that were removed from the final model were:
* EIN - just an id number
* SPECIAL_CONSIDERATIONS - this column had over 34,000 'N' values and only 27 'Y' values. Not helpful.
* STATUS - this column had over 34k 1's and only 5 0's - only five of the rows are zeroes which is not helpful

# Compiling, Training, and Evaluating the Model 
- The final model had three layers. The first layer had 100 neurons or nodes, the second layer had 30 neurons, and the third layer had 10 neurons. The model used two different activation functions - rectified linear units (relu) and sigmoid. The accuracy being 78% exceeding the target performance of 75%.
- So as to increase the performance of the Model, the following steps were performed:
* Removed two columns from the main model i.e., SPECIAL_CONSIDERATIONS and STATUS.
* Included Name column.
* Added three layers so as to increase the complexity.
* The activation functions on the second and third layers as well as the output layer were changed.

# Summary 
The analysis involved comparing the performance of a tuned neural network with an original neural network and a random forest classifier. The tuned neural network achieved a notable increase in accuracy, reaching 79% compared to the original network's 73% accuracy. This improvement was achieved by incorporating the organization name as a feature, removing special considerations and status from the feature variables, increasing model complexity with an additional hidden layer, and modifying activation functions. In parallel, the random forest classifier achieved 78% accuracy, surpassing the desired 75% threshold but falling slightly short of the tuned neural network. The results indicate that further fine-tuning could potentially enhance the predictive performance of either model, leading to even better classification accuracy.

