# Neural_Network_Charity_Analysis
The fictitious company AlphabetSoup asked for a binary classifier that could predict whether organizations would be successful if AlphabetSoup provided funding to them. Alphabet Soup has provided a dataset that includes over 34,000 organizations that have received funding from them. 

This dataset captured the following:
- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special consideration for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively
A neural network model was created to determine whether an applicant will be successful if funded by Alphabet Soup. Alphabet Soup requires the target prediction accuracy of the model to be 75%.

# Resources
charity_data.csv
sci-kit learn model_selection Documentation
sci-kit learn preprocessing StandardScaler Documentation
sci-kit learn preprocessing OneHotEncoder Documentation
TensorFlow Documentation Documentation
TensorFlow Keras Documentation

# Tools
GoogleColab
- new m1 macbook had problem running the kernel ***"Kernel Restarting The kernel appears to have died. It will restart automatically" 
Python v3.x
Pandas
OS
Sci-Kit Learn
TensorFlow
Keras

# Results

The first attempt to achieve 75% prediction accuracy used two hidden layers with 80 neurons in the first layer and 30 neurons in the second. Both hidden layers used the rectified linear unit (ReLU) activation function. The output layer uses the sigmoid function. This gave a total of 6061 trained parameters and 0 untrained parameters. This model accuracy was 72.5% 

![Screen Shot 2022-04-11 at 4 33 39 AM](https://user-images.githubusercontent.com/94031446/162697230-bd40391b-7b92-439e-88f3-cbbbb754cf0d.png)

After further Optimization of the model, accuracy was 75.9%

![Screen Shot 2022-04-11 at 4 34 08 AM](https://user-images.githubusercontent.com/94031446/162697313-b4562b8c-1447-43ed-a542-727a6f3f1985.png)

**What variable(s) are considered the target(s) for your model? 

"Is Successful" is the target variable for this model.

**What variable(s) are considered to be the features for your model?

All columns are features of this model. However, a targeted variables such as "EIN" and "NAME" were removed on the first trial and "EIN" on the optimization trial to improve the accuracy of the model.

**What variable(s) are neither targets nor features, and should be removed from the input data?

Variables such as null values, empty cells, and outliers should be removed.

**How many neurons, layers, and activation functions did you select for your neural network model, and why? 

3 layers were used to improve the ML module to get 75.9% instead of the first trial that used 2 layers. The first second and third layers on the second trial have 180 neurons, 60 neurons, and 40 neurons respectively. In addition, the activation function used on this model is  "relu" since it provided the best accuracy. 

![Screen Shot 2022-04-11 at 4 35 39 AM](https://user-images.githubusercontent.com/94031446/162697585-390e8049-6823-4fef-8114-303ec4776251.png)


**Were you able to achieve the target model performance?

Yes, the model accuracy was improved to 75.9%,  the previous score was 72.5.

**What steps did you take to try and increase model performance?

Initially changing the activation function was attempted which was unsuccessful. Bring back "NAME column and adding layers as well as configuring few value helped increase performance.
