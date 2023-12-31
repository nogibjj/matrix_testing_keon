# Mini Project 4

This weeks project is to take advantage of running different versions on Python through our GitHub Work flow to ensure different versions can be run virtually regardless of the version of Python code given on 5 versions of [Python](https://github.com/nogibjj/matrix_testing_keon/actions/runs/6254962670)

## Previewing different Python Build Versions

These build badges represent different versions on Python being run on `Ubuntu` and `Windows` which all passed the builds in the Github Actions

* [![ubuntu Python 3.7](https://github.com/nogibjj/matrix_testing_keon/actions/workflows/cicd.yml/badge.svg)](https://github.com/nogibjj/matrix_testing_keon/actions/workflows/cicd.yml) - Python 3.7 Build ubuntu

* [![CI](https://github.com/nogibjj/matrix_testing_keon/actions/workflows/cicd.yml/badge.svg)](https://github.com/nogibjj/matrix_testing_keon/actions/workflows/cicd.yml)  - Python 3.7 Build Windows

* [![CI](https://github.com/nogibjj/matrix_testing_keon/actions/workflows/cicd.yml/badge.svg)](https://github.com/nogibjj/matrix_testing_keon/actions/workflows/cicd.yml) - Python 3.8 Build Ubuntu

* [![CI](https://github.com/nogibjj/matrix_testing_keon/actions/workflows/cicd.yml/badge.svg)](https://github.com/nogibjj/matrix_testing_keon/actions/workflows/cicd.yml) - Python 3.8 Build Windows

* [![CI](https://github.com/nogibjj/matrix_testing_keon/actions/workflows/cicd.yml/badge.svg)](https://github.com/nogibjj/matrix_testing_keon/actions/workflows/cicd.yml) - Python 3.9 Build Ubuntu

* [![CI](https://github.com/nogibjj/matrix_testing_keon/actions/workflows/cicd.yml/badge.svg)](https://github.com/nogibjj/matrix_testing_keon/actions/workflows/cicd.yml) - Python 3.9 Build Windows

# Automation 



## 1. devcontainer

The .devcontainer folder mainly contains two files -

* Dockerfile defines the environment variables - essentially it ensures that all collaborators using the repository are working on the same environment to avoid conflicts and version mismatch issues
* devcontainer.json is a json file that specifies the environment variables including the installed extensions in the virtual environment

## 2. Makefile

The Makefile contains instructions for installing packages (specified in requirements.txt), formatting the code (using black formatting), testing the code (running all the sample python code files starting with the term 'Check...' ), and linting the code using pylint


## 3. GitHub Actions
  
Github Actions uses the main.yml file to call the functions defined in the Makefile based on triggers such as push or pull. Currently, every time a change is pushed onto the repository, it runs the install packages, formatting the code, linting the code, and then testing the code functions
  
## 4. Requirements.txt

The requirements.txt file has a list of packages to be installed for any required project. Currently, my requirements file only contains generic python packages, more specific packages can and will be added depending on scope of projects over time.


## Reference

* Refer to this [GitHub Actions with .devcontainer](https://github.com/nogibjj/matrix_testing_keon/blob/main/.github/workflows/cicd.yml)
