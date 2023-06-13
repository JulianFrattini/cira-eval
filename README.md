# CiRA Evaluation

[![GitHub](https://img.shields.io/github/license/JulianFrattini/cira-eval)](./LICENSE)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.8033165.svg)](https://doi.org/10.5281/zenodo.8033165)

## Summary of the Artifact

This repository contains the code to evaluate the capability of the [CiRA tool](https://github.com/JulianFrattini/cira) to automatically generate test case descriptions from causal natural language requirements. To this end, thre requirements of the [Corona Warn App](https://github.com/corona-warn-app/cwa-documentation/blob/main/scoping_document.md) were manually classified as either *causal* or *non-causal*, and for all causal sentences, a set of test cases were generated. These manually generated test cases are compared to the output of CiRA.

## Structure of the Artifact

This repository contains the following files:

* `data` : data necessary for the evaluation
  * `caw-acceptance-criteria`: list of sentences constituting the acceptance criteria of the Corona Warn App, manually classified as either *causal* or *non-causal*
  * `ground-truth`: a json files containing a manually generated set of test cases following the CiRA test suite syntax for every *causal* sentence
* `src\evaluation.ipynb`: Jupyter notebook for performing the calcularion
* `requirements.txt`: required Python libraries for executing the evaluation

## How to reproduce

In order to reproduce the evaluation, follow the steps below:

1. Make sure both [Python 3.10](https://www.python.org/downloads/release/python-3100/) and [pip](https://pypi.org/project/pip/) are available on your system.
2. Install the [requirememts](./requirements.txt) by running `pip install -r requirements.txt`.
3. Make sure the [CiRA tool](https://github.com/JulianFrattini/cira) is available on your system.
    1. Follow the [installation instructions](https://github.com/JulianFrattini/cira/blob/main/README.md) to set up the CiRA tool on your system.
    2. Ensure that the RESTful API, which the CiRA tool provides, is currently running.
4. Execute the [evaluation](./src/evaluation.ipynb) notebook.

## License

Copyright © 2023 Julian Frattini

This work (source code) is licensed under  [MIT License](./LICENSE).