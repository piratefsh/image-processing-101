# Image Processing 101

Code examples on how to do things with OpenCV on [iPython Notebook](http://ipython.org/notebook.html).

## Installation

These instructions are for Mac OSX. For installation on other systems, feel free to use your own choice of a virtual environment for Python. OpenCV for Python requires a local installation of OpenCV on your machine, from which we will create symlinks to in your virtual environment.

1. Install [virtualenv](https://virtualenv.readthedocs.org/en/latest/)
2. Install [OpenCV](http://opencv.org/)

```
# install OpenCV and create symlinks
brew tap homebrew/science
brew install opencv
```

3. Set up virtual environment

```
# create virtual environment
virtualenv .venv
source .venv/bin/activate

# install requirements, which includes iPython 
pip install -r requirements.txt
```

4. Create symlinks to local OpenCV installation

```

# for other systems, change the path to site-packages to where your OpenCV installation lies.

cd .venv/lib/python2.7
ln -s /usr/local/Cellar/opencv/2.4.10/lib/python2.7/site-packages/cv.py cv.py
ln -s /usr/local/Cellar/opencv/2.4.10/lib/python2.7/site-packages/cv2.so cv2.so

```

## Development

To run the iPython notebook, which will open up a browser tab with the .ipynb file that you can now work on.

```
ipython notebook
```


