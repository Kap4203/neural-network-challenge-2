# neural-network-challenge-2
This project aims to develop a neural network model to predict two key outcomes in an employee attrition dataset:
1. **Department Assignment** (Multi-class classification)
2. **Attrition Likelihood** (Binary classification)

## Project Overview
The objective of this project is to help Human Resources (HR) predict which department an employee belongs to and whether they are likely to leave the company. To do this, the neural network is trained using a dataset containing various features about employees, such as age, satisfaction levels, years at the company, and whether they work overtime.

## Key Features:
* Department Prediction: Classifies employees into one of three departments (Sales, R&D, HR) using the softmax activation function.
* Attrition Prediction: Uses the sigmoid activation function to predict whether an employee is likely to leave the company.

## Dataset
The dataset used for this challenge is a pre-processed employee dataset containing the following features:
* Age
* DistanceFromHome
* EnvironmentSatisfaction
* JobSatisfaction
* OverTime
* TotalWorkingYears
* WorkLifeBalance
* YearsAtCompany
* YearsInCurrentRole
* YearsSinceLastPromotion
* NumCompaniesWorked
* TrainingTimesLastYear
* Target Variables:
* Department: Multi-class target (3 categories: Sales, R&D, HR).
* Attrition: Binary target (Yes/No).

## Neural Network Architecture
The neural network architecture consists of:
* Input Layer: Takes in 12 features (after encoding and scaling).
* Shared Hidden Layers:
    * Dense layer with 16 units, ReLU activation
    * Dense layer with 8 units, ReLU activation
* Department Branch:
    * Hidden layer with 4 units, ReLU activation
    * Output layer with 3 units, softmax activation for multi-class classification
* Attrition Branch:
    * Hidden layer with 4 units, ReLU activation
    * Output layer with 1 unit, sigmoid activation for binary classification

### Loss Functions
* Categorical Crossentropy for the department output
* Binary Crossentropy for the attrition output

### Optimizer
Adam optimizer is used for training.

### Metrics
Accuracy is used for both department and attrition predictions.

## Results
The model was evaluated using accuracy metrics for both tasks:
* Department Prediction Accuracy: ~65%
* Attrition Prediction Accuracy: ~86%

The model could potentially be improved by:
* Handling class imbalance for the attrition prediction.
* Tuning hyperparameters such as learning rate and batch size.
* Experimenting with advanced architectures or regularization techniques.

## How to Use
1. Clone the repository and navigate into the project directory
2. Open the Jupyter notebook 'attrition.ipynb' to view the complete code and execute the model

### Dependencies
* pandas
* numpy
* sklearn
* tensorflow

### Directory Structure
```python
neural-network-challenge-2/
├── attrition.ipynb  # Jupyter notebook containing the full implementation of the model
├── LICENSE          # License file
└── README.md        # Project description and instructions
```

## License
This project is licensed under the Unlicense. See the LICENSE file for more details.

## Author
David Kaplan