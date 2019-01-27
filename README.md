# Number Recognition

A Machine Learning Algorithm I worked on using keras' MNIST dataset. My testing data is of 10,000 images but for sanity's sake I also drew some numbers on [Paint.NET](https://www.getpaint.net/) by resizing it to 28x28 pixels as my own testing data.

## How to view the \*.ipynb files

For some reason GitHub seems to be having a [problem](https://github.com/jupyter/notebook/issues/3035) on their backend sometimes. I just find that restarting it at a later time works. If the issue doesn't fix itself you can always use [Jupyter's nbviewer](https://nbviewer.jupyter.org/) to render and view the files. You can also just click the links in the table below to view the \*.ipynb files.

## Models

| Model Name     | Description | Testing Accuracy Rate % |
|---|---|---|
|[FCModel](https://nbviewer.jupyter.org/github/ghostiek/NumberRecognition/blob/master/Models/Notebooks/FCModel.ipynb)| A Fully Connected Neural Network | ~96
|[SimpleConvModel](https://nbviewer.jupyter.org/github/ghostiek/NumberRecognition/blob/master/Models/Notebooks/SimpleConvModel.ipynb)       | A pretty straightforward Convolutional Model| ~98
|[ConvModel_v1](https://nbviewer.jupyter.org/github/ghostiek/NumberRecognition/blob/master/Models/Notebooks/ConvModel_v1.ipynb) | Convolutional Model | ~99


## Models Architecture

#### FCModel:

INPUT (1x784) -> [FC -> RELU]\*2 -> [FC -> SOFTMAX]

#### SimpleConvModel:

INPUT (28x28x1) -> [CONV2D -> RELU]\*2 -> MAXPOOL2D -> [FC -> SOFTMAX]

#### ConvModel_v1:

INPUT (28x28x1) -> [[CONV2D -> RELU]\*2 -> MAXPOOL2D -> BATCHNORMALIZATION]\*2 -> [FC -> RELU] 

-> [FC -> SOFTMAX]

## Dependencies

| Package     | Version |
|---|---|
| numpy | 1.15.4
| matplotlib | 3.0.2
| keras | 2.2.4 
| Pillow | 5.4.1
| tensorflow | 1.12.0
