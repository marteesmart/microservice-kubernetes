[![CircleCI](https://dl.circleci.com/status-badge/img/gh/marteesmart/microservice-kubernetes/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/marteesmart/microservice-kubernetes/tree/main)


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


### Files in this repository

**1)** `app.py` - Standalone python app

**2)** `requirements.txt` - This file contains all dependencies to be installed for the standalone app

**3)** `make_prediction.sh` - Payload prediction file

**4)** `Makefile` - This file contains shell commands that can be executed using the `Make` linux tool.

**5)** `Dockerfile` - This file contains all the commands needed to assemble the app image.

**6)** `run_docker.sh` - This file contains the shell commands needed to build the image on docker locally and also run a container.

**7)** `run_kubernetes.sh` - This file contains the shell commands needed to deploy the app in a kubernetes cluster running locally.

**8)** `upload_docker.sh` - This file contains the shell commands needed to upload the docker image to docker hub.

