**HEART ATTACK PREDICTION**

**Introduction**

The project’s goal was to create a unique neural network model that would use the given dataset
to forecast the likelihood of a heart attack. The dataset includes a number of features pertaining
to cardiovascular risk factors and health conditions.

**Data preprocessing and exploration**

The dataset was loaded into pandas’ data frame.
For missing values ,the mean of the corresponding columns was used in their place.
The dataset was purged of duplicate entries , where found.
To obtain a better understanding of data basic statistics from dataset were analyzed.

**Extensive Feature Extraction**

For the project, considerable feature extraction was carried out using Principal component
Analysis(PCA).The PCA approach reduces dimensionality and preserves variance while
identifying significant features. The initial characteristics were changes into a collection of
principle components, which are uncorrelated variables. Utilized as input for the customized
neural network model, these elements revealed underlying patterns in the data. In the end, PCA
enhanced the model’s performance in identifying people who are at risk of heart attack by
streamlining the model’s input space and strengthening its generalization skill.

**Custom Feature Selection**

A custom feature selection algorithm was designed to select the most relevant features based on
their correlation with the target variable. The custom feature selection function calculates tg
correlation between each feature and the target variable y. The highest absolute correlation values
among the top {k} characteristics are chosen. The original feature matrix{X} is subset using
these chosen feature{X selected}. By using a correlation analysis to determine which aspects are
most important to target the variable, this technique makes sure that only those features are kept
for additional research or modeling.

**Feature Visualization**

A heatmap illustrating the correlation matrix between characteristics in ‘X’ and the target
variable ‘y’ is produced by function ‘plot_feature_importance’ .It facilitates the visualization of
the role that features play in target prediction. To see their correlation matrix a function
‘plot_correaltion_matrix’ in invoked using the ‘X_selected’ that have been chosen.

**Neural network Model**

• Sequential API of TensorFlow was used to create a neural network model with bespoke
architecture.

• Sigmoid activation functions were used in five hidden layers of the model.
• Using a random normal initializer, the models’ weights were initialized in a bespoke
manner.

• By using binary cross_entropy as the loss function ,The Adam optimizer was employed .

• The addition of dropout layers prevented the overfitting.

**Model Training and Evaluation**

The dataset was split into train and test datasets. Features were scaled using StandardScaler to
ensure uniformity. To improve its parameters and minimize the loss function, the model was
trained using the training data. The weighs and biases of the model were repeatedly adjusted
across several epochs in this procedure. To track effectiveness and avoid overfitting , validation
data were employed .Lastly , an accuracy assessment if the model was conducted using the test
data. The training history was visualized to monitor the model’s training and validation accuracy
over epochs.

**Results**

The testing results showed that the custom neural network model could accurately forecast the
likelihood of a heart attack with an accuracy of approximate 86%.The efficacy of the model was
enhanced by the feature selection method ,which assisted in determining the most pertinent
characteristics for heart attack prediction. The model’s learning process was illustrated by the
training history plot ,which also showed strong convergence .

![image](https://github.com/user-attachments/assets/13bd89af-244a-4c4f-b871-5d1c6aa12552)

