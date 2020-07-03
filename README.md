[![CircleCI](https://circleci.com/gh/tresvitae/ml-microservice-kubernetes.svg?style=svg&circle-token=fbf947a60cfc627c903c7b7e6e2e2f0dee21ba32)](<LINK>)



## Project Overview

This project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

Project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. The project contains:
* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

---

## Setup the Environment 

1. `python3 -m venv ~/.devops`
2. `source ~/.devops/bin/activate`
3. Install hadolint: https://github.com/hadolint/hadolint
4. Run `make install` to install the necessary dependencies (pylint!)
5. `make lint`
6. `./run_docker.sh`
7. (bash) run `python app.py`
8. (new terminal) `./make_prediction.sh`
9. `/.upload_docker.sh`

### VM & Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
1. ` sudo apt install virtualbox virtualbox-ext-pack`
2. `minikube start --vm-driver=virtualbox --memory 4096` 
3. check status of k8n `kubectl config view`
4. `./run_kubernetes.sh`