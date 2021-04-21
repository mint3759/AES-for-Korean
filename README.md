# Automated Essay Scoring for Korean
> A Deep Learning model that predicts the score of a given input essay. 

## Work in Progress

## Project Target
|  <center>Header1</center> |  <center>Header2</center> |  <center>Header3</center> |
|:--------|:--------:|--------:|
|**cell 1x1** | <center>cell 1x2 </center> |*cell 1x3* |
|**cell 2x1** | <center>cell 2x2 </center> |*cell 2x3* |
|**cell 3x1** | <center>cell 3x2 </center> |*cell 3x3* |
| Num | <center>Input</center> | <center>Model</center> | <center>Embedding</center> | <center>Progress</center> |
|:-----:|:-----:|:-----:|:-----:|
| 1 | 1 Essay = 1 Essay Average Vector | 2 GRU Layer | Glove | Done |
| 2 | 1 Essay = n Sentence Average Vectors | 2 GRU Layer | Glove | Done |
| 3 | 1 Essay = m Word Vectors|2 GRU Layer | Glove | Code O, Learning X |
| 4 | 1 Essay = n Sentence Average Vectors | 2 GRU Layer | pretrained BERT | Code O, learning X |
| 5 | 1 Essay = n Sentence Average Vectors | 2 GRU Layer | pretrained ELECTRA | Code X |
| 6 | 1 Essay = ??|Fine-tuning BERT |BERT |Planning |
| 7 | 1 Essay = ??|Fine-tuning ELECTRA |ELECTRA |Planning |

## Performance

The accuracy is calculated by Quadratic Weighted Kappa(QWK).


## Requirements (last updated at April 17, 2021)
 - Tensorflow 2.4.1
 - Keras 2.4.3
 - Gensim 3.2.0