## Food_not_Food_web_application
Machine Learning Powered App to decide whether a photo is food or not 
See it working live at: https://foodnotfood.vercel.app/

##Log
2022/10/12
* Downloaded ImageNet class list from GitHub (Want to get non-food classes from ImageNet)
* Downloaded and installed NLTK (to try and get a list of word associated with food)
* Got list of food using NLTK, filter imagenet dataset classes
* For images of food: random subset of images from Food101 and ImageNet (photos that are food)
* Got list of food classes and non-food classes
* Figure out how to download images from ImageNet(Random samples)
* Create food image dataset from Food101

2022/10/14
* Updated list of ImageNet food and non-food items to include ImageNet keys from
* -> https://github.com/mf1024/ImageNet-Datasets-Downloader


2022/10/15
* Started to downloading images from ImageNet. Filter these images on the backend into food_images and non_food_images
* Downloading 50 random images from 1000 random classes
* Then:filter 1000 random classes and images into food/not_food
* Split the data into training and test sets.

This creates a training and test split of `food` and `not_food` images.
This is so we can verify the performance of our model before deploying it.
It'll create such structure:

```
train/
    food/
        image1.jpeg
        image2.jpeg
        ...
    not_food/
        image100.jpeg
        image101.jpeg
        ...
test/
    food/
        image201.jpeg
        image202.jpeg
        ...
    not_food/
        image301.jpeg
        image302.jpeg
        ...
```

2022/10/16
* Trained first test model using EfficientNetB0
* Save the model as efficientnetB0.tflite.

2022/10/17
* Improved model by using more train/test data
* Deployed website from vercel.com
* The latest model is food_not_food_v3.tflite

## What data is used?

The current deployed model uses about 40,000 images of food and 25,000 images of not food.

* Food images come from the [Food101 dataset](https://data.vision.ee.ethz.ch/cvl/datasets_extra/food-101/).
* Not food and *some* food images come from [Open Images](https://storage.googleapis.com/openimages/web/index.html).
