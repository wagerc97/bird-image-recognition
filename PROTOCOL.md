# Protocol
### Using Keras/Tensorflow to build an image classifier neural network.
[What is Keras?](https://www.simplilearn.com/keras-vs-tensorflow-vs-pytorch-article#:~:text=is%20Deep%20Learning%3F-,What%20is%20Keras%3F,-What%20is%20PyTorch) -
Basically, Keras is an API that allows us to define the architecture of the neural network (NN).

[What is TensorFlow?](https://www.simplilearn.com/keras-vs-tensorflow-vs-pytorch-article#what_is_tensorflow) -
Basically, TensorFlow is a deep learning framework focussing on data flow for industry ready applications. 

## Load in image data
We use the [Bird Species](https://www.kaggle.com/datasets/gpiosenka/100-bird-species?select=birds+latin+names.csv) dataset from Kaggle. The input data is structured sucht that the parent directory of each image file names their label. Tensorflow can uses this file structure conveniently ([ImageDataGenerator](https://www.tensorflow.org/api_docs/python/tf/keras/preprocessing/image/ImageDataGenerator) would generate exactly this structure). 

We use ``image_dataset_from_directory()`` to generate the training, validation and test data from the directory.
As we use the data generator, the model infers the labels from the parent directories. Thus, they do not have to be stored in an array explicitly.  
