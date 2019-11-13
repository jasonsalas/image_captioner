# Image Captioner in Keras
An image caption service combining a convolutional neural network (image-in) and a recurrent neural network (text out). This service uses Keras as the deep learning framework, based on the [Flickr8K dataset](https://forms.illinois.edu/sec/1713398) and evaluated using the [BLEU score](https://machinelearningmastery.com/calculate-bleu-score-for-text-python/).

Here's a sample caption produced by the neural network after being fed an image:

![sample output image with caption](https://github.com/jasonsalas/image_captioner/blob/master/output_images/soccer.JPG)

*INSTRUCTIONS*
- Download the [Flickr8K Dataset](https://github.com/jbrownlee/Datasets/releases/download/Flickr8k/Flickr8k_Dataset.zip) and [Flickr8k text](https://github.com/jbrownlee/Datasets/releases/download/Flickr8k/Flickr8k_text.zip) 
- Run the _extract_features()_ method in the [captioner notebook](https://github.com/jasonsalas/image_captioner/blob/master/captioner.ipynb) to derive *features.pkl* and the method to produce *descriptions.txt* files. You can run these locally on a CPU, which takes about an hour to go through the 8,092 images from Flickr. 
- You can then copy only the rest of the captioner notebook, *features.pkl* and *descriptions.txt* to a cloud platform like AWS, Google Colab or FloydHub to train the model on GPUs. This saves the model to disk, which can then be downloaded and used locally.
- Run the code in the [evaluator and predictor notebook](https://github.com/jasonsalas/image_captioner/blob/master/evaluator_and_predictor.ipynb) locally with the trained model, evaluating the performance and making new predictions on unseen images on your local drive.

(Of course, you could run everything in the cloud if you wish.)

This demo is based off the wonderful e-book [Deep Learning for Natural Language Processing](https://machinelearningmastery.com/deep-learning-for-nlp/) by [Dr. Jason Brownlee](https://twitter.com/TeachTheMachine), and discussed in [a couple](https://medium.com/swlh/image-captioning-in-python-with-keras-870f976e0f18) of [blog posts](https://medium.com/@faizanmustafa75/keras-implementation-of-image-captioning-model-3a7ab68e67d4).
