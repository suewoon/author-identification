Spooky Author Identification - Identify authors from their writings
-----------------------
Disclamer: The problem set was originally posted on [Kaggle.com](https://www.kaggle.com/c/spooky-author-identification)

### Competition Overview 
Dataset contains text from works by three of authors(Edgar Allan Poe, HP Lovecraft, Mary Wollstonecraft Shelley). This Challenge aims to accurately identify the author of the sentences in the test set. 

### Data Dictionary 
For this project, the train dataset has 19579 different texts from three of authors.  Both train and test dataset reside in `intput` directory.

There are following features:

- **id**: a unique identifier for each sentence 
- **text**: some text written by one of the authors 
- **author**: the author of the sentence (`EAP`: Edgar Allan Poe, `HPL`: HP Lovecraft, `MWS`: Mary Wollstonecraft Shelley)

### Model & Results  

I tried a couple of models with word embeddings and without. As a result, SVC turned out to be the most accurate one, which leads me to the accuracy 0.43293. 


Installation 
-----------------------
Need to proceed these follwing steps in order to re-generate the same result. 

### Clone the repo
```git clone
```

### Install pipenv 
```pip install pipenv
```

### Install requirements 
```pipenv install 
```

EDA & Modelling Explained
-----------------------
EDA and modelling proceess is in 

1. [EDA]()
2. [Modelling Explained]()