<p align="center">
  <img align="center" alt="SafeURL logo" width="150" src="https://raw.githubusercontent.com/thechiranjeevvyas/SafeURL/refs/heads/main/webapp/assets/SafeURL.jpeg">
</p>

# SafeURL

Malicious URL Detection Model Neural Network Optimized by Genetic Algorithms made by [@thechiranjeevvyas](https://github.com/thechiranjeevvyas)

## About

SafeURL is a web application implementing a Multilayer Perceptron Neural Network optimized using genetic algorithms.
Detect whether a domain name or URL is malicious by inputting a URL. For instance,

```
https://www.google.com -> SAFE
yourbittorrent.com/?q=anthony-hamilton-soulife -> MALICIOUS
```

## Previews

<img alt="Preview 2" width="800" src="https://raw.githubusercontent.com/thechiranjeevvyas/SafeURL/refs/heads/main/webapp/assets/preview.png">

## Neural Network Model

<img alt="Model Image" width="800" src="https://raw.githubusercontent.com/thechiranjeevvyas/SafeURL/refs/heads/main/webapp/assets/model_graphic.png">

The model sequence defined within `genetic_algorithm_implementation.py` is as follows:

1. Integrate CSV Dataset and Remove Unnecessary Columns
2. Use SMOTE to Balance out Class Distribution in Dataset
3. Split Dataset into Training and Testing Sets using 80:20 Ratio
4. Initialize Multilayer Perception
5. Utilize Adam Optimization and Binary Cross Entropy Loss Function
6. Initialize Model Callback to Wait Until 0.1 Validation Loss
7. Train Model with 10 Epochs and Batch Size of 256
8. Verify Model Results using 10 Examples
9. Run Each Model Iteration through a Genetic Algorithm
10. Evaluate Fitness of Each Model by Referencing Accuracy
11. Determine Best Model within Population
12. Save the Best Model into a .h5 File Output

## Usage

To build from source, you will Python3 and Pip installed.

```
cd webapp
pip install -r requirements.txt
streamlit run app.py
```

Visit `localhost:8501` to see the web application

## Code Structure

### Research Jupyter Notebooks

The `Research_Notebooks` folder contains the Jupyter research notebooks for this project. Each notebook explores a unique aspect of the dataset.

`Feature_Extraction_Notebook.ipynb` extracts pertinent information out of the malicious and benign URLs Kaggle dataset

`Data_Visualization_Notebook.ipynb` provides relevant data visualizations of the features extracted in the feature extraction notebook

`Training_Models_Notebook.ipynb` tests a couple of models to classify which one is best suited for detecting malicious domains

`Genetic_Algorithm_Notebook.ipynb` experiments with genetic algorithms and applies it to a neural network

### Streamlit Web Application

The `webapp` folder contains all the necessary files to setup the web server for the application.

Once you execute `streamlit run app.py` visit `localhost:8501` in a browser to see the application.

The `app.py` file contains all the relevant Streamlit web application code.

The `model_generation.py` file contains the code to generate the classification NN without GA optimization.

The `genetic_algorithm_implementation.py` file contains the code to generate the classification NN with GA optimization.

## Contributing

SafeURL is open to any contributions. Please fork the repository and make a pull request with the features or fixes you want to be implemented.
