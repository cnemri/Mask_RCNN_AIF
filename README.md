# AI Framework Final Project

## 1. Introduction

The aim of this tutorial is to demonstrate the operation of Mask RCNN, a Deep-Learning-based algorithm that can detect objects in an image, classify them and tell which pixels belong to which object in the image.

## 2. Libraries and major dependencies

* Linux
* *Matterport* MaskRCNN implementation.
* Conda virtual environment
* Python > 3.6
* Keras
* Tensorflow-**cpu** = 1.15
...

## 3. Getting started

### Installing Conda

If you do not have Anaconda installed you can follow the instructions provided by the official documentation:
https://docs.conda.io/projects/conda/en/latest/user-guide/install/

### Setting the Virtual Environment

Run this command in the terminal :

`conda create -n MaskRCNN python=3.6 pip`

### Installing the dependencies

* Place the **requirements.txt** in your current working directory
* Activate your conda environment by running : `conda activate MaskRCNN`
* Run the following command : `pip install -r requirements.txt`

### Install Pycocotools

* Clone this repo : `git clone https://github.com/waleedka/coco.git`
* Go to PythonAPI and open the Makefile
* Replace python by python3
* Set your current working directory to PythonAPI and run `make` from a terminal

Congratulations ! you installed pycocotools successfully !

### Getting MaskRCNN pre-trained weights :

(Already done for you)

* Go to : https://github.com/matterport/Mask_RCNN/releases
* Download the **mask_rcnn_coco.h5** file
* Place the file in the *Mask_RCNN* directory


## 4. MaskRCNN on image

To test MaskRCNN on images, you can open the *demo.ipynb* in the samples folder and run it. It will randomly choose pictures from the images folder and do object detection, classification and will apply masks on them. Make sure that you have activated *MaskRCNN conda environment*.

## 5. MaskRCNN on Webcam feed

To test MaskRCNN using Webcam feed, you should run `python visualize_cv.py` from your terminal. A new window with frames from the webcam with masks, bounding boxes and objects annotations will appear. Since we are using the CPU tensorflow version, you will notice that the frames flow is dramatically slow.

## 6. MaskRCNN on video files

To test MaskRCNN with video files, you should do the following :

* Convert the video to mp4 format.
* Rename it to *videofile.mp4*.
* Place it into the *Mask_RCNN* directory.
* Activate *MaskRCNN conda environment*.
* Run `python process_video.py` from your terminal in the Mask_RCNN directory.

It will take a lot of time, a new video called *videofile_masked.avi* will be created in the same directory. You can interrupt the video processing any time using **Ctrl+C**. You will have your *videofile_masked.avi* anyway. It will contain the frames that the algorithm has already processed.
