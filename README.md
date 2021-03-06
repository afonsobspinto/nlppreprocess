# NLPPREPROCESS

NLPPREPROCESS is a preprocessing package for NLP task. The main objective of the package is to reduce time consumed for preprocessing by using ready made functions.

# Requirements

 * Python 3.4 or higher

# Installation

 ### Using PIP via PyPI
 ```
 $ pip install nlppreprocess
 ```

 ### Manually via GIT
 ```
 $ git clone git://github.com/gaganmanku96/nlppreprocess
 $ cd nlppreprocess
 $ python setup.py install
 ```

# Functionalities
1. Replaces words
2. Remove stopwords
3. Remove numbers
4. Remove HTML tags
5. Remove punctations
6. Lemmatize words either by Wordnet or Snowball

# Usage
```
>>> from nlppreprocess import NLP
>>> obj = NLP()
```
 ## Parameters
 ```
 >>> obj = NLP(
        replace_words=True,
        remove_stopwords=True,
        remove_numbers=True,
        remove_HTML_tags=True,
        remove_punctation=True,
        lemmatize=False,
        lemmatize_method='wordnet'
       )
 ```
 ## Using with Pandas Library
 ```
 >>> dataFrame['text'] = dataFrame['text'].apply(obj.process)

 ```
 ## Using with plain text
 ```
 >>> print(obj.process("Pass a text here"))
 ```
 ## Add more stopwords
 ```
 >>> obj = NLP()
 >>> obj.add_stopword(['this', 'and this'])
 ```
 ## Add more replace words
 ```
 >>> obj = NLP()
 >>> obj.add_replacement([("original", "replacement")])
 ```
