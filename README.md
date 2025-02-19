# deep-learning-challenge

Overview
The purpose of this analysis is to build a deep learning model that predicts the success of organizations applying for funding from a nonprofit foundation called Alphabet Soup. 

Results
•   Data Preprocessing
- Target Variable: IS_SUCCESSFUL
- Features: All other columns after encoding categorical variables.
- Removed Columns:
    EIN: A unique identifier for organizations (not useful for modeling).
	NAME: The name of the organization (not relevant for prediction).

Model Summary
•	Initial Model:
- Hidden Layers: 2
- Neurons: 80, 30
- Activation: ReLU
- Output: Sigmoid
- Accuracy: 72%

In the optimized model, the following steps were taken to increase the model's performance:
1.  The cutoff value was adjusted a few times to observe its effect on the accuracy of the model. 
2.  The number of epochs was increased and decreased to see how the model training performs.
3.  More hidden layers and neurons were added to help the model learn more complex patterns. 
4.  Different activation functions were used to optimize feature extraction.
5.  The ASK_AMT column was dropped because of the presence of too many unique values.
- Hidden Layers: 4
- Neurons: 256, 128, 64, 32
- Activation: ReLU
- Output: Sigmoid
- Accuracy: 72%

Summary of Results
 The deep learning achieved an accuracy of 72.55% after 100 epochs of training. The model used four hidden layers with varying neuron counts and ReLU activation function. Key steps in preprocessing included feature scaling, one-hot encoding of categorical variables, and grouping rare categories under "Other". Despite these optimizations, the model did not achieve above 75% accuracy target.

Key Findings:
	•	The model consistently improved during training but plateaued at 72.55% accuracy.
	•	The loss function decreased, indicating effective learning, but further improvements are needed.
	•	More complex architectures, additional epochs, and hyperparameter tuning could enhance performance.

Alternative Model for Solving the Problem:
While deep learning is effective for complex feature interactions, structured tabular data (like the charity_data.csv dataset) often benefit from traditional machine learning models such as XGBoost or Random Forest. 

XGBoost is specifically optimized for structured datasets. It handles categorical data efficiently-It can work with categorical features without requiring extensive encoding. It allows for interpretability by ranking feature importance. It has less computational cost compared to deep learning. XGBoost trains faster and requires less tuning.
	
