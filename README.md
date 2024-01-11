
# Image Caption Generator

The objective of the project is to build a Image Caption Generator that takes an image as its input and generates a caption in English beirfly describing the image.

## Dataset and Technologies

We have made use of the Flickr 8k dataset, which consists of approximately 8000 sample images along with 5 captions with each image. 

To encode representations from the input images, we used the VGG16 and the Inception V3 pre-trained CNN Models.

To learn the representations from the textual captions, we used the LSTM and GRU Recurrent Neural Networks.

## Model Architecture

We have used a three-phase architecture to build and train the Image Caption Generator. 

#### 1. Feature Extraction Phase

In this phase, the primary goal is to extract features from an image for training. 

This phase uses the CNN architectures mentioned above. The final output of this phase is features extracted in the form of vectors of size 256.

#### 2.	Encoder Phase

The primary goal of this phase is to learn numeric representations from the caption learnt so far pertaining to an image so far.

This phase uses the RNN architectures mentioned above. The final output of this phase is features extracted in the form of vectors of size 256.

#### 3. Decoder Phase

The primary goal of this is to concatenate the outputs of the Feature Extraction and Encoder Phases. This phase also produces the required output, which is the predicted word given an image and the caption generated till that point in time.

## Model Evaluation

We implemented four models using above-mentioned CNN and RNN architectures:

1. VGG16 - LSTM Model
2. VGG16 - GRU Model
3. InceptionV3 - LSTM Model
4. InceptionV3 - GRU Model

- The codes for each of these models can be found in the 'Codes' folder.
- The flowcharts for the architrctures of each of these models can be found in the 'Model Flowcharts' folder.

We evaluated the models using the training and testing errors obtained for each of them.

We also made use of the BLEU scores (BLEU - 1, BLEU - 2, BLEU - 3 and BLEU - 4 with cumulative weights) for evaulation.

## Results

The models using the Inception V3 Module take lesser time to train and give better results compared to the VGG16 models.

The models using the LSTM network take slightly more time than the GRU models but give better results.
