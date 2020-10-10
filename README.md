# Gesture-Recognition-Smart-Tv

To develop a cool feature in the smart-TV that can recognise five different gestures performed by the user which will help users control the TV without using a remote. 

The gestures are continuously monitored by the webcam mounted on the TV.

## Each gesture corresponds to a specific command:

Thumbs up:  Increase the volume
Thumbs down: Decrease the volume
Left swipe: 'Jump' backwards 10 seconds
Right swipe: 'Jump' forward 10 seconds  
Stop: Pause the movie

## Understanding the Dataset: 

The training data consists of a few hundred videos categorised into one of the five classes. Each video (typically 2-3 seconds long) is divided into a sequence of 30 frames(images). These videos have been recorded by various people performing one of the five gestures in front of a webcam - similar to what the smart TV will use. 

## Solution / Approach Used: 

Two Architectures: 3D Convs and CNN-RNN Stack:

1. CNN + RNN Stack architecture :  One is the standard CNN + RNN architecture in which you pass the images of a video through a CNN which extracts a feature vector for each image, and then pass the sequence of these feature vectors through an RNN. 

2. 3D Convs : The other popular architecture used to process videos is a natural extension of CNNs - a 3D convolutional network. 

## Key Note

There are a few key things to note about the conv-RNN architecture:

You can use transfer learning in the 2D CNN layer rather than training your own CNN 
GRU can be a better choice than an LSTM since it has lesser number of gates (and thus parameters).
