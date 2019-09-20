This is the implementation of Word2Vec SkipGram . Ive followed the tutorial of [DerekChia](https://github.com/DerekChia/word2vec_numpy) you can check out his Code. 
Author: Derek Chia
Email: derek@derekchia.com

# Word2Vec
Ive implemented the Word2Vec model with the help of above tutorial for better understanding on how word Embedding is done .Some of the addition that i have done to the code are as follows -

 1. Cbow Embedding
 2. Cosine Similarity
 3. Euclidean Distance 

## Project Example - 
In Word Embedding a Word in represented in the form of a vector . After the representation various Mathematical Tasks can be performed on the Vector 

    Language   ---  [0.26,0.75,1.56,0.54]
    Processing ---  [0.82,0.41,0.16,0.75]
  
Example  - 


> text = "the day is friday and the day is sunday and the day is thursday and the day is wednesday and the day is Monday"

Ive chosed the above test purposely to show how Word Embedding for words that appear in similar context have a similar vector or closer in `Cosine and Eucledian Distance` below are the Top Similar Words

#### Training Parameter -

> settings = {	'window_size': 2,'n': 3,'epochs': 200,'learning_rate': 0.01}


## Skip-Gram

> Predict Context Words based on the target Word

Similar Words to Word - `monday`
| Cosine Similarity |Theta |Eculedian Distance|Distance
|--|--|--|--|
| monday |0.99|monday|0.0
sunday |0.99|sunday|0.41
wednesday| 0.98|wednesday|0.41
friday |0.98|friday|0.42
thursday |0.96|thursday|0.55
the |0.89|the|0.69
day |0.14 |and|2.83

## CBOW

> Predict target word based on the context word

Similar Words to Word - `monday`
| Cosine Similarity |Theta |Eculedian Distance|Distance
|--|--|--|--|
| monday |0.99|monday|0.0
sunday |0.62|sunday|0.97
thursday| 0.58|thursday|1.55
friday |0.23|wednesday|3.29
wednesday |-0.32|friday|0.55
day |-0.34|and|3.34
is |-0.37 |is|4.96
  

    
    
    
