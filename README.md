# 🥷🏼 Ninjacart Image Classification 🥷🏼

### ℹ️ About Ninjacart
Ninjacart is India's largest fresh produce supply chain company. They are pioneers in solving one of the toughest supply chain problems of the world by leveraging innovative technology. They source fresh produce from farmers and deliver them to businesses within 12 hours. An integral component of their automation process is the development of robust classifiers which can distinguish between images of different types of vegetables, while also correctly labeling images that do not contain any one type of vegetable as noise.

### ❓ Problem statement
As a starting point, ninjacart has provided us with a dataset scraped from the web which contains train and test folders, each having 4 sub-folders with images of onions, potatoes, tomatoes and some market scenes. We have been tasked with preparing a multiclass classifier for identifying these vegetables. The dataset provided has all the required images to achieve the task.

### 🥅 Objective
The objective is to develop a program that can recognize the vegetable item(s) in a photo and identify them for the user.

### 📀 Data
This dataset contains images of the following food items: noise-Indian market and images of vegetables- onion, potato and tomato.<br>
Source: [Scaler DSML](https://www.scaler.com/courses/machine-learning-course-training/?utm_source=ads&utm_medium=googlesearch&utm_campaign=perf_scaler_academy_ads_googlesearch_brand-product-search_india&utm_content=data-science&utm_term=scaler%20dsml&param1=540845121596&param2=c&param3=&gad_source=1&gclid=CjwKCAjw5v2wBhBrEiwAXDDoJZlgk-Jn1LmTvHKniVl9QytGa1wTBDJGyPCjp1BCwfX3Kl1-eCkZbRoCKdwQAvD_BwE)

The train data contains the following number of images<br>
Tomato : 789<br>
Potato : 898<br>
Onion : 849<br>
Indian market : 599<br>

The train data contains the following number of images<br>
Tomato : 106<br>
potato : 83<br>
onion : 81<br>
Indian market : 81<br>

---
## Brief workflow

- In this project, we start by splitting the training data into training and validation data (since validation data is not explicitely present), followed by exploratory data analysis to understand more about the images we are working with.<br>
- Post this we start the pre-modelling process by building some utility functions to evaluate the performance of our model, building data pipelines and hyperparameter tuning pipeline.<br>
- In the modelling phase, we tried various architectures of CNN including Custom CNN from scratch (both with low and high complexity), pretrained models like VGG-16, Resnet-50 and MobileNetV3Small which were fine-tune by training the fully connected layers, with proper callbacks in place.<br>
- All the models were hyperparamater tuned using [Optuna](https://optuna.org/), in addition to deriving the hyperparameter importance. The best model was compared for each instance. <br>
- Hyperparameters: batch size, dropout rate, regularization type, regularization alpha and image augmentation.<br>

The best performing model was fine-tuned VGG-16 with train accuracy = 98.12%, val accuracy = 95.85%, test accuracy = 90.88%, train loss = 0.052, val loss = 0.171, test loss = 0.21.<br>

The observations from each section is written as markdown text in the notebook. Please visit the notebook for more details.<br>
