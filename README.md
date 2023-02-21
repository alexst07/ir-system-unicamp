# ir-system-unicamp
Task of ir system subject of Unicamp

## how to execute and test
### requirements
Anaconda

### Creating a new environment:
```shell
conda create --name irunicamp python=3.9
conda activate irunicamp
pip install jupyterlab
```

## Executing the notebook

To execute and test the notebook you just have to run all cells,
The function ```best_document_index``` calculate which document
from the dataset match better with each query.

The last part of the code will give the indexes of each document that
match better with each query:
```python
# find the best document match for each query
best_indexes = []
for q in query_corpus:
    best_i = best_document_index(q)
    best_indexes.append(best_i)
    
print(best_indexes)
```

## How this project was created?
This project uses gensim and numpy.
The first step was read and parse the dataset.
So, the corpus of documents and the dictionary was created.
These was the input of OkapiBM25Model from gensim.
So, TfidfModel was used the calculate the similarities between each document with the input query.
In the last, we calculated which document match best for each query.
ChatGPT was used to give information about the algorithm BM25, and give snippets of code about how to use 
gensim and BM25 in Python.
