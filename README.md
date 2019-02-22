# Caption_Generator-SIMPLE-
This is a very simple and less accurate version of a caption generator trained on the Flickr8k Dataset which can be trained on a very small RAM and in a small time. The preprocessing time has also been greatly reduced. This has been created to show a very basic Caption Generator which can be easily manipulated to construct a highly accurate caption generator trained on Flickr30k or even Coco Dataset.

FUNDAMENTALS:
To keep the model very simple and easy to train, a number of measures were taken-
=> Only one description(#1 in Flickr8k) per image was used.
=> Further, every word which only occured in only a single description was removed along with the description and the image that it occured in.
=> This filtering reduced the number of images to 6345 having one description each.
=> Further, the vocabulary was also greatly reduced which has adversely affected the accuracy of the model. 
