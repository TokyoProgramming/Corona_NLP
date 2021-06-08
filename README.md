# RNN_LSTM: COVID-19 Twitter text data 


## Table of contents

- [About the project](#About_the_project)
- [Technologies](#technologies)
- [Code Examples](#CodeExamples)
- [License](#License)
- [Reference](#Reference)

## About the project

This project will use Kaggle data which is about corona virus text on twitter. As you can check the data strucutre below, the data are twitter text and label (Extremely Negative, Negative, Neutral, Positive, Extremely Positive).  <br />
Let's see the example of this project ( this will easy to get the purpose of the project). <br />

```
classifier.predict('I hate corona virus')
```

```
# result 
('Extremely Negative', tensor(0) 
tensor([9.9935e-01, 9.4686e-09, 6.4548e-04, 5.4781e-08, 1.1805e-07]))
```

```
classifier.predict('Our life style has been changed a lot due to the covid-19')
```

```
# result
('Neutral', tensor(3), tensor([0.0082, 0.0067, 0.0128, 0.9482, 0.0240]))
```


Those results seems correct !! <br />
The model will classify the text which is relative to Covid-19.





- **data strucutre** <br/>

Twitter text data with label <br />
- total data = 41157
- train data = 28809
- test  data = 12348

<div align="center">

<table>
  


||  OriginalTweet  |  Sentiment  |
|----| ---- | ---- |
|0|  @MeNyrbie @Phil_Gahan @Chrisitv https://t.co/iFz9FAn2Pa and https://t.co/xX6ghGFzCC and https://t.co/I2NlzdxNo8 |  Neutral  | 
|2| advice Talk to your neighbours family to exchange phone numbers create contact list with phone numbers of neighbours schools employer chemist GP set up online shopping accounts if poss adequate supplies of regular meds but not over order  |  Positive  |
|3|  Coronavirus Australia: Woolworths to give elderly, disabled dedicated shopping hours amid COVID-19 outbreak https://t.co/bInCA9Vp8P |  Positive  | 
|...|  ...  |  ...  | 
|41157|  Me, ready to go at supermarket during the #COVID19 outbreak.\r\r\n\r\r\nNot because I'm paranoid, but because my food stock is litteraly empty. The #coronavirus is a serious thing, but please, don't panic. It causes shortage...\r\r\n\r\r\n#CoronavirusFrance #restezchezvous #StayAtHome #confinement https://t.co/usmuaLq72n  |  Extemely Negative  |
</table>

</div>
  

## Technologies

Project is created with:

- Python 3.8.4
- RNN_LSTM
- pytorch
- fastai 

## Project table

- #### set up firstai
- #### cleaning data
    - ###### convert & to and 
    - ###### Remove Unicode Characters 
    - ###### how to deal with #texts

- #### traiing the model

## result 78.9% accuracy
 - confusion_matrix
   
    |                     | Extremely Negative  |  Negative | Neutral | Positive |  Extremely Positive | 
    | :------------ |:---------------:| -----:|:------------ |:---------------:| -----:|
    | Extrememly  Negative | 1068 | 470  | 8    | 25   | 1   |
    | Negative             | 206  | 2343 | 134  | 312  | 10  |
    | Neutral              | 3    |  121 | 1992 | 171  | 5   |
    | Positive             | 5    |  240 | 202  | 2792 | 251 |
    | Extremely Positive   | 1    |  12  | 10   | 422  | 1544|

## Reference

