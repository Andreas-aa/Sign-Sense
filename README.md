# *American Sign Language Image Classification*

This project aims to develop a model for American Sign Language (ASL) recognition, enabling the prediction of letters and words from images and videos of ASL gestures.
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
  => Takes an image or video file with ASL gestures as input and outputs the predicted letter or word.


## Dataset
This dataset consists of ASL images, organized into 29 folders, each representing a distinct class. The training dataset comprises 87,000 images, each with a resolution of 200x200 pixels. The 29 classes encompass the 26 letters of the alphabet (A-Z), as well as SPACE, DELETE, and NOTHING.  

Each training and test case corresponds to a label (0-27) that maps one-to-one to an alphabetic letter (A-Z). _Please note that there are no cases for 9=J or 25=Z due to similarities in gesture motions._  

In some model iterations, the SPACE, DELETE, and NOTHING classes were removed to evaluate if the model's performance could be improved without them.  

You can download the Kaggle dataset on this link : https://www.kaggle.com/datasets/grassknoted/asl-alphabet/data

## Usage

Here's a quick look at what the API looks like:
![Live Usage of the API predicting the word LEWAGON](API_TEST.gif)
