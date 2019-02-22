# Caption_Generator-SIMPLE-
This is a very simple and less accurate version of a caption generator trained on the Flickr8k Dataset which can be trained on a very small RAM and in a small time. The preprocessing time has also been greatly reduced. This has been created to show a very basic Caption Generator which can be easily manipulated to construct a highly accurate caption generator trained on Flickr30k or even Coco Dataset.

# FUNDAMENTALS:
To keep the model very simple and easy to train, a number of measures were taken-
1. Only one description(#1 in Flickr8k) per image was used.
2. Further, every word which only occured in only a single description was removed along with the description and the image that it occured in.
3. This filtering reduced the number of images to 6345 having one description each.
4. Further, the vocabulary was also greatly reduced which has adversely affected the accuracy of the model. 

# IMPLEMENTATIONS:
The notebooks should be executed in the order of "VGG16 Preparation", "Preparing Text Data", "FILTER", "EXTRACTOR", "TRAINER", "PREDICTOR".

# VGG16 Preparation.ipynb
In the "VGG16 Preparation", I have popped the last classification layer of Keras' VGG16 which has been later used for extracting features from images.

# Preparing Text Data.ipynb
All the descriptios from the Flickr8k.token.txt of the dataset have been written to a text file descriptions.txt after proper processing. Only the first description for each image has been used.

# FILTER.ipynb
Here we filter the descriptions and remove the ones having words occuring only once in the entire descriptions.txt. Subsequently only the corrosponding images are chosen from the entire Dataset. This is done to reduce the preprocessing and training time.

# EXTRACTOR.ipynb
Here, we extract features from all the remaining images and save them to the features.pkl

# TRAINER.ipynb
Finally, we split the remaing images onti training and test sets and train the model saving the model after every epoch.

# PREDICTOR.ipynb
Here, we predict the caption for any input image.
