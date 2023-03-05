# deep-learning-challenge
Module 21 Homework

# Background
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

-EIN and NAME—Identification columns
-APPLICATION_TYPE—Alphabet Soup application type
-AFFILIATION—Affiliated sector of industry
-CLASSIFICATION—Government organization classification
-USE_CASE—Use case for funding
-ORGANIZATION—Organization type
-STATUS—Active status
-INCOME_AMT—Income classification
-SPECIAL_CONSIDERATIONS—Special considerations for application
-ASK_AMT—Funding amount requested
-IS_SUCCESSFUL—Was the money used effectively

# Step 1: Preprocess the Data
Using your knowledge of Pandas and scikit-learn’s StandardScaler(), you’ll need to preprocess the dataset. This step prepares you for Step 2, where you'll compile, train, and evaluate the neural network model.

Using the information we provided in the Challenge files, follow the instructions to complete the preprocessing steps.

Read in the charity_data.csv to a Pandas DataFrame, and be sure to identify the following in your dataset:
![image](https://user-images.githubusercontent.com/112498067/222938820-59f87b6f-6546-4c6b-8ddd-cf37580002b5.png)


What variable(s) are the target(s) for your model?
What variable(s) are the feature(s) for your model?
Drop the EIN and NAME columns.
![image](https://user-images.githubusercontent.com/112498067/222938833-41439416-360f-4c8b-88d2-e96bb69d2ea8.png)

Determine the number of unique values for each column.
![image](https://user-images.githubusercontent.com/112498067/222938836-f7b39152-f5b0-4fdd-b37e-54e2103fdc03.png)

For columns that have more than 10 unique values, determine the number of data points for each unique value.
![image](https://user-images.githubusercontent.com/112498067/222938897-83490954-2760-43ed-b0f3-c44e7630dfa0.png)

Use the number of data points for each unique value to pick a cutoff point to bin "rare" categorical variables together in a new value, Other, and then check if the binning was successful.
![image](https://user-images.githubusercontent.com/112498067/222938953-9320fb19-b4e9-45de-a750-960549e5fff6.png)


Use pd.get_dummies() to encode categorical variables.
![image](https://user-images.githubusercontent.com/112498067/222938966-61614284-1c47-4f55-967d-c4f2e29dac3c.png)

Split the preprocessed data into a features array, X, and a target array, y. Use these arrays and the train_test_split function to split the data into training and testing datasets.

Scale the training and testing features datasets by creating a StandardScaler instance, fitting it to the training data, then using the transform function.
