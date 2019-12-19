# Resume Analysis Project

## Introduction
This project was primarily worked on in google colab, but also some amount in jupyter notebooks. The two models as well as the randomly generated embeddings were produced in the colab file which has the name "585-project-code". If you are to open that file you will be greeted with a command to mount to a google drive. If you wish to use google drive to analyze this data, change the filepath to the drive you wish to work in. 

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

Both the 585-project-code as well as the Naive Bayes classifier code are designed to be able to be run by the user. They take a decent chunk of time to set up, but once set up, they can be used fairly freely. Most of the scripts are to set up the raw data for processing. To make modifications on the parameters, you will need to find the GridSearchCV calls further down in the code. The first three classifiers you see will be:
- Gradient Boost Classifier
- Random Forest Classifier
- Multilayer Perceptron Model Classifier
