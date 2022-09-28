<!--[![tee-stark](https://circleci.com/gh/tee-stark/k8s-ml-microservices.svg?style=svg)](https://app.circleci.com/pipelines/github/Tee-Stark/k8s-ml-microservices?branch=master)-->
[![tee-stark](https://dl.circleci.com/status-badge/img/gh/tee-stark/k8s-ml-microservices/tree/main.svg?style=svg)](https://app.circleci.com/pipelines/github/Tee-Stark/k8s-ml-microservices?branch=master)

## Project Overview

In this project, I operationalize a Machine Learning Microservice API with Docker and Kubernetes. 

Given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). 
In this project, I was able to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

The project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project, I:
* Tested my project code using linting
* Completed a Dockerfile to containerize this application
* Deployed the containerized application using Docker and made a prediction
* Improved the log statements in the source code for this application
* Configured Kubernetes and created a Kubernetes cluster
* Deployed a container using Kubernetes and made a prediction
* Uploaded a complete Github repo with CircleCI to indicate that my code has been tested

<!--You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).-->

<!--**The final implementation of the project will showcase your abilities to operationalize production microservices.**-->

---

## Setup the Environment

* Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv. 
```bash
python3 -m pip install --user virtualenv
# You should have Python 3.7 available in your host. 
# Check the Python path using `which python3`
# Use a command similar to this one:
python3 -m virtualenv --python=<path-to-Python3.7> .devops
source .devops/bin/activate
```
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
