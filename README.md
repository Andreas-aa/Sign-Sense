# *American Sign Language Image Classification*

This project aims to develop a model for American Sign Language (ASL) recognition, enabling the prediction of letters and words from images and videos of ASL gestures. The system utilizes various techniques including convolutional neural networks (CNNs), transfer learning, data augmentation, and landmark detection for accurate recognition of ASL gestures.

## Project Description

Sign language is an essential means of communication for people who are deaf or hard of hearing. However, there is a communication barrier between people who use sign language and those who do not. This project aims to reduce this barrier by developing a model that can recognize ASL signs and translate them into English.

The project uses a labeled dataset of ASL images to train an image classification model. The model is based on a Convolutional Neural Network (CNN) and is trained using the TensorFlow library.

## Features

- Use of a Convolutional Neural Network (CNN) for classification
- Transfer Learning (YOLOv8)
- Training of the model on a labeled dataset
- Evaluation of the model on a test dataset
- Streamlit API
- CV2/MediaPipe

## Installation

To install the project, you need to clone this GitHub repository and install the required dependencies.  
- The dependencies are listed in the `requirements.txt` file. You can install the dependencies using pip:
`pip install -r requirements.txt`

- Launch the FastAPI: `uvicorn package_folder.api_file:app --reload`

- Prediction endpoint of the API:
      `/predict`
  => Accepts an image or video file containing ASL gestures and returns the predicted letter or word.


## Dataset
The data set is a collection of images of alphabets from the American Sign Language, separated in 29 folders which represent the various classes.   

The training data set contains 87,000 images which are 200x200 pixels. There are 29 classes, of which 26 are for the letters A-Z and 3 classes for SPACE, DELETE and NOTHING.   

Each training and test case represents a label (0-27) as a one-to-one map for each alphabetic letter A-Z (and no cases for 9=J or 25=Z because of gesture motions).   

For some modeles 3 classes for SPACE, DELETE and NOTHING were removed to check if the model can work better.

You can download the Kaggle dataset on this link : https://www.kaggle.com/datasets/grassknoted/asl-alphabet/data

## Usage

The project's API was deployed on the cloud in March 2024 and is not currently available for use. Here's a quick look at what it looked like :
![Live Usage of the API predicting the word LEWAGON](API_TEST.gif)
