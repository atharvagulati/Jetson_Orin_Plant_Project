# Precision agriculture ML vision model for efficient and effective pesticide/fertilizer spreading minimizing nutrient runoff and toxic ecosystem disturbances 

 This is a machine learning model using pre-existing deep learning networks (imagenet and detectnet) to classify nutrient deficiency's in specific plants (in this case, different types of gourds), whether it be Nitrogen, Potassium, or no deficiency at all. Eventually, the model will be able to understand the severity of each deficiency, will be able to detect more nutrient deficiency (such as zinc, phosphorus, etc.), and will be able to apply this algorithm to different crops rather than ashgourd, bittergourd, or snakegourd. Pesticide and herbicide applications will behave similarly, but will utilize a different model with different training data for accurate applications. 

![A sample leaf used in the dataset](<Screenshot 2026-07-09 141740.png>)

## The Algorithm

The model is trained on a large dataset of images using the resnet18 neural network. There are 9 different classes comparing nutrient deficiencies and species of plants. It then uses imagenet (a deep learning network inside of the jetson-inference library) to classify a test image input as a part of one of these nine classes. The model then outputs the image back with a score from 0-100 based on how confident the model is on the image being in a certain class.

## Running this project

This project relies on the public library, jetson-inference and uses the jetson orin nano. First, navigate to jetson-inference/python/training/classification/data, and add the dataset (nutrient_plant_dataset). Navigate outside of data into models and add the model (nutrient_plant). Then, perform the following steps in the terminal as the video suggests:
1. cd jetson-inference/python/training/classification
2. NET=models/nutrient_plant
3. DATASET=data/nutrient_plant_dataset
4. imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/("test image location") ("output image")

https://drive.google.com/file/d/1KUVA6s4kjKlADqLddn60MoZxnY_gnsVo/view?usp=sharing 
