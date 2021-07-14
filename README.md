Getting started with Python
===========================

This is [Data Train](https://www.uni-bremen.de/research-alliance/forschungsdaten/data-train) course [OT-ST-WS-04](https://www.uni-bremen.de/research-alliance/forschungsdaten/data-train/data-train-curriculum/data-steward-track/ot-st-ws-04-getting-started-with-python)


You can run this notebooks interactevely on [![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/koldunovn/python_for_geosciences/master)
 
This is a short overview of how Python with examples of data analysis and visualization. 

PRs with corrections are very welcomed.

## Getting started for Linux/Mac (for Windows see below)

The fastest way is to install [Miniconda](http://conda.pydata.org/miniconda.html), that contains [`conda`](http://conda.pydata.org/docs/intro.html) package manager and `Python`. On the [Miniconda](http://conda.pydata.org/miniconda.html) page select **Python 3** installer script for your system and download it, for example:

```
wget https://repo.continuum.io/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
```

Change mode of the downloaded scrip to executable, e.g.:

```
chmod +x Miniconda3-latest-MacOSX-x86_64.sh
```

Run installation process:
```
./Miniconda3-latest-MacOSX-x86_64.sh
```
At the end the script will offer you to add Miniconda3 install location to the PATH in your `.bashrc/.bash_profile`. You should say 'yes'. Please double check that you have something like this in your `.bashrc/.bash_profile`:

```
# added by Miniconda3 4.3.21 installer
export PATH="/Users/koldunovn/miniconda3/bin:$PATH"
```
If you for whatever strange reason use csh/tcsh, then add to your `.cshrc`:

```
setenv PATH /Users/koldunovn/miniconda3/bin:$PATH
```
Now you can open a new terminal window (sourcing not always works) and try to type:

```
conda
```
if as a result you see conda help, then everything is set up properly. The last thing before installing packages is to add `conda-forge` channel:
```
conda config --add channels conda-forge 
```
Now you can install nessesary packages:
```
conda install ipython jupyter matplotlib scipy pandas netcdf4 requests xarray dask bokeh
```
To begin working with notebooks execute:
```
jupyter notebook
```
the browser should pop up with jupyter main page. You can navigate to the folder with notebooks from there and open them.

## Getting started for Windows

- First you have to download and install Anaconda python distribution for your system from [here](https://www.anaconda.com/products/individual#windows) (scroll down to "Anaconda installers"). [There is a nice video tutorial](https://medium.com/@GalarnykMichael/install-python-anaconda-on-windows-2020-f8e188f9a63d). If installation is sucessful, you will be able to work with several first notebooks. In order to work with `netCDF` files `xarray`, `dask`, `bokeh` some additional steps are required.

- Go to start menu and launch `Anaconda prompt` programm.
- Execute follwing commands:
```
conda config --add channels conda-forge 
```
and then
```
conda install netcdf4 requests xarray dask bokeh
```
- Agree with installation of additional packages by entering `Y`

Now you should be good to go. You can launch Jupyter notebook from visual Anaconda interface, or by opening `Anaconda prompt` and typing:
```
jupyter notebook
```


Author
========
Nikolay Koldunov

koldunovn@gmail.com
