# Twon-Simulations - Large Scale Simulations

The repository contains a three modules recommender, schedular, and networks. The first module recommender run the ranking service and update the ranking of the feed. The second module schedular run the service to get response from different LLMs. The third module is network generation that is to create a graph of users in mongodb.

# Project Setup and Execution

This project involves running a series of scripts written in Python and Node.js. The `Makefile` provided in this repository helps automate the process of installing dependencies and running the scripts in the correct order.

## Prerequisites

- **Python**: Make sure Python is installed on your system. You can download it from [python.org](https://www.python.org/).
- **Node.js**: Make sure Node.js is installed on your system. You can download it from [nodejs.org](https://nodejs.org/).

## Makefile Targets

The `Makefile` includes the following targets:

This target installs the python dependencies for Networks directory.
```sh
make install_network
```
This target installs the Node.js dependencies for both the Schedular and Recommender directories.
```sh
make install_node
```
This target runs the Generate_Networks.py script located in the Networks directory. The output is logged to networks.log.
```sh
make generate_networks
```
This target runs the recommender.js script from the Recommender directory and the schedular.js script from the Schedular directory simultaneously and the output is logged to ranker.log and Schedular.log.
```sh
make run_recommender_schedular
```
