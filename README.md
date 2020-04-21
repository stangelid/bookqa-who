# BookQA: Character-based Book Question Answering

This repo holds the BookQA evaluation dataset described in the paper:

[**Book QA: Stories of Challenges and Opportunities**](https://www.aclweb.org/anthology/D19-5811/)

Stefanos Angelidis, Lea Frermann, Diego Marcheggiani, Roi Blanco and Lluís Màrquez  
_In Proceedings of the Workshop on Machine Reading for Question Answering (2019)_


## Obtaining the data
You can download our **character-based evaluation data** using [this google drive url](https://drive.google.com/uc?id=1rK8ud9BHeMZrnXv_P6QQorVuJvohl5cp&export=download).

You can find the original book texts from DeepMind's [NarrativeQA repo](https://github.com/deepmind/narrativeqa).


## Dataset description
Using the NarrativeQA corpus as a starting point, we have constructed a classification-style dataset of 3,427 question-answer pairs, spanning 614 books. All questions expect a character from the corresponding book as the answer. Thus, the QA task is reduced to a prediction over a book-specific, pre-defined set of characters. For more information about our dataset, please refer to our paper.

## Files and data formats
The public dataset is split in 3 files:


