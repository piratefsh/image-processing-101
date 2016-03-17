# Image Processing 101

Code examples on how to do things with OpenCV on [iPython Notebook](http://ipython.org/notebook.html).

## Installation

These instructions are for Mac OSX. For installation on other systems, feel free to use your own choice of a virtual environment for Python. OpenCV for Python requires a local installation of OpenCV on your machine, from which we will create symlinks to in your virtual environment.

### step 1
Install [virtualenv](https://virtualenv.readthedocs.org/en/latest/)

### step 2
Install [OpenCV](http://opencv.org/)


```
# install OpenCV and create symlinks
brew tap homebrew/science
brew install opencv
```
### step 3
Set up virtual environment

```
# create virtual environment
virtualenv .venv
source .venv/bin/activate

# install requirements, which includes iPython 
pip install -r requirements.txt
```

### step 4
Create symlinks to local OpenCV installation

```

# for other systems, change the path to site-packages to where your OpenCV installation lies. 

cd .venv/lib/python2.7
ln -s `brew --prefix opencv`/lib/python2.7/site-packages/cv.py cv.py
ln -s `brew --prefix opencv`/lib/python2.7/site-packages/cv2.so cv2.so

```

### Installation for Anaconda

```
conda install -c https://conda.anaconda.org/menpo opencv3
```

## Development

To run the iPython notebook, which will open up a browser tab with the .ipynb file that you can now work on.

```
ipython notebook
```

## Common errors

### ImportError: No module named cv2
Did you complete step 4 of the installation? Ensure that you are linking to existing cv2.py and cv2.so files. 

### cv2 still not found even after proper linking
Try restarting the virtual enviroment and iPython.

```
deactivate
source .venv/bin/activate
ipython notebook
```

## Other errors?
Submit an issue on Github, and I'll do my best to help you out!

