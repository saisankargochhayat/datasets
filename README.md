# Thoth Datasets

This repo contains notebooks to download and explore the datasets provided by Thoth Team.

The datasets are available from two sources:

- On Kaggle under [Thoth Station](https://www.kaggle.com/thothstation/datasets), where you can also use them directly through Kaggle kernels.
If you want to work locally, just download the dataset after signing in with your account.

- As [Git LFS](https://git-lfs.github.com/) under this repo if you want to work on your local machine.

## Overview

The goal of this repo is to provide datasets widely available and useful for data scientists.
Thoth Team within the office of the CTO at Red Hat has collected datasets that can be made open source within the IT domain for training Machine Learning models.

## Datasets

- Thoth Solver Dataset

- Thoth Performance Dataset

### Thoth Solver Dataset

Thoth Solver Dataset is based on solver reports created using [Thoth Dependency Solver](https://github.com/thoth-station/solver)
which tries to answer a simple question - what packages will be installed (resolved by pip or any Python compliant dependency resolver) for the provided stack?

Thoth Solver Dataset is made by 10000 solver reports in json format: ~436Mb once extracted. 
([.zip file](https://github.com/thoth-station/datasets/blob/master/notebooks/thoth-solver-dataset/thoth-solver-dataset-v1.0.zip) ~102.8Mb Git LFS)

and it is described in the notebook called [Thoth Solver Dataset](https://github.com/thoth-station/datasets/blob/master/notebooks/thoth-solver-dataset/ThothSolverDataset.ipynb).

### Thoth Performance Dataset

Thoth Performance Dataset has been created with one of the components of Thoth called [Amun](https://github.com/thoth-station/amun-api).
This service acts as an execution engine for Thoth where applications are built and tested using [Thoth Performance Indicators (PI)](https://github.com/thoth-station/performance).
Amun can be scheduled through another component in Thoth called [Dependency Monkey](https://github.com/thoth-station/adviser/blob/master/docs/source/dependency_monkey.rst).
This component aims to automatically verify software stacks and aggregate relevant observations.
Thoth Performance Dataset contains tests on performance for software stacks for different types of applications (e.g Machine Learning).

Thoth Performance Dataset is made by ~4000 inspection reports in json format: ~46Mb once extracted.
([.zip file](https://github.com/thoth-station/datasets/blob/master/notebooks/thoth-performance-dataset/thoth-performance-dataset-v1.0.zip))


## Working on your branch (Git LFS)

This repository relies on [Git LFS](https://git-lfs.github.com/),
therefore you need to install `Git LFS` following these [instructions] (https://git-lfs.github.com/)
in order to use the datasets when you change branch using `git ceckout`.

## Start working on the data

After cloning the repo follow these steps:

1. Install `pipenv`.

```bash
pip install pipenv
```

2. Install the dependencies provided in `Pipfile` and `Pipfile.lock` in an environment.

```bash
pipenv install
```

3. Start using the notebook provided or work on your own notebook with the dataset.

```bash
pipenv run jupyter-notebook
```

## How you can use the Data

You can download and use this data for free for your own purpose, all we ask is three things

- you cite Thoth Team as the source if you use the data;
- you accept that you are solely responsible for how you use the data;
- you do not sell this data to anyone, it is free!
