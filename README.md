# A6_distilBERT


![image](https://github.com/edvyan/A6_distilBERT/assets/46171741/45cb2efc-8cb4-439d-905c-5f3c6b9b7a1c)


In an experiment involving model distillation techniques, different layer selection strategies were employed to train student models using a teacher model. The outcomes varied as follows:

Top-K Layer Selection: Utilizing the top layers of the teacher model, the student model showed a training loss of 0.2737 and a validation loss of 0.7949, achieving a validation accuracy of 68.00%.

Bottom-K Layer Selection: Distillation with the bottom layers of the teacher model led to a slightly better training loss of 0.2376 and a comparable validation loss of 0.7908, enhancing the validation accuracy slightly to 68.70%.

Odd Layer Selection: Employing only the odd layers for distillation, the training loss was reduced to 0.2289, though the validation loss increased to 0.8093. The validation accuracy was similar to the Top-K approach at 67.50%.

Even Layer Selection: This strategy, using only even layers, achieved the lowest training loss at 0.2266 and a validation loss of 0.8265, but it surprisingly resulted in the highest validation accuracy of 66.50% among all tested strategies.

Challenges encountered in this experiment included the resource intensity and time consumption associated with training multiple student models, particularly with large datasets and complex models. To overcome these limitations, an improvement strategy could be to ensemble multiple student models that have been trained using different initial layer selection methods. Ensemble methods typically lead to better performance and greater robustness.
