# Deploying a Sentiment Analysis Model

## Project Overview

In this project, I have used Amazon SageMaker to complete an entire lifecycle of a machine learning project. The goal is to build a very simple web page in which a user can submit a movie review and the prediction model behind the scenes will predict whether it is Positive or Negative review. The prediction model is implemented using Pytorch framework and trainned on IMDB dataset.


## Project Instruction

This entire project is done on Amazon sagemaker and uses some heavy GPU instances for training the models. If you want execute this on local machine, you might want to train the model on subset of the training data from IMDB dataset. Also there are steps where we upload the data to amazon S3 instances in order to train using aws instances which you can totally ignore on local machines


### General Outline

- Step 1: Downloading the data
- Step 2: Preparing and Processing the data
- Step 3: Upload the data to S3
- Step 4: Build and Train the PyTorch Model
- Step 5: Testing the Model
- Step 6: Deploying the model for testing
- Step 7: Use the model for testing
- Step 6  Deploy the model for the web app
- Step 7  Use the model for the web app


### Delete the Endpoint
Remember to always __SHUT DOWN YOUR ENDPOINT__ if you are no longer using it. You are charged for the length of time that the endpoint is running so if you forget and leave it on you could end up with an unexpectedly large bill.
```
	predictor.delete_endpoint()
```
