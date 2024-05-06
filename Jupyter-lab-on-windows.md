# de-ik-matmernok2

## Jupyter Lab and MATLAB kernel on Windows:

In order to use the MATLAB kernel in Jupyter Lab or Notebook:
- Matlab has to be installed
- a valid license is needed to be activated
- correct version of Python has to be installed
- Jupyter Lab / Jupyter Notebook has to be installed
- MATLAB kernel has to be installed

This was tested on Windows 10 2022H2.

## Installation steps:
#### Python:
You should have that already installed on your system. In order to check which version of Python is currently installed:
`python --version`
`python -V`
`py --version`
`py -V`

[Mathlab and Python compatibility](https://www.mathworks.com/support/requirements/python-compatibility.html)
Matlab is currently compatible with python versions: 3.9 / 3.10 / 3.11

###### Troubleshooting:
* If Python is not installed, download and install the latest version from [Python's official website](https://www.python.org/downloads/). When installing: "Add Python to environment variables"/ "Add Python to path" 
* If `python` is not working, but `py` is, then python is not in the path.
* How to add python to path:
  * windows key + x >> System  >> Advanced system settings >> Environment variables >> Path >> Edit >> New
    * C:\Users\"user"\AppData\Local\Programs\Python\Python"xxx"\
    * C:\Users\"user"\AppData\Local\Programs\Python\Python"xxx"\Scripts\

####  Matlab
If you are installing from scratch, this should be the next step. You can download the installer from [MathWorks website](https://www.mathworks.com/downloads/). Don't forget to install the `Symbolic math toolbox`.

#### Install Jupyter Lab:
In the command prompt type `pip install jupyterlab`
Check if Jupyter Lab is working properly by typing `jupyter lab` into the command prompt. It will be opened in the default browser at `localhost:8888/lab`
Shutdown Jupyter Lab (File >> Shut Down)

#### Install MATLAB kernel for Jupyter Lab:
In my experience, this is the tricky part.

`pip install matlab_kernel`
Open jupyter lab by typing `jupyter lab` in te command prompt and choose MATLAB notebook from the Launcher.

You can check the status of the kernel in the upper right corner. It should be in idle status.

This code will test, if the MATLAB kernel and Symbolic math toolbox is installed and working correctly:
```matlab
syms y(t);
input = diff(y,t) + 3*y == exp(3*t);
solution = dsolve(input);
disp(solution)
```
Kernel status: busy, dolgozik kicsit és ki kellene írnia az eredményt
`exp(3*t)/6 + C1*exp(-3*t)`

###### Troubleshooting:
You can check the logs and you can look for errors in the command prompt where jupyter lab was started from.
---
If the kernel is connected and in idle status, but it is not implementing the code (i.e., the status of the kernel is not changed to busy):
- Shutdown Jupyter Lab.
- Open MATLAB.
- Run the command `matlab.engine.shareEngine` to enable the MATLAB Engine API for Python.
- Close MATLAB.

Run the command prompt as administrator and navigate to the folder: `matlabroot\extern\engines\python`
`cd "matlabroot\extern\engines\python"` // for example matlabroot = "C:\Program Files\MATLAB\R2024a"
In the directory enter this command:
`python -m pip install .`
This has something to do with Python and the MATLAB engine.

You can try to add MATLAB to the path as well.
`where matlab`

Kernel error messages: 
kernel died, it will restart automatically
kernel disconnected
no kernel
kernel status connecting utan kernel status idle 

expose python? https://am111.readthedocs.io/en/latest/jmatlab_install.html

#### 5. Configure Jupyter Lab to work with MATLAB kernel:
- Open Jupyter Lab by typing `jupyter lab` in the command prompt.
- Create a new Jupyter notebook by clicking on the "New" button and selecting "Notebook" -> "MATLAB".
- Start using MATLAB in Jupyter Lab!

