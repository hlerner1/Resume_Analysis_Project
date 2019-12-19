# Resume Analysis Project

## Introduction
This project was primarily worked on in google colab, but also some amount in jupyter notebooks. The two models as well as the randomly generated embeddings were produced in the colab file which has the name "585-project-code". If you are to open that file you will be greeted with a command to mount to a google drive. If you wish to use google drive to analyze this data, change the filepath to the drive you wish to work in. 

## Privacy Statement
We used real resumes from a recent hackathon at our school. These resumes were given to us with the assumption that we will anonymize the data to the best of our ability and keep the main files private. Unfortunately this means that our annotated data is not viewable on GitHub.
## Setting up
  ### Changing important filepaths
- The ls check of file path
- mypath
  - same path as the ls file path
- glove_file
  - the file path to a 50-dimensional glove embedding file
- the temp variable
  - to gather the labeled data

### Necessary Packages
  - PyPDF2
  - textract
  - nltk
  - allennlp

## Instructions

### Main Models File
Both the 585-project-code as well as the Naive Bayes classifier code are designed to be able to be run by the user. They take a decent chunk of time to set up, but once set up, they can be used fairly freely. Most of the scripts are to set up the raw data for processing. To make modifications on the parameters, you will need to find the GridSearchCV calls further down in the code. The first three classifiers you see will be:
- Gradient Boost Classifier
- Random Forest Classifier
- Multilayer Perceptron Model Classifier
Use the parameters dictionaries to declare your special parameters for the problem.

After you are finished with the GloVe embedding data, you can move on to ELMo! This part of the code starts out with a set of installations and imports to prepare the AllenNLP library's ELMo model to run. Here again we need to process the data. This part can be more or less ignored unless you want to change how you work with the ELMo vector output. Currently the implementation is set to take the mean of the output vector until it is the shape (1024,). This is usually not desirable for successful implementations of the model, but due to issues talked about in our paper we ended up using this method for our implementation. Similarly to the GloVe embeddings, you can tune the hyperparameters in the same fashion for ELMo.

### Naive Bayes Classifier File
This file functions very similarly to the main file. The primary differences make no change for use for the user. This file is much less interactive than the main file. If you load this in, change the correct file paths, and click run all, you should be given a Naive Bayes classifier analysis of the input data.
