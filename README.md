Food_not_Food
Machine Learning Powered App to decide whether a photo is food or not 

Log
* 2022/10/12
* Downloaded ImageNet class list from GitHub (Want to get non-food classes from ImageNet)
* Downloaded and installed NLTK (to try and get a list of word associated with food)
* Got list of food using NLTK, filter imagenet dataset classes
* For images of food: random subset of images from Food101 and ImageNet (photos that are food)
* Got list of food classes and non-food classes
* Figure out how to download images from ImageNet(Random samples)
* Create food image dataset from Food101

* 2022/10/14
* Updated list of ImageNet food and non-food items to include ImageNet keys from
* -> https://github.com/mf1024/ImageNet-Datasets-Downloader


* 2022/10/15
* Started to downloading images from ImageNet. Filter these images on the backend into food_images and non_food_images
* Downloading 50 random images from 1000 random classes
* Then:filter 1000 random classes and images into food/not_food

* 2022/10/16
* Trained first test model using EfficientNetB0
