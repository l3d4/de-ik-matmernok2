# de-ik-matmernok2

### Step-by-step guide to install MATLAB, Jupyter Lab, and MATLAB kernel on Windows:


#### 1. Install Python:
- Check if Python is installed by opening a command prompt and typing `python --version`.
- If Python is not installed, download and install the latest version from [Python's official website](https://www.python.org/downloads/).

#### 2. Install MATLAB:
- Ensure you have a valid MATLAB license.
- Download the MATLAB installer from [MathWorks website](https://www.mathworks.com/downloads/).
- Run the installer and follow the installation instructions.

#### 3. Install Jupyter Lab:
- Open a command prompt and type `pip install jupyterlab`.

#### 4. Install MATLAB kernel for Jupyter:
- Open MATLAB.
- Run the command `matlab.engine.shareEngine` to enable the MATLAB Engine API for Python.
- Close MATLAB.
- Open a command prompt and type `pip install matlab_kernel`.
- Type `python -m matlab_kernel install --user` to install the MATLAB kernel for Jupyter.

#### 5. Configure Jupyter Lab to work with MATLAB kernel:
- Open Jupyter Lab by typing `jupyter lab` in the command prompt.
- Create a new Jupyter notebook by clicking on the "New" button and selecting "Notebook" -> "MATLAB".
- Start using MATLAB in Jupyter Lab!
