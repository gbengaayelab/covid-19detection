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

## Usage

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

## Contributing

If you find a bug or have a feature request, please open an issue or submit a pull request. We welcome contributions from the community!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.