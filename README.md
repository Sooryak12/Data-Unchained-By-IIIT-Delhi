# Data-Unchained-By-IIIT-Delhi
ML competiton on a span of 4 days with 3 rounds .


## First Round 

#### Position -First place 

#### Problem :Structural Data 
The Problem was to train a model which will decide whether a player is fit for a bidding round or not. 

####Approach: 
We have analyzed the data and found that it was a biased data [Not Selected >>>>Selected] .So our main approach was to increase the predictions of Selected rather than not selected. Proper Preprocessing was done and we replaced -3,-1 with zeros and made the Region column Categorical .We got 1st in public leaderboard with a XGboost model in ensemble. Though our decision tree model didn't perform well in public leaderboard we got 0.97% accuracy in private leaderboard. 

## Second Round: 

#### Position: Third Place 

#### Problem : Text Based 
The problem was to classify content of blogs to one of 12 classes describing their overall emotion .

#### Approach: 
The key point in this problem lies in the proper analysis of preprocessing of the text. First we searched for the things to process in text and found that many links,tags,numbers,exclamations were there. We lowercased the text ,decontracted and removed unnecessary stopwards ,removed links ,tags ,exclamations,numbers .Then fed it into the Bert Model .Bert took care of the rest. 

## Final Round: 

#### Positon: Second Place 

#### Problem: Image Sequence
The problem is to train a model which determines the speed of the car using a series of dash-cam images (ie 8 frames). 

#### Approach: 
This was the toughest problem as I have never worked on image field and this was an image sequence task. 
https://medium.com/smileinnovation/how-to-work-with-time-distributed-data-in-a-neural network-b8b39aa4ce00 
This article helped to learn about TimeDistributed Layers and we have used them in the model. Time Distributed layers are used to feed image sequence into a work. 
We resized the image to (180,320) preserving the aspect ratio and made numpy arrays in shape of (8,180,320,3) and our output was 2 values velocity in x direction and y direction . Our Model had atime distributed layer of Pretrained InceptionResnet followed by a LSTM to gather information about the sequence followed by Dense Layers.
