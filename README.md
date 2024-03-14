# A6_distilBERT

# Model Distillation Techniques Experiment

## Overview
In this experiment, different layer selection strategies were applied in the training of student models using a teacher model. The outcomes varied across different strategies.  

![image](https://github.com/edvyan/A6_distilBERT/assets/46171741/43e4da7d-ff85-40b6-9b59-4058e50b05c9)

Dataset: MNLI dataset https://cims.nyu.edu/~sbowman/multinli/   

## Experiment Results

### Top-K Layer Selection
- **Utilized Layers**: Top layers of the teacher model
- **Training Loss**: 0.2737
- **Validation Loss**: 0.7949
- **Validation Accuracy**: 68.00%

### Bottom-K Layer Selection
- **Utilized Layers**: Bottom layers of the teacher model
- **Training Loss**: 0.2376
- **Validation Loss**: 0.7908
- **Validation Accuracy**: 68.70%

### Odd Layer Selection
- **Utilized Layers**: Only odd layers for distillation
- **Training Loss**: 0.2289
- **Validation Loss**: 0.8093
- **Validation Accuracy**: 67.50%

### Even Layer Selection
- **Utilized Layers**: Only even layers
- **Training Loss**: 0.2266
- **Validation Loss**: 0.8265
- **Validation Accuracy**: 66.50%

## Challenges Encountered
- The initial layer selection is crucial for capturing task-specific features essential for the target task. Failure to align this layer selection with the student model's architecture and capabilities can hinder the effective transfer of knowledge distilled from the teacher model.
- Challenges encountered in this experiment included the resource intensity and time consumption associated with training multiple student models, particularly with large datasets and complex models. 

## Proposed Improvement
- Develop methods to dynamically choose initial layers that suit the student model's design and limits. 
- Another improvement strategy could be to implement multiple student models that have been trained using different initial layer selection methods. 
