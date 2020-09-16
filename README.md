[![CircleCi](https://circleci.com/gh/vdjeudjam/project-ml-microservice-kubernetes.svg?style=svg)](https://app.circleci.com/pipelines/github/vdjeudjam/project-ml-microservice-kubernetes)
 
 ## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

### Description of Project Files
* /.circleci/config.yml - circleCi configuration file to set up Continous Integration
* /model_data - The model data for Boston Housing Price Prediction
* /output_txt_files - Predictions output logs for Docker and Kubernetes  
* Dockerfile - Docker image build configuration 
* Makefile - Environment setup, installm, lint and test Commands configuration 
* app.py - Python Flask App for Boston Housing prices predictions about through API calls
* make_prediction.sh - Make predictions based on input values for Boston Housing Price Prediction
* requirements.txt - List of required packages 
* run_docker.sh - Docker build configuration file 
* run_kubernetes.sh : Kubernetes Cluster deployment file based on docker image 
* upload_docker.sh : Docker image push configuration file
 
 ---

## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
