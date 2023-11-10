# BERTIS
This is the official repository for BERTIS, a model presented in the paper "*META4: Semantically-Aligned Generation of metaphoric gestures using self-supervised text and speech representations*".

This repo has information on the training and testing code of BERTIS. The model is published on [HuggingFace](https://huggingface.co/mireillfares/BERTIS).

Bibtex:
```ruby
@article{fares2023META4,
  title={META4: Semantically-Aligned Generation of metaphoric gestures using self-supervised text and speech representations},
  author={Fares, Mireille and Pelachaud, Catherine and Obin, Nicolas},
  journal={arXiv preprint arXiv:XXX.XXX},
  year={2023}
}
``` 

## BERTIS Model Description
BERTIS (BERT-based Image Schema) is a computational model designed to classify input texts into specific Image Schema classes. Image Schemas are cognitive patterns that play a fundamental role in shaping the way humans conceptualize and reason about various concepts present in language. BERTIS is built upon the BERT architecture. The model is fine-tuned using a specialized corpus created by *Wachowiak et al.(2022)*.

## BERTIS Image Schema Classes
The main purpose of BERTIS is to automatically categorize input texts into predefined Image Schema classes. BERTIS considers 14 distinct Image Schema classes, each capturing a specific cognitive pattern. These classes and their corresponding examples (taken from Wachowiak et al. (2022)) are listed below:
- *CENTER-PERIPHERY*: She brushed the thought away.
- *CONTACT*: That blew me away.
- *CONTAINMENT*: Keep it in the back of your mind.
- *COVERING*: His judgement is clouded.
- *FORCE*: They are attracted to each other.
- *LINK*: Breaking social ties.
- *OBJECT*: Seize the opportunity.
- *PART-WHOLE*: They assembled a theory.
- *SCALE*: This class is bigger than that one.
- *SOURCE_PATH_GOAL*: The time for action has arrived.
- *SPLITTING*: What separates the men from the boys?
- *SUBSTANCE*: Emotions are tinged with suffuse.
- *VERTICALITY*: No known spoken language uses the lateral axis for time.
- *SUPPORT*: The poor in our country need a boost up.


<!-- ### Model Sources [optional] --
- **Repository:** [More Information Needed]
- **Paper [optional]:** [More Information Needed]
- **Demo [optional]:** [More Information Needed]>
## Uses
<!-- Address questions around how the model is intended to be used, including the foreseeable users of the model and those affected by the model. -->
<!-- ### Direct Use This section is for the model use without fine-tuning or plugging into a larger ecosystem/app. [More Information Needed] -->
<!-- ### Downstream Use [optional] This section is for the model use when fine-tuned for a task, or when plugged into a larger ecosystem/app [More Information Needed] -->
<!-- ### Out-of-Scope Use This section addresses misuse, malicious use, and uses that the model will not work well for. [More Information Needed] -->
<!-- ## Bias, Risks, and Limitations This section is meant to convey both technical and sociotechnical limitations. [More Information Needed] -->
<!-- ### Recommendations This section is meant to convey recommendations with respect to the bias, risk, and technical limitations. Users (both direct and downstream) should be made aware of the risks, biases and limitations of the model. More information needed for further recommendations.
-->
<!-- ## How to Get Started with the Model
Use the code below to get started with the model.-->

# Training and Testing Details
The data used for training, validating and testing BERTIS is found in lwachowiak's [repo](https://github.com/lwachowiak/Systematic-Analysis-of-Image-Schemas-through-Explainable-Multilingual-Language-Models/blob/main/Data/Image%20Schemas%20English%20and%20German.csv). 

80% of the data were used for training BERTIS, 10% for validation, and 10% for testing it.
<!-- ### Training Procedure  This relates heavily to the Technical Specifications. Content here should link to that section when it is relevant to the training procedure. -->
<!-- #### Preprocessing [optional]
[More Information Needed]-->
<!--  #### Training Hyperparameters
- **Training regime:** [More Information Needed] <!--fp32, fp16 mixed precision, bf16 mixed precision, bf16 non-mixed precision, fp16 non-mixed precision, fp8 mixed precision 
#### Speeds, Sizes, Times [optional]
-->
<!-- This section provides information about throughput, start/end time, checkpoint size if relevant, etc. 
[More Information Needed]-->
# Evaluation
## Metrics
- Precision: measures the proportion of correctly predicted positive instances out of all instances predicted as positive. It focuses on the accuracy of positive predictions.
- Recall: measures the proportion of correctly predicted positive instances out of all actual positive instances. It focuses on the ability to capture positive instances.
- F1-score: the harmonic mean of precision and recall, providing a balanced measure that combines both metrics

## Results

|       Class      | Precision | Recall | F1-score |
| ---------------- | --------- | ------ | -------- |
|"CENTER-PERIPHERY"|    0.98   |  0.94  |   0.96   |
|"CONTACT"         |    1      |  1     |   1      |
|"CONTAINMENT"     |    0.74   |  0.67  |   0.7    |
|"COVERING"        |    1      |  1     |   1      |
|"FORCE"           |    0.8    |  0.91  |   0.85   |
|"LINK"            |    1      |  1     |   1      |
|"OBJECT"          |    0.81   |  0.83  |   0.82   |
|"PART-WHOLE"      |    1      |  1     |   1      |
|"SCALE"           |    1      |  1     |   1      |
|"SOURCE_PATH_GOAL"|    0.81   |  0.74  |   0.77   |
|"SPLITTING"       |    1      |  1     |   1      |
|"SUBSTANCE"       |    1      |  1     |   1      |
|"SUPPORT"         |    1      |  1     |   1      |
|"VERTICALITY"     |    0.88   |  0.93  |   0.90   |

**Overall Accuracy** : **0.93** 

For all Image Schema classes, F1-score is between 0.77 and 1, indicating that BERTIS performs well in terms of both accurately predicting the correct Image Schema classes (precision) and capturing many correct Image Schema classes as possible (recall). Indeed these results are also reflected in the precision and recall scores for all Image Schema classes. We observe a high precision (between 0.74 and 1) for all classes, which indicates the number of correct predicted
Image Schema classes. The recall scores are above 0.74 for most of the classes, with one Image Schema class having a recall score equal to 0.67. The overall accuracy of BERTIS with respect to all Image Schema classes is equal to 0.93, indicating a high accuracy and good performance in classifying the input text into the correct Image Schema classes. 



**Developed by:** Mireille Fares

**Language(s) (NLP):** English, can generalize to other languages such as German

**License:** Academic Free License

**Finetuned from model:** BERT Base Cased model

## Other cool stuff
[META4](https://github.com/mireillefares/META4/blob/main/README.md)
