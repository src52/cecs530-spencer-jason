# Approximate Computing for Energy-Efficient CNN Training with CIFAR-10

This notebook was ran with the following dependencies and requirements:

Python 3.10

etrommer/torch-approx 0.1.0 on Github, commit `10e0a87c5f31bc9c4ad0c4105fe608edcebb120d`

etrommer/agn-approx 0.1.0 on GitHub, commit `efbd57985989828bbf4d2cbf5e27fc62b60456e2`

# Setup

## Setting up Python 3.10

Begin by creating a virtual Python environment with version 3.10.19.

You can install Python 3.10.19 manually, or use a Python version manager like `pyenv`. The example I am providing uses `pyenv`.

`pyenv install 3.10`

`pyenv virtualenv 3.10 env_name`

`pyenv activate env_name`

Once you are running Python version 3.10, ensure pip is installed by running the following:

`python -m ensurepip --upgrade`

## Setting up torch-approx and evoapproxlib

Then, clone this repository with the .ipynb file, and `cd` into the directory.

Once you are in the directory, clone the `torch-approx` repository at commit `10e0a87c5f31bc9c4ad0c4105fe608edcebb120d`.

Using a terminal, `cd` into the torch-approx root directory and run `pip install --no-build-isolation .`

While still in the `torch-approx` directory, execute the `./install_evoapprox.sh` script. This will take about five to ten minutes to build, as it's compiling a lot of C code.

## Setting up agn-approx

Once installed, `cd ..` out of the torch-approx directory, back into the root of this repository. Clone the `agn-approx` repository at commit `efbd57985989828bbf4d2cbf5e27fc62b60456e2`, and `cd` into the `agn-approx` folder.

Run `pip install --no-build-isolation .` to install the `agn-approx` package.

`cd` out and return to the root of this repository, with the .ipynb file.

## Setting up jupyter-lab and executing the notebook

Run `pip install ipykernel wheel ninja jupyterlab`

Run `python -m ipykernel install --user --name=<name_of_your_env>`

Run `jupyter-lab`. It will open a web browser, and once there select "Kernel > Change Kernel" from the top menu bar. Ensure your virtual environment is selected.

You can now run the cells in order.
