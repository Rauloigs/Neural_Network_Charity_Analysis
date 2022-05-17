# Neural_Network_Charity_Analysis


## Overview 
Using machine learning and neural networks I designed a binary classifier that can make predictions, wheter a campaign of an organization funded by Alphabet soup will be succesful. 

I designed this with the features provided in the datset found in the resources folder of this repository.The dataset is a CSV that contains more than 34,000 organizations that have received funding from Alphabet Soup. 

## Results: 

### Data Preprocessing

- What variable(s) are considered the target(s) for your model? 

As it can be seen in the features: **IS_SUCCESSFUL** feauture was selected as my target. this feauture implies: *Was the money used effectively?*


- What variable(s) are considered to be the features for your model?

You can see here the list with the original description of my source. And this was also the list for my third and last attempt of optimizing my model:

1. APPLICATION_TYPE—Alphabet Soup application type
2. AFFILIATION—Affiliated sector of industry
4. CLASSIFICATION—Government organization classification
5. USE_CASE—Use case for funding
6. ORGANIZATION—Organization type
7. STATUS—Active status
8. INCOME_AMT—Income classification
10. ASK_AMT—Funding amount requested
11. IS_SUCCESSFUL—Was the money used effectively


- What variable(s) are neither targets nor features, and should be removed from the input data?


### Compiling, Training, and Evaluating the Model

- How many neurons, layers, and activation functions did you select for your neural network model, and why?

As you can see in the image below it was 80 neurons for the first layer, 40 for the second, 2 for the third, with the following activation functions respectively relu, relu, relu. For the output layer I used the sigmoid activation function.

<img width="892" alt="thirdattempt" src="https://user-images.githubusercontent.com/84519822/168829794-f847cd6e-2453-4098-bb04-d2a9db4550b8.png">


I chose this neurons, because it was were I found the model to be more stable after my test with my first and second attempt. What I mean with more stable it is that since the beggining I noticed (while the model was training) the accuracy was "high", almost all time close to the final accuracy, instead the first two attempts started quite low and from there they were increasing and stucked at 50 epochs out of a 100.

- Were you able to achieve the target model performance?
No. In the following question an aswers you will discover the steps and realize how close or far it was to achive that 75% of accuracy.


- What steps did you take to try and increase model performance?

For this this answer I want to adress my first two attemps with a brief description: 

**FIRST ATTEMPT**
1. Dropping SPECIAL_CONSIDERATIONS, which I don´t consider important, because there at just to options and one of the is 0.07% of the total.
2. I added another hidden layer with the activation function tanh with 10 nodes

In this image you can observe the new hidden layer added with its activation function

<img width="900" alt="firstattempt" src="https://user-images.githubusercontent.com/84519822/168655394-6079396b-5ec6-48e5-8fac-19adc5bfc065.png">


Here you can see the result of this model, which it actually drecreased the accuracy

<img width="469" alt="firstattemptaccloss" src="https://user-images.githubusercontent.com/84519822/168655578-c6dde65d-1eb2-427a-a082-638a9f8b2554.png">


**After this attempt I asked my self?... More binning?**
I didn't find it necesseraly to bin more Features due that all other features besides APPLICATION TYPE & CLASSIFICATION, had less than 10 values. Nevertheless the ASK_AMT (asked amount) has too many values and its density is concentrated in a small range. I also decided not to bin this, becuase I believe it to be one of the most important features for Alphabet Soup to take into account as a whole and there is no a tendency amount for this feature. 


**SECOND ATTEMPT**
1. APPLICATION_TYPE binning reduce from 9 to 6
2. Reducing the binning of CLASSIFICATION from 6 to 4
3. Dropping SPECIAL_CONSIDERATIONS, which I don´t consider important, because there are two options and one of the is 0.07% of the total.
4. Changing the activation function of the third hidden layer from tanh to sigmoid
5. Increasing the third layer nodes from 30 to 40.


In this image you can observe the new hidden layer added with its activation function

<img width="924" alt="secondattempt" src="https://user-images.githubusercontent.com/84519822/168657963-db49e2dd-29d6-489d-82d5-66e59e588e65.png">


Here you can see the result of this model, which it actually drecreased the accuracy

<img width="740" alt="secondattemptaccloss" src="https://user-images.githubusercontent.com/84519822/168658050-c32c604b-ac9a-4561-89f7-a8a48139beee.png">


**THIRD ATTEMPT**
1. APPLICATION_TYPE binning increased from 9 to 11
2. Increasing the binning of CLASSIFICATION from 6 to 8
3. Setting the neurons from the third layer to 2.
4. third layer activation function: relu

You can go over the images in the follwing section were the results will be sumarized. 


## Summary: 
Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.

I realized the 
