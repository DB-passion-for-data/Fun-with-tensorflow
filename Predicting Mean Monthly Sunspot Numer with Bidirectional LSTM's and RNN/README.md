# Predicting Mean Monthly Sunspot Numer with Bidirectional LSTM's and RNN
<img src ="https://upload.wikimedia.org/wikipedia/commons/6/67/Sunspots_1302_Sep_2011_by_NASA.jpg"></img>

## Bidirectional LSTM
Bidirectional LSTMs are an extension of traditional LSTMs that can improve model performance on sequence classification problems.

In problems where all timesteps of the input sequence are available, Bidirectional LSTMs train two instead of one LSTMs on the input sequence. The first on the input sequence as-is and the second on a reversed copy of the input sequence. This can provide additional context to the network and result in faster and even fuller learning on the problem.


<img src = 'https://miro.medium.com/max/764/1*6QnPUSv_t9BY9Fv8_aLb-Q.png'></img>

## Simple RNN
Recurrent Neural Network(RNN) are a type of Neural Network where the output from previous step are fed as input to the current step. In traditional neural networks, all the inputs and outputs are independent of each other, but in cases like when it is required to predict the next word of a sentence, the previous words are required and hence there is a need to remember the previous words. Thus RNN came into existence, which solved this issue with the help of a Hidden Layer. The main and most important feature of RNN is Hidden state, which remembers some information about a sequence.
It is the first algorithm that remembers its input, due to an internal memory, which makes it perfectly suited for machine learning problems that involve sequential data


<img src = 'https://builtin.com/sites/default/files/styles/ckeditor_optimize/public/inline-images/unrolled-rnn_0.png'></img>

## Data
<a href='https://www.kaggle.com/robervalt/sunspots'> Get Data Here </a>


Sunspots are temporary phenomena on the Sun's photosphere that appear as spots darker than the surrounding areas. They are regions of reduced surface temperature caused by concentrations of magnetic field flux that inhibit convection. Sunspots usually appear in pairs of opposite magnetic polarity. Their number varies according to the approximately 11-year solar cycle.

Source: https://en.wikipedia.org/wiki/Sunspot
### Acknowledgements for data :
SIDC and Quandl.

Database from SIDC - Solar Influences Data Analysis Center - the solar physics research department of the Royal Observatory of Belgium. SIDC website

## Data Overview
![download](https://user-images.githubusercontent.com/69857637/119633362-4d9ff100-be2f-11eb-92cf-7ac6ed32bc1c.png)

Range of time in this Dataset is 1749-02-28 to 2021-01-31
Its almost 99318 days.
We also can see seasonality  in this dataset.

![download (1)](https://user-images.githubusercontent.com/69857637/119633670-9a83c780-be2f-11eb-8374-8aa0bc91e519.png)

We can also see that there are no negative values in the data. So 'Relu' wiil be a good activation function here.

## Model Summary 
![Screenshot from 2021-05-26 14-41-10](https://user-images.githubusercontent.com/69857637/119634697-9e641980-be30-11eb-8521-6b5af1c23371.png)


## Original vs Forecasted
![download (2)](https://user-images.githubusercontent.com/69857637/119634020-ef274280-be2f-11eb-8953-ac24ed6f8f65.png)

Our forecastedcurve is nicely fitting the original curve.

## Training and validation Loss
![download (3)](https://user-images.githubusercontent.com/69857637/119634423-6066f580-be30-11eb-90fd-a06b40b0d8e9.png)


## Testing the Model
![Screenshot from 2021-05-26 14-45-43](https://user-images.githubusercontent.com/69857637/119635874-ba1bef80-be31-11eb-8927-62032eae3ab4.png)


 From the official site we have the value of all the monthly Mean sunspot numbers. Lets try and predict the next mean sunspot number. The red box is the value to be predicted.
 
 Predicted value : 8.041251
 
 The original value was 8.7 and our predicted value is 8.04 ,so it can be said that model is performing well.

