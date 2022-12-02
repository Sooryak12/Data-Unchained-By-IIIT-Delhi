# Data-Unchained-By-IIIT-Delhi
ML competiton  by Elysieum IIIT Delhi on a span of 4 days with 3 rounds on tabular data ,text ,image sequence.
#### Won Second Place in the Event.

Article on how I solved the final round problem : https://sooryaprakash84.medium.com/hands-on-practice-with-time-distributed-layers-using-tensorflow-c776a5d78e7e

## First Round 

#### Position -First Place 

#### Problem :Structural Data 
The Problem was to train a model which will decide whether a player is fit for a bidding round or not. 

##### Round 1 https://www.kaggle.com/t/93a0c57f9b384997a5cec9bd69317d79

#### Approach: 
<!-- We have analyzed the data and found that it was a biased data [Not Selected >>>>Selected] .So our main approach was to increase the predictions of Selected rather than not selected. Proper Preprocessing was done and we replaced -3,-1 with zeros and made the Region column Categorical .We got 1st in public leaderboard with a XGboost model in ensemble. Though our decision tree model didn't perform well in public leaderboard we got 0.97% accuracy in private leaderboard. 
-->

## Second Round: 

#### Position: Third Place 


## Final Round: 

#### Positon: Second Place 

#### Problem: Image Sequence
The problem is to train a model which determines the speed of the car using a series of dash-cam images (ie 8 frames). 



##### Round 3 https://www.kaggle.com/t/ef5b543a20a3406c812ce036f60105e5 

#### Approach: 
This is the toughest problem as I have not worked much on computer vision and this was an image sequence task. 
https://medium.com/smileinnovation/how-to-work-with-time-distributed-data-in-a-neural network-b8b39aa4ce00 
This article helped to learn about TimeDistributed Layers . Time Distributed layers are used to feed list of image sequence into a model. 
We resized the image to (180,320) preserving the aspect ratio and made numpy arrays in shape of (8,180,320,3) and our output had 2 values velocity in x direction and y direction . Our Model had atime distributed layer of Pretrained InceptionResnet followed by a LSTM to gather information about the sequence followed by Dense Layers.


