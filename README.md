A version of AlexNet used to classify fruits on the fruits-360 dataset (Tensorflow 1.15.0)

path_changes.txt consists of all the line numbers in different files where you need to specify a path of your own choice. (What the path is used for has also been described)

tfdl_env.yml consists of all the dependencies that you need to install in order to run the network.
This .yml file can be used to create a separate conda environment different from the 'base' conda environment.
Use the folowing code: conda env create -f tfdl_env.yml

fruits-360 folder consists of a sample Training class of images.
To download the entire dataset, go to the following link: https://www.kaggle.com/moltean/fruits
(Note:- I ignored the following classes in training and testing: Mangostan, Pear Kaiser, Tomato Maroon
You can involve them too, but you will have to do some dataset-related modifications)

dataset_rel_changes.txt contains required Dataset Related Modifications:
(After removing the 3 classes mentioned above, there were 52,200 images in training set total. For each epoch, 200 of these images were used, picked at different indices
2 images each 522 spaces apart)
Any dataset modification will require a number of changes in the code of cnn_saver.py.