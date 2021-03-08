[![CircleCI](https://circleci.com/gh/MahinderChhapola/mlhouseprediction/tree/master.svg?style=svg)](https://circleci.com/gh/MahinderChhapola/mlhouseprediction/tree/master)

## Project Overview

This project is using the machine learning algorithms to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. It is based on Python flask, `app.py`—that serves out predictions (inference) about housing prices through API calls. It is using docker and kubernetes to containerize and scaling the application.


### How to run using Docker

First, run the below command which will create the docker image and runs app:

```
./run_docker.sh
```

Second, open a new tab on the terminal and run prediction script:

```
./make_prediction.sh
```

### How to run using Kubernetes

First, you need to run the above docker script to follow kubernetes steps.

Second, run kubernetes script:

```
./run_kubernetes.sh
```

Finally, you can run verify with prediction script:

```
./make_prediction.sh
```

### Project files structure and description

The project files consists of main python application, dockerfile, requirements and automation scripts to run the project using the one-line command.

* Application `app.py` and `model_data` to make a prediction of the houses in Boston
* `Dockerfile` contains the instructions to build and run the application
* Dependencies are documented in 'requirements.txt'
* Automation scripts `run_docker.sh`, `upload_docker.sh`, `make_prediction.sh`, `run_kubernetes.sh` and `Makefile`

