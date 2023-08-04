# -N100-stock-model
Third PyTorch project, getting used to the syntax and wordings

## How does it work?
You'll have to have the information for the opening, closing, high, low, and adjusted closing prices
for the past 7 days. There is an example at the end where the model is trained where I use the
test dataset to see how accurate the results are. You can input your information like that.
This is ONLY for the ^N100 stock

## How did you create it?
I used the kaggle dataset with Global Markets Data across 2008-2023. Here's the dataset: 
https://www.kaggle.com/datasets/pavankrishnanarne/global-stock-market-2008-present 
I used an LSTM cell with 16 layers and 64 neurons, as well as batch normalization
between the Linear layers so that gradients were more effective since that was a problem
I noticed during training. Dropout layers are included to reduce overfitting. I used a sliding window
technique to encapsulate my data, using a window of 7 instances.
