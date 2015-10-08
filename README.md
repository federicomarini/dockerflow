# `dockerflow` - Docker-compose setup for simultaneous running of the flowcatchR-based containers

## Introduction

This repository provides the `docker-compose.yml` configuration file for running the [flowcatchR](http://bioconductor.org/packages/flowcatchR)-based containers simultaneously on the same machine using [Docker](http://www.docker.com/) containers and [Docker Compose](https://github.com/docker/compose).

The components are: 

* [`flowstudio`](https://github.com/federicomarini/flowstudio) - https://github.com/federicomarini/flowstudio, a command-line/IDE interface to RStudio where `flowcatchR` and its dependencies are preinstalled.
* [`flowshiny`](https://github.com/federicomarini/flowshiny) - https://github.com/federicomarini/flowshiny, a Shiny Server running the shinyFlow web application
* [`flowjupy`](https://github.com/federicomarini/flowjupy) - https://github.com/federicomarini/flowjupy, a Jupyter Notebook interface

For more information on how to install the single components, please refer to their repositories.

## Installation and setup

This app needs a recent version of Docker and Docker Compose:

 * [Docker installation instructions](https://docs.docker.com/installation/#installation)
 * [Docker Compose installation instructions](http://docs.docker.com/compose/)
 * clone this repository (`git clone https://github.com/federicomarini/dockerflow.git`)  

## Usage

* `cd` into the `dockerflow` folder
* `docker-compose up` (to pull the Docker images from the DockerHub)
* ... or alternatively `docker-compose up --file docker-compose_DIY.yml` (to have the images built locally from the cloned repositories of the components)
* If all goes well
    - On Linux, browse to [http://localhost:8888](http://localhost:8888) for the [Jupyter](http://jupyter.org/) notebook interface available in the home folder to find example notebooks illustrating the usage of the [`flowcatchR`](http://bioconductor.org/packages/flowcatchR) package
    - On Linux, browse to [http://localhost:3838/shinyFlow](http://localhost:3838/shinyFlow) for the [`shiny`](http://shiny.rstudio.com/) web application illustrating the usage of the [`flowcatchR`](http://bioconductor.org/packages/flowcatchR) package
    - On Linux, browse to [http://localhost:8787](http://localhost:8787) for the [RStudio](http://www.rstudio.com/) IDE interface available, , after logging in with user `rstudio` and password `rstudio`. A sample script with the full steps of the workflow is available for the user to learn and explore the functionality of the [`flowcatchR`](http://bioconductor.org/packages/flowcatchR) package. The package can be loaded with the conventional `library("flowcatchR")` command
    - On MacOS or Windows running [`Docker Toolbox`](https://www.docker.com/toolbox) find the Docker host URL with `docker-machine ip default|[name of the virtual machine]` and replace `localhost` in the locations specified above with the returned IP address

## Contact
For additional details regarding the functions of [`flowcatchR`](http://bioconductor.org/packages/flowcatchR), please consult the package documentation, the package vignette or write an email to marinif@uni-mainz.de. 

## Bug reports/Issues/New features

Please use https://github.com/federicomarini/flowcatchR/issues for reporting bugs, issues or for suggesting new features to be implemented.

