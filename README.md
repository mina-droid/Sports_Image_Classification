# Sports_Image_Classification Model

## Competition link (You must use this link to be able to join the competition): https://www.kaggle.com/t/f3e7c2ff1eff448c94b0f7753ddff60d

## Description:
In today’s world of internet, a massive amount of data is getting generated every day and content-based classification of images is becoming an essential aspect for efficient retrieval of images and have attracted application in several fields and one of such field is sports. Building a model that is able to classify different sports activities into different categories could be useful for automated sports analysis tasks.

## Evaluation
The evaluation metric for this competition is Categorical Accuracy

## Submission Format
The submission file should be a .csv file which contains two columns: image_name,label. The image_name is the imagename.jpg, the label is the predicted class and should be one of the following values: 0,1,2,3,4,5

Where Basketball --> 0 Football-->1 Rowing-->2 Swimming-->3 Tennis-->4 Yoga-->5
The submission should contain exactly 688 lines (for the 688 images in the test set). The image names don't have to be in a particular order but each image in the test set must have exactly one row in your submission file. The file should contain a header and have the following format:

image_name,label
0.jpg,4

1.jpg,0

## Dataset Description
The full dataset can be found in this link: https://drive.google.com/file/d/1s07aL-7nvhO8ESJy_uTCZJMF5lw5LAGK/view?usp=share_link

The dataset is also uploaded to this Kaggle competition and can be used directly in Kaggle notebooks [Make sure the notebooks are private until the competition ends]

This folder consists of two main subfolders:

Train : contains 1681 images. The label is in the image name. Image format is a mix between .png and jpg

Test: 688 images without labels all jpg

## Report
Note: training accuracy always between 98%– 100%, in all models our goal was to solve overfitting.
Trial 1: CNN Model
At first, we tried to implement the architecture found in LAB 7 in many ways as of changing the hyperparameters (filter size, number of filters, stride size, activation functions) as well as the number of layers (fully connected, convolution, maximum pooling), also adding regularization methods to prevent overfitting (batch normalization, dropout)

