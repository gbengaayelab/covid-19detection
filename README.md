# Covid-19 Detection Model

This is a machine learning model for predicting whether a person has Covid-19 based on their symptoms. It uses a Decision Tree Classifier algorithm to classify the input data as either "Covid-19 Detected" or "No Covid".

## Dependencies

Before running this code, ensure that you have the following dependencies installed:

- pandas
- scikit-learn
- matplotlib
- joblib

You can install these dependencies using pip:

```
pip install pandas scikit-learn matplotlib joblib
```

## Getting Started

To get started, clone this repository and navigate to the root directory:

```
git clone https://github.com/gbengaayelab/covid-19detection.git
cd your-repo
```

Next, run the following command to train the model:

```
python train.py
```

This will read the `CovidDataset.csv` file, preprocess the data, and train the model. The trained model will be saved in a `joblib` file called `covid-19detection.joblib`.

Finally, you can run the following command to test the model:

```
python test.py
```

This will test the model on a small set of sample data and print the accuracy score to the console.

## Dataset
The CovidDataset.csv file contains data used to train the model. The dataset consists of records with 21 features including "Breathing Problem", "Fever", "Dry Cough", "Sore throat", "Running Nose", "Asthma", "Chronic Lung Disease", "Headache", "Heart Disease", "Diabetes", "Hyper Tension", "Fatigue", "Gastrointestinal", "Abroad travel", "Contact with COVID Patient", "Attended Large Gathering", "Visited Public Exposed Places", "Family working in Public Exposed Places", "Wearing Masks", and "Sanitization from Market". The target feature is "COVID-19", which indicates whether the person has Covid-19 or not.



## Usage

Building the model
The covid-19_detection.py file contains code for building the model. The first step is to import the required modules and load the dataset into a pandas dataframe. The dataset is then split into input and output datasets. The input dataset contains all the features except the target feature "COVID-19", and the output dataset contains only the target feature.

Next, the input dataset is preprocessed by replacing the text values "Yes" and "No" with 1 and 0 respectively. Similarly, the target feature is also preprocessed by replacing "Yes" with "Covid-19 Detected" and "No" with "No Covid".

The preprocessed data is then split into training and testing datasets using the train_test_split function. A Decision Tree Classifier model is then created using the DecisionTreeClassifier function and trained with the training datasets.

The accuracy of the model is calculated using the accuracy_score function and saved using the dump function from the joblib module.

Predicting Covid-19
The covid-19_detection.py file can also be used to predict Covid-19 based on input symptoms. To do this, the saved model is loaded using the load function from the joblib module. The model is then used to predict Covid-19 based on sample input datasets.

The predictions are then plotted on a bar chart using the matplotlib module.


You can use the trained model to make predictions on new data by importing the `joblib` file and calling the `predict` method. Here's an example:

```
import joblib

# Load the model from the joblib file
model = joblib.load('covid-19detection.joblib')

# Make predictions on new data
prediction = model.predict([[0,1,1,1,0,1,1,1,0,0,1,0,1,1,0,1,0,1,1,1]])

print(prediction)
```

This will print either "Covid-19 Detected" or "No Covid" to the console, depending on the input data.


## Conclusion
This project demonstrates how a Decision Tree Classifier model can be used to predict Covid-19 based on symptoms. The model achieves high accuracy, making it a potentially useful tool for detecting Covid-19 in patients.

## Contributing

If you find a bug or have a feature request, please open an issue or submit a pull request. We welcome contributions from the community!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.