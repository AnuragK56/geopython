# Spatial Data Science with PyData

* Time: Thursday, April 12, 13:30 - 15:30

### Instructors

- [Levi John Wolf](https://ljwolf.org) - [University of Bristol](http://www.bristol.ac.uk/geography/levi-j-wolf/overview.html)
- Sergio Rey - [Center for Geospatial Sciences, University of California, Riverside](http://spatial.ucr.edu/peopleRey.html)

### In collaboration with

- [Dani Arribas-Bel](http://darribas.org/) -  University of Liverpool
- [Wei Kang](http://spatial.ucr.edu/peopleKang.html)
- [Marynia Kolak](https://marynia.me)
- [Joris Van den Bossche](https://jorisvandenbossche.github.io/) - Ghent University 

This repository contains the materials and instructions for the Spatial Data Science with PyData workshop at [Geopython 2018](http://2018.geopython.net/#w0).

## Schedule

- 13:30 - 14:25: Representing spatial relationships for Data Science
- 10 Minute Break
- 14:35 - 15:30: Using spatial information to build better models

## Obtaining Workshop Materials

The preferred method for attending the workshop is to get a local installation of the software packages running on your own computer. 
This makes it simple for you to take what you've learned and apply it in your own work. 
As a secondary alternative, we suggest you consider the directions provided by [@darribas](https://twitter.com/darribas) about [the Geographic Data Science software stack, made available on docker.](https://github.com/darribas/gds_env).

If you are familiar with GitHub, you should clone or fork this GitHub repository to a specific directory. Cloning can be done by:

```bash
git clone https://github.com/weikang9009/pysal_AAG2018.git
```

If you are not using git, you can grab the workshop materials as a zip file by pointing your browser to (https://github.com/pysal/geopython) and clicking on the green *Clone or download* button in the upper right.

![download](figs/download.png)

Extract the downloaded zip file to a working directory.

## New to Command Line

Are you not sure how to access a working directory or command line? For this workshop, we recommend starting with two points:

1. find your Terminal,
2. Learn to Change Your Working Directory.

For those who have MacOS operating systems, you can find Terminal in your Utilities. For those using other operating systems, search for multiple options online, depending on your taste. A terminal launched looks like this:

![terminal](figs/terminal.png)

Once in your terminal, type ```ls```. This will list all of the contents in your current directory. You will likely see your Data, Documents, Desktop, Download, and many other folders and files. 

To change working directories, you will type ```cd``` plus the name of the directory you'd like to change to. If you are diving into a subdirectory, or child of the directory you were just in, then that name on its own is sufficient. For example, to access the "Downloads" directory, you type ```cd Downloads```.

![downloads](figs/downloads.png)

If you just downloaded the zip file into Downloads, first make sure you have unzipped the folder. Once unzipped, assuming it is still in the Downloads directory, type ```cd pysal_AAG2018``` to access. Then ```ls``` to list the contents. You have successfully navigated to your working directory to the workshop, and are ready for installations!

![downloads](figs/workingdir.png)

## Installation

We will be using a number of Python packages for geospatial analysis. 

**Please make sure to do these setup steps before attending the conference!**

### Setting up the environment

An easy way to install all of these packages is to use a Python distribution such as [Anaconda](https://www.anaconda.com/download/#macos). In this workshop we will be using **Python 3.6** so please download that version of Anaconda. 

- [Installing on Windows](https://docs.anaconda.com/anaconda/install/windows)
- [Installing on Mac](https://docs.anaconda.com/anaconda/install/mac-os)

![anaconda](figs/anaconda.png)

Once you have downloaded Anaconda, start a terminal and navigate to the directory of the downloaded/ cloned materials. If you just learned to navigate to your working directory in the tutorial above, you are ready for the next step. For those who need a refresh: if the materials now live in the directory ```/Users/hu/wei/Dropbox (ASU)/python_repos/pysal_AAG2018```, you need to navigate to that directory from the terminal (using command ```cd```):

![directory](figs/directory.png)

Once we have done that, run:

```bash
conda-env create -f gds_stack.yml
```

This will build a conda environment that sandboxes the installation of the required packages for this workshop so we don't break anything in your computer's system Python (if it has one).

This may take 10-15 minutes to complete depending on the speed of your network connection.

Once this completes, you can activate the workshop environment with:

* on Mac, Linux
```bash
source activate gds
```
* on Windows:
```bash
activate gds
```


###
Next, you will want to test your installation with:
```bash
 jupyter-nbconvert --execute --ExecutePreprocessor.timeout=120 check_workshop.ipynb
```

You should see something like:
```bash
[NbConvertApp] Converting notebook check_py_stack.ipynb to html
[NbConvertApp] Executing notebook with kernel: python3
[NbConvertApp] Writing 393375 bytes to check_py_stack.html
```

Open check_workshop.html in a browser, and scroll all the way down, you should see something like:

![htmlout](figs/htmlout.png)

If you do see the above, you are ready for the workshop.
