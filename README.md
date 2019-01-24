# Number Recognition

A Machine Learning Algorithm I worked on using keras' MNIST dataset. My testing data is of 10,000 images but for sanity's sake I also drew some numbers on [Paint.NET](https://www.getpaint.net/) by resizing it to 28x28 pixels as my own testing data.

## How to view the files

For some reason GitHub seems to be having a [problem](https://github.com/jupyter/notebook/issues/3035) on their backend sometimes. I just find that restarting it at a later time works. If the issue doesn't fix itself you can always use [Jupyter's nbviewer](https://nbviewer.jupyter.org/) to render and view the files. You can also just click the links in the ReadMe to view the \*.ipynb files
## Models

| Model Name     | Description | Testing Accuracy Rate % |
|---|---|---|
|[FCModel](https://nbviewer.jupyter.org/github/ghostiek/NumberRecognition/blob/master/Models/Notebooks/FCModel.ipynb)| A Fully Connected Neural Network | ~96
|[SimpleConvModel](https://nbviewer.jupyter.org/github/ghostiek/NumberRecognition/blob/master/Models/Notebooks/SimpleConvModel.ipynb)       | A pretty straightforward Convolutional Model| ~98
