# Number Recognition

Machine Learning Algorithms I worked on using keras' MNIST dataset. My testing data is of 10,000 images but for sanity's sake I also drew some numbers on [Paint.NET](https://www.getpaint.net/) by resizing it to 28x28 pixels as my own testing data. The best solution, using CNN, ranked 58th out of 2,468 teams (Top 2.35%) on [Kaggle's Digit Recognizer Competition](https://www.kaggle.com/c/digit-recognizer).

## How to view the \*.ipynb files

For some reason GitHub seems to be having a [problem](https://github.com/jupyter/notebook/issues/3035) on their backend sometimes. I just find that restarting it at a later time works. If the issue doesn't fix itself you can always use [Jupyter's nbviewer](https://nbviewer.jupyter.org/) to render and view the files. You can also just click the links in the table below to view the \*.ipynb files.

## Models

| Model Name     | Description | Testing Accuracy Rate % | Kaggle Public Leaderboard % |
|---|---|---|---|
|[FCModel](https://nbviewer.jupyter.org/github/ghostiek/NumberRecognition/blob/master/Models/Notebooks/FCModel.ipynb)| Fully Connected Neural Network | ~96 | ~97 |
|[SimpleConvModel](https://nbviewer.jupyter.org/github/ghostiek/NumberRecognition/blob/master/Models/Notebooks/SimpleConvModel.ipynb)       | Straightforward Convolutional Model| ~98.5 | N/A |
|[ConvModel_v1](https://nbviewer.jupyter.org/github/ghostiek/NumberRecognition/blob/master/Models/Notebooks/ConvModel_v1.ipynb) | Convolutional Model | ~99.3 | ~99.9 |
|[ConvModel_v2](https://nbviewer.jupyter.org/github/ghostiek/NumberRecognition/blob/master/Models/Notebooks/ConvModel_v2.ipynb) | Changed placement of BN<br> and added a dynamic learning rate | ~99.6 | ~99.94 |


## Models Architecture

#### FCModel:

INPUT (1x784) -> [FC -> RELU]\*2 -> [FC -> SOFTMAX]

#### SimpleConvModel:

INPUT (28x28x1) -> [CONV2D -> RELU]\*2 -> MAXPOOL2D -> [FC -> SOFTMAX]

#### ConvModel_v1:

INPUT (28x28x1) -> [[CONV2D -> RELU]\*2 -> MAXPOOL2D -> BATCHNORMALIZATION]\*2 -> [FC -> RELU] 

-> [FC -> SOFTMAX]

#### ConvModel_v2:

INPUT (28x28x1) -> [[CONV2D -> RELU] -> BATCHNORMALIZATION]\*2 -> MAXPOOL2D -> DROPOUT]\*2 -> [FC -> RELU] 

-> [FC -> SOFTMAX]


### Positioning of BatchNormalization in the CNN Architecture

Although the authors of the [original research paper on BatchNormalization](https://arxiv.org/pdf/1502.03167.pdf) have indicated that it should be included between linear and non-linear layers it has been found [in practice to yield better results](https://github.com/ducha-aiki/caffenet-benchmark/blob/master/batchnorm.md) when adding it after the activation layer.


## Dependencies

| Package     | Version |
|---|---|
| numpy | 1.15.4
| matplotlib | 3.0.2
| keras | 2.2.4 
| Pillow | 5.4.1
| tensorflow | 1.12.0
