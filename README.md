# Assignment 2:
The second step in this project was to create a REST API with endpoints for GET, POST, PUT, and DELETE verbs, and tests for each endpoint. As part of this assignment the app.py, test_app.py, Dockerfile.api, Dockerfile.test, run_api.sh, run_tests.sh and python-app.yml files were created.

## The Workflow:
The workflow for assignment 2 is python-app.yml and was written to be triggered when pushes or pull requests are made of the main branch and can also be run manually from the actions tab as described for the workflow in assignment 1. As with the workflow from assignment 1, this workflow will check out the code, set up python, install the dependencies and then execute the specified tests (in this case test_app.py).

## The Code:
The app.py file contains code to get, create, update, and delete items and the test_app.py file has tests to ensure that each of those functions are working as they should. Dockerfile.api containerizes app.py and run_api.sh then uses Dockerfile.api to build an image, creates and starts a container for that image and exposes that container on port 5000. Dockerfile.test and run_tests.sh function in a similar manner but for the test_app.py file. The python-app.yml workflow was designed to run the codes but if you wanted to run any of the files separate from the workflow you would simply have to clone the repo and use the terminal and the commands ./run_api.sh and run_tests.sh to execute the app.py and test_app.py files respectively.
