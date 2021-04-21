# Automated Essay Scoring for Korean
### (Last updated at April 21, 2021)
> A Deep Learning model that predicts the score of a given input essay. 
> Currently only for English Dataset(ASAP). Korean Dataset is not opened yet.

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
| 4 | Combined | 1 Essay = 768 Word Vectors| GRU | Glove | Learning |
| 5 | By prompt | 1 Essay = 768 Word Vectors| GRU | Glove | Learning |
| 6 | Combined | 1 Essay = 128 Sentence Average Vectors | GRU | pretrained BERT | Learning |
| 7 | Combined | 1 Essay = 128 Sentence Average Vectors | GRU | pretrained ELECTRA | Coding |
| 8 | Combined | 1 Essay = ?? | Fine-tuning BERT | BERT | Planning |
| 9 | Combined | 1 Essay = ?? | Fine-tuning ELECTRA | ELECTRA | Planning |

## Requirements
 - Tensorflow 2.4.1
 - Keras 2.4.3
 - Gensim 3.2.0