# Chaii-37th-Place
I'd like to thank Google research and Kaggle for hosting this competition through this competition I have gained a lot of experience and the field of NLP.  this was my first NLP competition on Kaggle and I'm glad to have scored a silver medal which would tentatively make me a Kaggle competitions expert. 😃
## Approach 1 : Question answering
I trained the following models namely XLM-Roberta-large , MURIL , REMBERT , BERT trained on XQUAD. All models here have been trained for 5 folds with extra data. MLQA, Hindi xQuad, Tamil translated SQUAD.
| Model Name | H & T Split | Public LB Score |
| ---- | ---- | ---- |
| XLM Roberta Large | No | 0.771 |
| XLM Roberta Large | Yes | 0.754 |
| MURIL | Yes | 0.738 |
| Rembert | No | 0.788 |
| BERT | No | 0.642 |
| InfoXLM  | No  | 0.714 |

*My final model was a single five-fold ensemble of from Rembert trained on the extra data available from MLQA and XQUAD and Tamil translated SQUAD*

I would have tried ensembling models but averaging scores did note seem to work and as i had started seriously getting into the competition only in the last week I did not have time to figure out a voting pipeline as many other solutions have done.

## Approach 2: Seq2Seq (Incomplete) 😭
the second approach I attempted was by building a text to text transformer model using the mT5-base transformer. This approach showed promise as it was the only one in which all the correct letters were being predicted but in this I face the unique and weird problem that none of the spaces between the words were being predicted. hence I could not properly post process the outputs or this model to get a get a proper submission. I would be really grateful if someone from the Kaggle community would be able to help me out with this problem.

The links to my notebooks are as follows:
- Training Notebook : [Click here](https://www.kaggle.com/aishikai/chaii-seq2seq-mt5-fit)
- Seq2Seq Training notebook : [Click Here](https://www.kaggle.com/aishikai/chaii-rembert-fit)
- Inference Notebook : [Click Here](https://www.kaggle.com/aishikai/chaii-inference)
- H&T Split Inference Notebook :  [Click Here](https://www.kaggle.com/aishikai/chaii-inference-ht-split)
