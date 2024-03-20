## Overview of the Analysis

**Purpose of the Analysis**

To create a predictive model to evaluate the likelihood of success in the nonprofit foundation Alphabet Soup. The success of this tool means supporting the selection of applicants who fund, the best chance of success on their ventures. It is required we use a model that supports the data (in CSV) provided by Alphabet Soup which includes more than 34,0000 organisations thath ave received funding over the years. The data set includes metadata about each organisation such as Identification, Application, Affiliation, Classification, Use Case, Organisation, Status, Income, Special Considerations, Funding Amount and a measurement of Success. 

## Results

Initial Model:
- 2 hidden layers
- 80 and 30 nodes
- 'relu' activation function on the hidden layers
- Epochs 100
- Accuracy at: 72.56%
- Loss at: 57.97%

![image](https://github.com/IMWILLAU/deep-learning-challenge/assets/61693472/108b3543-6518-47de-81fb-49188a3c9fbc)
![image](https://github.com/IMWILLAU/deep-learning-challenge/assets/61693472/3fd4977b-0f08-417b-bb59-2df92725619c)


Optimisation 1:

Attempt - 1
- 4 hidden layers
- 80, 30, 30 and 30 nodes
- 'relu' activation function on the hidden layers
- Epochs 100
- Accuracy at: 72.63%
- Loss at: 59.59%

![image](https://github.com/IMWILLAU/deep-learning-challenge/assets/61693472/9205b83a-3712-4386-b9f0-3742604b7254)
![image](https://github.com/IMWILLAU/deep-learning-challenge/assets/61693472/c9896cca-5990-43ee-bde6-e04d107b13eb)


Attempt - 2
- 4 hidden layers
- 80, 30, 30 and 30 nodes
- 'relu' activation function on the hidden layers
- Epochs 50
- Accuracy at: 72.59%
- Loss at: 59.13%

![image](https://github.com/IMWILLAU/deep-learning-challenge/assets/61693472/e64a61b8-48dc-41d3-b687-2fd3bc016dac)




**Data Reprocessing**
- Uploaded file to Google Colab
- Read the data from the CSV and turned into a dataframe
- Dropped unneccessary columns 'EIN' and 'NAME'
- Determined unique values
- Looked at APPLICATION_TYPE value counts for binning
- Looked at CLASSIFICATION value counts for binning
- Converted categorical data to numeric with 'pd.get_dummies'
- Split the preprocessed data into features and target arrays
- Scaled the training and ftesting features by creating a 'StandardScalar', fitting into the data then using a transform function

**Compiling, Training and Evaluating the Model**
- Created the neural network model by assigning the number of input features
- Applied the hidden layers
- Created an output layer with activation function 'relu'
- Using keras.layers
- Compiled the model with relevant epochs
Unfortunately not able to reach the accuracy of 75%. Taken further steps with the variations of the parameters as seen above in the results.

## Summary
After testing different variations on parameters, we find that there is a very small room for change in the accuracy of 72%. As shown above, we were able to apply more neurons and hidden layers, reduce the epochs in the training regimen only to find minimal change in the accuracy. After multiple attempts it's found that thus far, 75% accuracy is not achievable with this avaialable data. It would be wise to take into consideration of a different model in order to achieve higher accuracy.

