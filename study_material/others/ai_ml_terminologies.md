
# Neural Networks and Deep Learning
- Neural networks reflect the behavior of the human brain, allowing computer programs to recognize patterns and solve common problems in the fields of AI, machine learning, and deep learning.
- Weights and Biases are adjusted by a neural network as it learns from a training dataset

## Feature engineering
To learn more about features, click [here](https://github.com/singhgautam7/GCP-PDE-preparation---GRS/blob/main/study_material/others/ai_ml_terminologies.md)
### Definition
Manipulation of features to improve the quality and predictive capabilities of machine learning models. This is known as feature engineering.
### Steps
- Identify useful features
- Features may be in original data but might need some transformations
- Features derived from other features.
### Ways to engineering features
- Transform the orginal features
	- Ex: Lower case words and remove punctuation
	- Map Numeric valriable to a scale of 0 to 1 if the different features are from different numeric range (**Normalization**)
- Bucketing
	- Create sub-groups of feature values
	- This reduces number of values
- Feature cross	
	- Cartesian product of two or more features
	- Helps when there are non-linear relationships
- Binary features
	- Ex: is_red, is_blue etc
- Decompose values to parts
	- Ex: From date extract year, month and day

## One-Hot Encoding
- Map from an attribute value to a single bit in a binary array
- Each postion in array represent a possible value
- Ex: Red represent 100, Blue represent 010 and Green represent 001. Here we mapped colors to three different binary arrays

# Common Facts/Terminologies for examination

### Clustering
It is unsupervised learning technique for identifying group of similar entities

### Normalization
It is a transform that scales numeric value to the range 0 to 1

### Bucketing
It is used to convert a feature bin to multiple binary features that is typically based on a value range.
Ex: A grade for marks 80 - 100, B grade 60 - 79 and so on

### Regularization
Limiting the information captured by model to prevent overfitting.

### Overfitting
- Fits too well with the training data
- When the model performs great on the input(training) data but poorly on the test data
- Correction for overfitting: 
        - Regularization, which limits the amount of data captured. The higher the degree of the regularization, the more you can prevent overfitting.

### Underfitting
- When the model performs poorly on the input(training) data but great on the test data. 
- Correction for underfitting: 
        - Increase the complexity of model. Ex: Increase the number of layers in deep learning.
        - Increase the training time, epochs

### High Variance
 - Small changes in a few features leads to large differences in the output.
 - Low variance is desired

### High Bias
- Occurs when relationships are missed.
- Low bias is desired
- Happens when we do not generalize the training data enough 

<details><summary>Bias vs Variance</summary>
<p>

![enter image description here](https://community.alteryx.com/t5/image/serverpage/image-id/52874iE986B6E19F3248CF?v=v2)

</p>
</details>

### Learning rate
- Increasing the learning rate = Fast learning (at the risk of possibly missing the absolute optimal solution)
- Decreasing the learning rate = Slow learning

### Hyperparameters
- Hyperparameters are values that need to be selected before training process begins also can be modified during training
- Hyperparameters are parameters whose values control the learning process and determine the values of model parameters that a learning algorithm ends up learning.
- Ex: 
	- Learning Rate.
	- Number of Epochs.
	- Momentum.
	- Regularization constant.
	- Number of branches in a decision tree. 

### Difference between of Parameters and Hyperparameters
| Parameters | Hyperparameters |
|--|--|
| Estimated during the training with historical data | Values set beforehand |
| It is a part of the model | External to the model |
| The estimated value is saved with the trained model | Not a part of trained model, hence values aren't saved |
| Dependent on the dataset that the system is trained with | Independent of the dataset |

### Difference between of Features and Labels
|Features|Labels|
|--|--|
|Attribute of an entity|Attribute that is predicted|
|Describe characteristics of an entity|Category of an entity|
|Acts as I/P variable|Acts as O/P|

### Example of Features and Labels
|Features|Labels|
|--|:-:|
|No. of rooms, no. of bedrooms, size of kitchen, zip code etc.|Selling Price|
|Petal length, petal widh, sepal length, sepal width|Flower Species|
|Amount, product purchased, time of day, location|Fraud/Not Fraud|
|Age, occupation, zip code, no. of years of education|Income|

# Some other Terminologies
<details><summary>click to expand</summary>
<p>
	
### Tensorflow Terminologies
(Taken from this [link](https://medium.com/google-cloud/a-tensorflow-glossary-cheat-sheet-382583b22932))
-   **Train/Eval/Test** — Training is data used to optimize the model, evaluation is used to asses the model on new data during training with new data, test is used to provide the final result
-   **Classification/Regression —** Regression is prediction a number (e.g. housing price), classification is prediction from a set of categories or output classes (e.g. prediction the color of a house from red/blue/green).
-   **Linear regression-** A classic way of predicting an output by multiplying and summing input features with weights and biases. Useful for regression
-   **Logistic regression —** Similar to linear regression but predicts a probability, useful for classification.
-   **Neural network —** Like linear/logistic regression, but with the addition of an activation function, that makes it possible to predict outputs that are not linear combinations of inputs. Often intermediate layers of nodes are used “deep learning”.
-   **Weights / biases** — Weights are values that the input features are multiplied by to predict an output value. Biases are the value of the output given a weight of 0.
-   **Converge —** An algorithm that converges will eventually reach the optimal answer, even if very slowly. An algorithm that doesn’t converge may never reach the optimal answer.
-   **Learning rate**  — How quickly the optimizers changes weights and biases. Generally a high learning rate trains faster but risks not converging, whereas a lower rate trains slower
-   **Bias/Variance —** How much the output is determined by the features. more variance often can mean overfitting, more bias can mean a bad model
-   **Regularization**  — Variety of approaches to reduce overfitting, including adding the weights to the loss function, randomly dropping layers (dropout).
-   **Epochs** — How many times you run the optimization over the training data
-   **Batch size —** How many training examples you optimize for a time
-   **Ensemble learning** — Training multiple models with different parameters to solve the same problem
-   **Numerical instability —** Many deep learning algorithms can run issues with very large or very small values due to the limits of floating point number representations in computers
-   **Gradient explosion**- A common case of numerical instability
- **Label**: The correct classification/value
- **Input**: Predictor Variables - Example: Input + Label sample to train your model
- **Model**: Mathematical function, Some work is done on inputs for an output
- **Training**: Adjusting Variable weights in a model to minimize error
- **Prediction**: Using the model to guess the label for an input - Supervised Learning: Training your model using examples data to predict future data
- **Unsupervised Learning**: Data is analyzed without labels for patterns or clusters
- **Neuron**: A way to combine inputs and weighting them to make a decision (it is one unit of input combination)
- **Gradient Descent**: The process of testing error in order to minimize its value iteratively decreases towards a minimum. (This can be global or local maximum and starting points and learning rates are important to ensure the process doesn’t stop at local minima. Too low a learning rate and your model will train slowly, too high and it may miss the minimum)
- **Hidden Layer**: A set of neurons that act on the same input data.
- **Features**: The data values/fields you choose to model, these can be transformed (x^2, y^2, etc)
- **Feature Engineering**: The process of building a set of feature combinations to act on inputs
- **Precision**: The positive predictive value how many times it correctly predicted a thing as its classification (eg cat)
- **Recall**: The true positive rate, How many times a think is in the class (the actual number of cats)
- **Sparse Vector**: Sparse vector contains only 0 and 1, whereas only one 1

</p>
</details>
