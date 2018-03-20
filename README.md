Spooky Author Identification - Identify authors from their writings
-----------------------
Disclamer: The problem set was originally posted on [Kaggle.com](https://www.kaggle.com/c/spooky-author-identification)

### Competition Overview 
Dataset contains text from works by three of authors(Edgar Allan Poe, HP Lovecraft, Mary Wollstonecraft Shelley). This Challenge aims to accurately identify the author of the sentences in the test set(text multi-classification problem). 

### Data Dictionary 
For this project, the train dataset has 19579 different texts from three of authors.  Both train and test dataset reside in `intput` directory.

There are following features:

- **id**: a unique identifier for each sentence 
- **text**: some text written by one of the authors 
- **author**: the author of the sentence (`EAP`: Edgar Allan Poe, `HPL`: HP Lovecraft, `MWS`: Mary Wollstonecraft Shelley)

## Install 
This projects use MITIE for recognizing named entities. Install MITIE package and compile it as a shared library 
(If you're running Windows, this won't work. Go to [MITIE repo](https://github.com/mit-nlp/MITIE) for intsall guides)
```
# install 
pip install git+https://github.com/mit-nlp/MITIE.git

# compile 
cd mitielib
make
```

Process 
-----------------------
First off, I did some basic EDA on the dataset and try out couple of 
different models(with word embeddings) in order to predict authors 
from their writing with simple feature engineering. 
Next, I also extracted some named entities from writings as a feature generation.
Lastly, I compared the results(accuracy) between models with and without content-based features. 

The whole EDA and modeling proceess is in [Spooky Author Identification Notebook](https://nbviewer.jupyter.org/github/suewoon/author-identification/tree/master/modelling-exaplained.ipynb)

Model & Results  
-------------------------
As a result, SVC without word embeddings turned out to be the most accurate one, which led me to the accuracy 0.43293.  
