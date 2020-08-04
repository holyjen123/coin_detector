# coin_detector

## Introduction

As a continuation of learning about machine learning, I created another custom detector that can detect US coins. I was brainstorming for a project that I could work on after my [street detection](https://github.com/holyjen123/object_detection.git) when I came up with the idea that it would be cool to make a detection model that can identify the different coins and add up the value. At my house, I have a pineapple coin bank that holds a large amount of coins that I can’t count up unless I dedicate some time into it. I figured using what I learned so far to create a project that I can use daily would be a great idea. 

## Object

In order to create a model that can detect different US coins, I needed to distinguish 4 classes: penny, dime, quarter, and nickel. I also made sure to make my model detect only the face of the coin because there would be too many possibilities for the tail side. I thought this would help make the prediction confidence be higher. 
Unlike my previous model, I made sure to feed my model a much larger quantity of images and train it much longer. This time, I used about 130 images for each class, totaling up to about 520. This was easily done by using this [extension](https://download-all-images.mobilefirst.me/). My final model held an index of 2217. 

## Conclusion

<img src="https://github.com/holyjen123/coin_detector/blob/master/readme_images/penny.png" alt="penny" width="200" height="175">
<img src="https://github.com/holyjen123/coin_detector/blob/master/readme_images/quarter.png" alt="quarter" width="300" height="275">
*first picture detected penny with a threshold of 0.52 
<br>
*second picture detected nickel with a threshold of 0.14
<br>
<br>
The first test, I got pretty good results. However, the second test shows a very poor threshold. The model also shows that it detected a wrong coin. 

## Problems

There are several possible reasons as to why the model didn’t work out quite well. One is the word difference. On each coin, there are words surrounding the face. These words all differ in every coin, which means that a penny will likely differ from another penny because of what is written on it. Furthermore, the coin’s year varies widely. So this could have been the problem for the model, but I am not 100% sure. 
Another problem could have been the images itself. Since I used an extension to easily gather hundreds of images, many of them might not have been the best choice. For example, a lot of the training images that I used all had a white background. Looking at the results, the coin with the white image was detected far more accurate than the coin with a noisy background. 
My model could have also been affected by the fact that I didn’t downgrade the resolution when I was labeling. Changing the resolution of an image helps speed up the training process. For my training images, I didn’t change the resolution because there were about 500 images and it would have taken too much. However, that could have affected the way the images were processed. I doubt this is the actual case, but I am still taking into consideration that this could have been a problem. 

## What's Next

Although this model has a lot of flaws and isn’t the most suitable to work with, I do want to keep continuing. I would create an API for this model so that I can apply it to other applications, such as an app. That would also be the next thing on the list. To make this model practical, it would be nice to create an app that users can easily work with. 
