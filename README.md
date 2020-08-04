# coin_detector

## Introduction

As a continuation of learning about machine learning, I created another custom detector that can detect US coins. I was brainstorming for a project that I could work on after my [street detection](https://github.com/holyjen123/object_detection.git) when I came up with the idea that it would be cool to make a detection model that can identify the different coins and add up the value. At my house, I have a pineapple coin bank that holds a large amount of coins that I can’t count up unless I dedicate some time into it. I figured using what I learned so far to create a project that I can use daily would be a great idea. 

## Object

In order to create a model that can detect different US coins, I needed to distinguish 4 classes: penny, dime, quarter, and nickel. I also made sure to make my model detect only the face of the coin because there would be too many possibilities for the tail side. I thought this would help make the prediction confidence be higher. 
Unlike my previous model, I made sure to feed my model a much larger quantity of images and train it much longer. This time, I used about 130 images for each class, totaling up to about 520. This was easily done by using this [extension](https://download-all-images.mobilefirst.me/). My final model held an index of 2217. 

## Conclusion
