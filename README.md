# Neural Network Charity Analysis

## Analysis Overview
The purpose of this project is to use deep-learning neural networks with the TensorFlow platform in Python, to analyze and classify the success of charitable donations.

## Results
### Data Preprocessing
- For my model only the column of IS_SUCCESSFUL was considered as a target.
- In the first model the next columns were considered as a feature APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT.
- The variables of EIN and NAME were removed because they were not considered as relevant to the model. For the second models also the columns of STATUS and SPECIAL_CONSIDERATIONS were removed.

![image](https://user-images.githubusercontent.com/96214489/169714832-ae47bd9b-4ba2-420d-8119-1b04ad013d21.png)

![image](https://user-images.githubusercontent.com/96214489/169714960-c592e486-36ab-4b67-99c3-ae08cd8e636f.png)


### Compiling, Training, and Evaluating the Model
- In the first model only a 2 layers, with 80 and 30 neurons respectively, were used in the first model, however, by seeing the count of features used to the model (37) the quantity of neurons increased to 110 in the first layer and 50 for the second layer. In the last try to optimize the model a third layer was added with the quantity of 100, 50 and 30 neurons.
- I was not able to achieve the target model performance, altough I did performance a change of features, quantity of layers and neurons, bucketing, and activation method; the accuracy didn't achieve the target of 75% and remains around 72%-73% every time.
- The first thing I did was to remove more columns that look irrelevant (STATUS and SPECIAL_CONSIDERATIONS), bucket the categories in the columns of APPLICATION_TYPE and CLASSIFICATION, increase the neurons for each layer, increase the quantity of epochs to 200, increase by one the layers and finally I tried changing the activation method to "tanh", "sigmond" and "relu".

![image](https://user-images.githubusercontent.com/96214489/169715303-e3c08536-398f-43af-8ac9-b9ecaa9e9004.png)

## Summary
By using neural networks, in machine learning, the performance of your prediciton could be pretty good or not so good, you need to try and change the model as many times as you need to achieve the expected performance. This last part could be considered as the most exhaustive of the whole code writing.
In the case of this model, perhaps going deeper in the neural network could increase the performance, or perhaps an irrelevant feature was considered. Wichever was the case, in neural networks you always need to be aware of all the variables you are using to get, not an expected result, but a prediction close to reality. 
