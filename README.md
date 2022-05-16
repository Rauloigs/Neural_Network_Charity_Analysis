# Neural_Network_Charity_Analysis

FIRST ATTEMPT CHANGES
1. Dropping SPECIAL_CONSIDERATIONS, which I don´t consider important, because there at just to options and one of the is 0.07% of the total.
2. I added another hidden layer with the activation function tanh with 10 nodes

In this image you can observe the new hidden layer added with its activation function

<img width="900" alt="firstattempt" src="https://user-images.githubusercontent.com/84519822/168655394-6079396b-5ec6-48e5-8fac-19adc5bfc065.png">

Here you can see the result of this model, which it actually drecreased the accuracy

<img width="469" alt="firstattemptaccloss" src="https://user-images.githubusercontent.com/84519822/168655578-c6dde65d-1eb2-427a-a082-638a9f8b2554.png">



SECOND ATTEMPT
1. APPLICATION_TYPE binning reduce from 9 to 6
2. Reducing the binning of CLASSIFICATION from 6 to 4
3. Dropping SPECIAL_CONSIDERATIONS, which I don´t consider important, because there are two options and one of the is 0.07% of the total.
4. Changing the activation function of the thirs hidden layer from tanh to sigmoid
5. Increasing the third layer nodes from 30 to 40.


In this image you can observe the new hidden layer added with its activation function

<img width="924" alt="secondattempt" src="https://user-images.githubusercontent.com/84519822/168657963-db49e2dd-29d6-489d-82d5-66e59e588e65.png">


Here you can see the result of this model, which it actually drecreased the accuracy


<img width="740" alt="secondattemptaccloss" src="https://user-images.githubusercontent.com/84519822/168658050-c32c604b-ac9a-4561-89f7-a8a48139beee.png">



What I decided not to do.. 

MORE BINNNING?
I didn't find it necesseraly to bin more Features due that all other features besides APPLICATION TYPE & CLASSIFICATION, had less than 10 values. Nevertheless the ASK_AMT (asked amount) has too many values and its density is concentrated in a small range. I also decided not to bin this, becuase I believe it to be one of the most important features for Alphabet Soup to take into account as a whole and there is no a tendency amount for this feature. 

