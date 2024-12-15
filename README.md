# deep-learning-challenge

The present challenge involves using machine learning and neural networks to predict if applicants will be successful if funded by Alphabet Soup, a nonprofit organization. By using the features in the provided dataset (see below), the challenge involved creating a binary classifier that could predict whether applicants will be successful, if funded by Alphabet Soup.

The data used for this challenge can be found in the link below:
https://static.bc-edx.com/data/dl-1-2/m21/lms/starter/charity_data.csv

The CSV file contains over 34,000 organizations that have received funding from Alphabet Soup over the years. These data were used to develop the mentioned model.

The present repo contains several iterations of the code, which aimed to increase the model performance. The repo organization is as follows:

- AlphabetSoupCharity.ipynb: original code, where the model performance was approximately 73.0%

- AlphabetSoupCharity_Optimization_1.ipynb: first optimization of the code, where the model performance was only 72.4%, lower than the original iteration of the code. In this iteration of the code, the units of the first and second layers were changed to 20, and a third layer was added, with units = 8. "Relu" was used as the activation parameter.

- AlphabetSoupCharity_Optimization_2.ipynb: second optimization of the code where the model performance was 74.2%, higher than the previous iterations, but not reaching the goal of at least 75.0%. This iteration of the code was similar to the first optimization, but in addition to adding a layer and modifying the units values, only the column 'EIN' was dropped.

- AlphabetSoupCharity_Optimization_3.ipynb: in this final optimization of the code, the model's performance increased to 75.9%. This iteration of the code was similar to the second optimization, with the additional modification of choosing a lower cutoff value (i.e., 10)(see code).

- h5_files folder contains the h5 files generated during each of the code iterations and optimizations.

- report.md: file that contains a brief discussion and interpretation of the results.


