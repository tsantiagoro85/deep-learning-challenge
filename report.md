# Report deep-learning-challenge

## Analysis overview:
The present challenge aimed to apply machine learning and neural networks to predict if applicants will be successful if funded by Alphabet Soup, a nonprofit organization. By using the features in the dataset found in the link below, the challenge involved creating a binary classifier that could predict whether applicants will be successful if funded by Alphabet Soup.

## Methods overview:
To achieve this, data were read from the link:
https://static.bc-edx.com/data/dl-1-2/m21/lms/starter/charity_data.csv

Once imported, a pre-processing stage involved various steps including, but not limited to dropping specific columns (depending on the optimization iteration). Cutoff values were used to create a list of classifications to be replaced. These values may have differed depending on the iteration of the code used. Pre-processed data were split into features and target arrays, and into training and testing datasets using train_test_split(). StandardScaler instances were created, the StandardScaler was fit, and the data were scaled.

Finally, the model was compiled, trained and evaluated. Briefly, two to three hidden layers were used, depending on the iteration of the code used. The model was compiled using model.compile() and trained using model.fit(). The model was then evaluated using model.evaluate().

## Results overview: 
Several iterations of the code were attempted until reaching at least 75% accuracy, which was achieved in the last iteration of the code (i.e., 75.9%).

Data Preprocessing:

What variable(s) are the target(s) for your model? The target variable of the model is the column 'IS_SUCCESSFUL'.

What variable(s) are the features for your model? The variables that are the features for the model are those other than 'IS_SUCCESSFUL', which is the target variable, and the two columns that were initially dropped in preprocessing, 'EIN' and 'NAME'. Therefore, the variables that are features include 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS', and 'ASK_AMT'.

What variable(s) should be removed from the input data because they are neither targets nor features? As shown in the original code and the following iterations, the variables 'EIN' and 'NAME' should be removed from the input data since they are neither targets nor features. However, dropping only the column 'EIN' aided in increasing the model performance in later iterations of the code.

Compiling, Training, and Evaluating the Model:

How many neurons, layers, and activation functions did you select for your neural network model, and why? The number of initial neurons used changed on subsequent iteration of the code. Unlike the original code, the iterations of the code used 20 neurons in the first and second hidden layers, and 8 neurons in the third hidden layer. One neuron was then used in output layer. In terms of the activation functions, the 'relu' activation was used. The 'sigmoid' function was utilized in the output layer since values are normalized to a probability between 0 and 1, which is ideal for a binary classification dataset as the one in the present challenge.

Were you able to achieve the target model performance? The model performance was 75.9% after three optimization iterations, hitting the target of a minimum of 75.0%.

What steps did you take in your attempts to increase model performance? Several steps were taken to increase the model performance, depending on the optimization. Briefly, in the first optimization of the code, the achieved model performance was 72.4%, lower than the original iteration of the code. Here, the units of the first and second layers were changed to 20, and a third layer was added, with units = 8. "Relu" was used as the activation parameter. On the second optimization of the code, the model performance was 74.2%, higher than the previous iterations, but not reaching the target of at least 75.0%. This iteration of the code was similar to the first optimization, but in addition to adding a layer and modifying the units values, only the column 'EIN' was dropped. In the final iteration of the code, the model's performance increased to 75.9%. This iteration of the code was similar to the second optimization, with the additional modification of choosing a lower cutoff value (i.e., 10)(see code). 
