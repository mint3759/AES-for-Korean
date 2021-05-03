# Automated Essay Scoring for Korean
### (Last updated at April 21, 2021)
> A Deep Learning model that predicts the score of a given input essay. 
> Currently only for English Dataset(ASAP). Korean Dataset is not opened yet.

## To do
 - Learning  
 - Fine-tuning Codes  
 - \.ipynb to \.py  

## Progress \& Performance
### Considered Parts
 - Dataset: **By prompt** or **Combined**
 - Input Information: A vector corresponds to **Essay** or **Sentence** or **Word**
 - Model: **GRU** or **BERT-based**
 - Embedding: **Glove** or **BERT-based**
 - QWK: Quadratic Weighted Kappa Score. 0.0 \- 1.0.
### Evaluation
> The accuracy is calculated by Quadratic Weighted Kappa(QWK).
> Due to the lack of dataset, we used 5-Fold Cross Validation and measure the QWK for each fold.

| \# | Dataset | <center>Input</center> | <center>Model</center> | <center>Embedding</center> | <center>Progress</center> | <center>QWK</center> |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 1 | Combined | 1 Essay = 1 Essay Average Vector | GRU | Glove | Done | 0.6427 |
| 2 | Combined | 1 Essay = 128 Sentence Average Vectors | GRU | Glove | Done | 0.7594 |
| 3 | By prompt | 1 Essay = 128 Sentence Average Vectors | GRU | Glove | Done |
| 4 | Combined | 1 Essay = 512 Word Vectors | GRU | Glove | Done | 0.7923 |
| 5 | By prompt | 1 Essay = 512 Word Vectors | GRU | Glove | Done |
| 6 | Combined | 1 Essay = 128 Sentence Average Vectors | GRU | pretrained BERT | Done | 0.7319 |
| 7 | Combined | 1 Essay = 512 Word Vectors | GRU | pretrained BERT | Learning |
| 8 | By prompt | 1 Essay = 1 Vector from BERT | GRU | pretrained BERT | Learning |
| 9 | Combined | 1 Essay = 128 Sentence Average Vectors | GRU | pretrained ELECTRA | Coding |
| 10| Combined | 1 Essay = 512 Word Vectors | GRU | pretrained ELECTRA | Coding |
| 11| By prompt | 1 Essay = 1 Vector from ELECTRA | GRU | pretrained ELECTRA | Coding |
| 12| Combined | 1 Essay = 1 Vector from BERT | Fine-tuning BERT | BERT | Learning |
| 13| Combined | 1 Essay = 1 Vector from ELECTRA | Fine-tuning ELECTRA | ELECTRA | Coding |

## Requirements
 - Tensorflow 2.4.1
 - Keras 2.4.3
 - Gensim 3.2.0
