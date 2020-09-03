# cars-classification
Applying what I learned from the [TensorFlow without a PhD](https://www.eventbrite.com/e/workshop-tensorflow-without-a-phd-by-martin-gorner-google-tickets-63597698428#) workshop by [Martin Görner](https://twitter.com/martin_gorner), I created a convolutional neural network that is trained to recognize images of cars and classify them. 
This was done using [Google Colaboratory](https://colab.research.google.com/), a browser-based environment that contains all the required dependencies, including TensorFlow and the required libraries.


## Dataset
The Cars dataset contains 16,185 images of 196 classes of cars. The data is split into 8,144 training images and 8,041 testing images, where each class has been split roughly in a 50-50 split. Classes are typically at the level of Make, Model, Year, e.g. 2012 Tesla Model S or 2012 BMW M3 coupe.

The images are uploaded to and stored in Google Drive, which can be mounted by Colab. The rest (annotations and class names) are stored locally and uploaded directly to Colab.

To speed up the training process, every image is reduced to a smaller color palette. The code in reassign_cluster.ipynb takes all of the image's pixel values, finds n=32 clusters, and declare each cluster centre will be a color in the output image.


## Instructions to run the notebook
Note: I recommend running the notebook using Google Colab, where we can utilize Google's powerful GPUs to help speed up the training process. In addition, there is no need to install any new libraries as they have already been installed on the remote machines.

1. First, download the [Stanford cars dataset](https://www.kaggle.com/jutrera/stanford-car-dataset-by-classes-folder)

2. Extract the zip file into a folder and upload it into your Google Drive

3. In this repository, click on cars_classification.ipynb and then "Open in Colab"

4. Go to the new tab and ensure that you are logged into your Google account

5. Modify `data_path` if it does not match the location of your dataset in Google Drive

6. Click on "Runtime" and "Run all", then "Run anyway" when a warning shows up


## Acknowledgements
The dataset is provided by [Stanford](http://ai.stanford.edu/~jkrause/cars/car_dataset.html)

3D Object Representations for Fine-Grained Categorization
Jonathan Krause, Michael Stark, Jia Deng, Li Fei-Fei
4th IEEE Workshop on 3D Representation and Recognition, at ICCV 2013 (3dRR-13). Sydney, Australia. Dec. 8, 2013.   

The dataset is organized into [classes folder](https://www.kaggle.com/jutrera/stanford-car-dataset-by-classes-folder) thanks to [Jesús Utrera](https://www.kaggle.com/jutrera) 


## Resources
[TensorFlow, Keras and deep learning, without a PhD](https://codelabs.developers.google.com/codelabs/cloud-tensorflow-mnist)

[Learn TensorFlow 5: Complex Images](https://codelabs.developers.google.com/codelabs/tensorflow-lab5-compleximages)
