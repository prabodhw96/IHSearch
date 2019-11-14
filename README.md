# Image Hashing Search Engine

## Overview
In this project, we build a scalable image hashing search engine using OpenCV, Python, and VP-Trees. Image hashing algorithm finds duplicate or near-duplicate images in a dataset based on their computed hashes. VP-tree is a special data structure that can be used to scale image hashing search engine to millions of images.

Using a VP-Tree we can reduce our search complexity from O(n) to O(log n), enabling us to obtain our sub-linear goal!

## Dependencies
Install the following dependencies using pip:
* numpy
* cv2
* imutils
* vptree

## Dataset
[CALTECH-101 Dataset](http://www.vision.caltech.edu/Image_Datasets/Caltech101/) is used for this project. It consists of 9,144 total images across 101 categories.

## Execution
Add the location of images in ``index_images.py``.<br>
``imagePaths = list(paths.list_images("101_ObjectCategories"))``<br>
``101_ObjectCategories`` refers to the location of images.

Create the pickle files of hashes and VP-tree by running ``index_images.py``.<br>
``$python index_images.py``

For searching an image,<br>
``$python search.py --query "image location"``