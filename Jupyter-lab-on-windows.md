# de-ik-matmernok2

### How to install Jupyter Lab, and MATLAB kernel on Windows:

In order to use the MATLAB in Jupyter Lab or Notebook, 
- Matlab has to be installed
- a valid license is needed to be activated
- MATLAB kernel has to be installed

Matlab is only compatible with python versions: 
3.9 
3.10 
3.11

## Installation steps:
#### Install Python:
- check which version of Python is currently installed on the system
`$ python --version`
3.11.9
- ha python nem működik de py igen csekk hogy pathban van-e

#### Install MATLAB:
- Login to the [MathWorks website](https://www.mathworks.com/downloads/) and download the installer for Windows
- Run the installer, don't forget to install `symbolic math toolbox`
- After installation run MATLAB and give in credentials when needed (<neptunkód>@mailbox.unideb.hu + password)
- Close MATLAB

#### Install Jupyter Lab:
- in the command prompt type `pip install jupyterlab`
- check if Jupyter Lab is working properly by typing `jupyter lab` into the command prompt
- shutdown Jupyter Lab

#### Install MATLAB kernel for Jupyter Lab:
- 

#### 1. Install Python:
- Check if Python is installed by opening a command prompt and typing `py --version` or `python --version`.
- If Python is not installed, download and install the latest version from [Python's official website](https://www.python.org/downloads/).
when installing - Add Python to environment variables
ha mégse működik akkor:
PATH-hez:
ha python --version nem fut
python ms store-t nyitja meg
de py --version működik akkor:
add python to PATH
windows key + x system properties >> system >> advanced system settings >> Environment variables >> Path double click >> ott new:
new
C:...user...appdata..pythonXX
pythonXX\Scripts
OK
Manage app execution aliases
App installer turn off

#### 2. Install MATLAB:
- Ensure you have a valid MATLAB license.
download login neptun@mailbox.unideb.hu
symbolic math toolbox
- Download the MATLAB installer from [MathWorks website](https://www.mathworks.com/downloads/).
- Run the installer and follow the installation instructions.

#### 3. Install Jupyter Lab:
- Open a command prompt and type `pip install jupyterlab`.
check if installed correctly: jupyter lab
shutdown

#### 4. Install MATLAB kernel for Jupyter:
- Open MATLAB.
- Run the command `matlab.engine.shareEngine` to enable the MATLAB Engine API for Python.
- Close MATLAB.
pip install jupyter-matlab-proxy
install engine API https://www.mathworks.com/help/matlab/matlab_external/install-the-matlab-engine-for-python.html
cd "matlabroot\extern\engines\python"
python -m pip install .
ez pl hibát dob python 3.12-re
- Open a command prompt and type `pip install matlab_kernel`.
- Type `python -m matlab_kernel install --user` to install the MATLAB kernel for Jupyter.


#### 5. Configure Jupyter Lab to work with MATLAB kernel:
- Open Jupyter Lab by typing `jupyter lab` in the command prompt.
- Create a new Jupyter notebook by clicking on the "New" button and selecting "Notebook" -> "MATLAB".
- Start using MATLAB in Jupyter Lab!

ha nem működik - no kernel - kernel disconnected jobb felső sarok
bezár
pip install setuptools 
vagy matlab path-hez adása
where matlab
első futásnál bejelentkezés

expose python? https://am111.readthedocs.io/en/latest/jmatlab_install.html