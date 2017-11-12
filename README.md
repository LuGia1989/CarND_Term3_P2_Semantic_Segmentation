# Semantic Segmentation
### Overview
In this project, we will label the pixel of a road using a Fullly Convolution Network technique. The pre-trained VGG16 network is chosen and first used as a decoder. A 1x1 convolutional layer is connecting the decoder and encoder to preserve spatial information. Then the feature maps extract from different levels of the VGG16 network are directly sent to the corresponding transpose convolutional layers in the decoder as extra input to take advantage of information extracted from multiple semantic levels. The model structure is a replicate from this paper: [Fully Convolutional Networks for Semantic Segmentation](http://ieeexplore.ieee.org/abstract/document/7478072/). 

### Set up

 - python 3.6
 - tensorflow 1.4
   Numpy
   SciPy
   Mathplotlib

### Model Hyper-parameters

These following are the  hyper-parameters that I selected:

 - Epochs: 50
 - Batch size: 32
 - Learning rate: 0.0001
 - Dropouts: 0.25

Also, in the `training_log.txt` file shows the log during the model training using the above hyper-parameters.

##### Dataset
Download the [Kitti Road dataset](http://www.cvlibs.net/datasets/kitti/eval_road.php) from [here](http://www.cvlibs.net/download.php?file=data_road.zip).  Extract the dataset in the `data` folder.  This will create the folder `data_road` with all the training a test images.

### Start
##### Run
Run the following command to run the project:
```python Semantic_Segmentation.py
```

### Result Exploration
Sample of pixel mapping on the road can be found in the folder `runs`.  The visualization of the sample of the pixel mapping on the road can be run in the `Semantic_Segmentation_Exploration.ipynb` 
