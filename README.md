# BookQA: Character-based Book Question Answering

This repo holds the BookQA dataset described in the paper:

[**Book QA: Stories of Challenges and Opportunities**](https://www.aclweb.org/anthology/D19-5811/)  
Stefanos Angelidis, Lea Frermann, Diego Marcheggiani, Roi Blanco and Lluís Màrquez  
_In Proceedings of the Workshop on Machine Reading for Question Answering (2019)_


## Obtaining the data
You can download our **character-based QA data** using [this google drive url](https://drive.google.com/uc?id=1rK8ud9BHeMZrnXv_P6QQorVuJvohl5cp&export=download).

You can find the **original book texts** from DeepMind's [NarrativeQA repo](https://github.com/deepmind/narrativeqa).


## Dataset description
Using the NarrativeQA corpus as a starting point, we have constructed a classification-style dataset of 3,427 question-answer pairs, spanning 614 books. All questions expect a character from the corresponding book as the answer. Thus, the QA task is reduced to a prediction over a book-specific, pre-defined set of characters. For more information about our dataset, please refer to our paper.

## Files and data formats
The public dataset is split in 3 files:

 - `characters.json`  
 Holds a mapping from character IDs to aliases used in the book text to refer to this character. It is formatted as follows:  
```  
{
  <book-id#1>: [
    {"id": <character-id#1>,
     "aliases": [list-of-aliases]},
    {"id": <character-id#2>,
     "aliases": [list-of-aliases]},
    ...
  ],
  ...
}
```  
 
 - `who_questions.json`
 Holds the questions (question IDs) and answers (character IDs). The question IDs refer to the index (0-indexed) of the question in the original NarrativeQA `qaps.csv` file. It is formatted as follows:  
```  
{
  <book-id#1>: [
    {"question_id": <question-id#1>,
     "answers": [list-of-character-ids]},
    {"question_id": <question-id#2>,
     "answers": [list-of-character-ids]},
    ...
  ],
  ...
}
```  
 
 - `artificial_questions.json`  
 Holds the artificial questions we used to pre-train our memory network. The format is as follows:
 ```  
{
  <book-id#1>: [
    {"question_id": <artif-question-id#1>,
     "question": <the-artificial-question-text>,
     "answer": <character-id>,
     "answer-text": <the-artificial-answer-text>,
     "source": <the-sentence-we-obtained-the-question-from>},
    {"question_id": <artif-question-id#2>,
     "question": <the-artificial-question-text>,
     "answer": <character-id>,
     "answer-text": <the-artificial-answer-text>,
     "source": <the-sentence-we-obtained-the-question-from>},
    ...
  ],
  ...
}
```  
