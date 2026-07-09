# Project Name: Precision agriculture ML vision model for efficient and effective pesticide/fertilizer application minimizing nutrient runoff and toxic ecosystem disturbances 

 Add short description of project here > This is a machine learning model using pre-existing deep learning networks (imagenet and detectnet) to classify nutrient deficiency's in specific plants (in this case, different types of gourds), whether it be Nitrogen, Potassium, or no deficiency at all. Eventually, the model will be able to understand the severity of each deficiency, will be able to detect more nutrient deficiency (such as zinc, phosphorus, etc.), and will be able to apply this algorithm to different crops rather than ashgourd, bittergourd, or snakegourd. Pesticide and herbicide applications will behave similarly, but will utilize a different model with different training data for accurate applications. 

![add image descrition here](direct image link here)

## The Algorithm

Add an explanation of the algorithm and how it works. Make sure to include details about how the code works, what it depends on, and any other relevant info. Add images or other descriptions for your project here. 

The model takes an image as an input. Mainly, it will perform best with ashgourd, bittergourd, and snakegourd because of the current limited dataset used to train the model. The model (using imagenet, a deep learning model within the jetson-inference library) outputs the picture back with its predicted class and a confidence score between 0% and 100%

## Running this project

1. Add steps for running this project.
2. Make sure to include any required libraries that need to be installed for your project to run.

[View a video explanation here](video link)
