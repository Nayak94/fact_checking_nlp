# Fact Verfication using ML and NLP
- This project is dedicated to perform [fact checking](https://www.politifact.com/article/2018/feb/12/principles-truth-o-meter-politifacts-methodology-i/) of the claims recorded by various press, media and social medial organizations. The dataset used is available on Datacommons.
- The data can be viewed [here](https://huggingface.co/datasets/datacommons_factcheck)

### Requirements:

- Before proceeding, kindly make sure you have a spacy v3.x installed and it's English language medium size model is installed("en_core_web_md")

- If not kindly refer here for installing [spacy](https://spacy.io/usage) and [language](https://spacy.io/models/en) models

- Also the datasets api from HuggingFace should be installed from [here](https://huggingface.co/docs/datasets/installation.html) to download datasets.

### Implementation 

- Besides text classfication, the purpose of this project is also to use industry-grade nlp packages and state-of-the-art nlp architectures provided by them. Spacy is one of developing entity in this category. 

- Below is the expected data format by the text classfier. 

|    | texts                                                                                  | labels                               |
|---:|:---------------------------------------------------------------------------------------|:-------------------------------------|
|  0 | 1928 school board send home letter child say al smith elect president allow read bible | {'cats': {'True': 1.0, 'Fake': 0.0}} |
|  1 | country rich wealth country dissipate horizon                                          | {'cats': {'True': 0.0, 'Fake': 1.0}} |
|  2 | pope francis mass jesus metaphorical literal                                           | {'cats': {'True': 0.0, 'Fake': 1.0}} |
|  3 | say politifact report 95 percent donald trump say lie                                  | {'cats': {'True': 0.0, 'Fake': 1.0}} |
|  4 | marijuana schedule drug understand mean research                                       | {'cats': {'True': 0.0, 'Fake': 1.0}} |

Note :- The texts above is preprocessed i.e. punctuations and stopwords removed and lemmatized.

- Below are the results achieved using Bag-Of-Words binary text classifier.

<h3><center>Epochs:100, n_gram=2, drop=0.2</center></h3>

<h3><center>Train set results</center></h3>

|    |     True |     Fake |
|:---|---------:|---------:|
| p  | 1        | 1        |
| r  | 0.278135 | 0.721865 |
| f  | 0.435221 | 0.838468 |

<h3><center>Test set results</center></h3>

|    |     True |     Fake |
|:---|---------:|---------:|
| p  | 1        | 1        |
| r  | 0.244011 | 0.755989 |
| f  | 0.392297 | 0.861041 |


### References

- Spacy Knowledge Base from [here](https://spacy.io/usage/v3-1)

