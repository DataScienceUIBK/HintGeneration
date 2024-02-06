<span align="center">
    <a href="https://huggingface.co/datasets/JamshidJDMY/TriviaHG/tree/main"><img alt="Huggingface" src="https://img.shields.io/static/v1?label=Dataset&message=TriviaHG&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAMAAAAoLQ9TAAAAIGNIUk0AAHomAACAhAAA+gAAAIDoAAB1MAAA6mAAADqYAAAXcJy6UTwAAAIoUExURQAAAP/////57v/67xUVFf/clv+KAP/uzf/sxv8AAP9TAP/ltP///v/ouP/////////////////////////////8+v/pvP/biP/Vbf/Vbv/cif/qv//9+//////////03v/Yev/Zfv/14//25v/Uav/Vbv/46//////dkf/gmP/////04P/25//pvP/sxf/////lr//ouP/qwP/tyf/msv/ntf/+/P/36f/LUf/36P/w0v/w0//w0//w0//78//gm//QZv/RZv/gm//78v/////14v/nt//gnP/hn//w0f/////w0f/hn//gnP/nt//14v/////////////////LLv/MGv/PGf/LL//LG//THP/THv/SHv/UHv/LGv/LH/7SHuK8JOzDIuW+I+jAI//LHv/PTP/NF/PBG3BkOpyGMvrOH4R0NoV0NvzJGv/MF//QT//MLv/LGPu/FNayJu7FIdq2Jf7DFP/JF//ML//LJurCIsCiKujCIubAI7+hK/DHIf/LJ//HK//NGf/SHeS9IlxSP25QQmtOQmVZPu3DIf/RHf/HLP++Kf/AD/++EP3EFNCfLNhpQthrQdinKv/FFP/AEP+/K/++Dv/BEv+/Ef/CE//MIf/NIP/MGf++D//KTP/FOP/DE//PG//PHP/JGP/EFP/EM//BDf/TH//GFP/CEP/DEP/EEv/BDv/MS//IJ//JHf/JHP/JP//IQf/IHP/IJv/LSf///7SHOh0AAABUdFJOUwAAAAAAAAAAAAAAAAAABiZCQykIAUGn3/Hy4q5KAwRy7vJ/Yfb7cR/X4ipkdpepAqi5mavM2z5v/pGTtZS2QtP4999bIGyry8yUR4fJzbJ2BRIRE9ZoIHEAAAABYktHRAH/Ai3eAAAAB3RJTUUH6AIGEyohVAr+rAAAARZJREFUGNNjYGBgZGTi4xcQFBJmZmRkYQDxRUTFxCUkpaRlZBkZQXw5eYWQ0LCw0HBFJWGgCCOrskpEZFR0dExkrKoaG1BAXSMuPiExOjopOSpFU4uRgV07NS09IzMqKzsnNy9fh4OBU7egsKi4JCo6ubSsvEJPlkHfoDIqqqq6prauPiqqwVCYgcuosam5pbWtvaOzq6nbWJZBy6Snt69/wsRJk6f0TZ1masZgbjF9xsxZhbPnzJ01c8a8+ZYMVgt6F5aHLly0eGHokqVTl1kz2CxYXhi1YuWq1WuiouauXWbLYGe/bv2GjZscHDdv2bh1m5MzA7eLq5u7h6eXoLePr5+/ENDpjBwBgYH6PIyMQcF8vIyMAKnZUpQQgaV4AAAAJXRFWHRkYXRlOmNyZWF0ZQAyMDI0LTAyLTA2VDE5OjQyOjI1KzAwOjAwybP6HAAAACV0RVh0ZGF0ZTptb2RpZnkAMjAyNC0wMi0wNlQxOTo0MjoyNSswMDowMLjuQqAAAAAodEVYdGRhdGU6dGltZXN0YW1wADIwMjQtMDItMDZUMTk6NDI6MzMrMDA6MDBAgVbbAAAAAElFTkSuQmCC&color=20BEFF"/></a>
    <a href="https://colab.research.google.com/github/DataScienceUIBK/TriviaHG/blob/main/Framework/Framework.ipynb"><img src="https://img.shields.io/static/v1?label=Colab&message=Framework&logo=Google%20Colab&color=f9ab00"></a>
</span>

# TriviaHG: A Dataset for Automatic Hint Generation for Factoid Questions

This repository contains folders pertaining to the results and experiments discussed in the paper *TriviaHG: A Dataset for Automatic Hint Generation for Factoid Questions*. Below, we provide details regarding the materials available in this repository:

## Dataset

Within this folder, you will find the training, validation, and test sets of the TriviaHG dataset. Refer to the table below for the dataset statistics:

|                   | Training | Validation | Test  |
| ----------------- | -------- | ---------- | ----- |
| Num. of Questions | 14,645   | 1,000      | 1,000 |
| Num. of Hints     | 140,973  | 9,638      | 9,619 |

## Framework

Contained within this folder is the code for the proposed framework designed to generate hints for given questions. To execute the code, follow these steps:

1. Start by training the QuestionType Detector. Run `Train.ipynb` located in the `Framework/utils/Hint_Generation/Question_Classification` directory.

2. Once the QuestionType Detector is trained, run `Pipeline.py`. This will initiate the framework, generating hints and evaluating them based on the convergence and familiarity quality attributes for the questions listed in the `Framework/questions/questions.json` file.

## Human Evaluation - Answering

This folder contains Excel files used to solicit responses from six human participants. Each participant received ten Excel files, with each file comprising ten questions. The table below represents the types of questions and the corresponding statistics from each participant.

|  Question Type  |  Hard-B  |  Hard-F  |  Hard-V  |  Medium-B  |  Medium-F  |  Medium-V  |  Easy-B  |  Easy-F  |  Easy-V  |
|-----------------|----------|----------|----------|------------|------------|------------|----------|----------|----------|
|      ENTITY     |  5 / 9   |  5 / 9   |  4 / 9   |   8 / 8    |   6 / 8    |   4 / 8    |  8 / 8   |  8 / 8   |  6 / 8   |
|      HUMAN      |  2 / 9   |  0 / 9   |  0 / 9   |   5 / 8    |   1 / 8    |   0 / 8    |  6 / 8   |  6 / 8   |  4 / 8   |
|     LOCATION    |  0 / 9   |  0 / 9   |  0 / 9   |   7 / 8    |   5 / 8    |   2 / 8    |  7 / 8   |  6 / 8   |  4 / 8   |
|      OTHER      |  3 / 9   |  2 / 9   |  0 / 9   |   5 / 8    |   2 / 8    |   0 / 8    |  8 / 8   |  7 / 8   |  7 / 8   |

## Human Evaluation - Quality

This folder contains ten Excel files, including human annotation values for relevance, readability, ambiguity, convergence, and familiarity quality attributes for 2,791 hints. The table below presents the average scores for each quality attribute.

|         Method       |    Match     | Readability  |  Ambiguity   | Convergence  | Familiarity  |
|----------------------|--------------|--------------|--------------|--------------|--------------|
|         Bing         |     4.09     |     4.67     |     1.51     |     2.23     |     2.47     |
| LLaMA 7b - Finetuned |     4.01     |     4.70     |     1.56     |     2.20     |     2.41     |
|  LLaMA 7b - Vanilla  |     3.64     |     4.47     |     1.87     |     2.12     |     2.02     |

## Model Performance

In this folder, you will find the generated hints and their evaluation values for convergence and familiarity quality attributes. Refer to the table below for the results across different models.

|        Model        | Convergence | Familiarity |
|---------------------|-------------|-------------|
|   LLaMA_7b_Vanilla  |    0.307    |    0.833    |
|  LLaMA_13b_Vanilla  |    0.350    |    0.929    |
|  LLaMA_7b_Finetuned |    0.400    |    0.890    | 
| LLaMA_13b_Finetuned |    0.410    |    0.881    |
|  LLaMA_70b_Vanilla  |    0.425    |    0.941    |
|       GPT_3.5       |    0.438    |    0.911    |
|     WizardLM_70b    |    0.446    |    0.942    |
|        Gemini       |    0.455    |    0.911    |
| LLaMA_70b_Finetuned |    0.494    |    0.862    |
|     GPT_4_turbo     |    0.525    |    0.875    |
|         Bing        |    0.540    |    0.946    |

## Entities

This folder contains a JSON file comprising 50,000 entities used in IQR to find Q1 and Q3 for normalization.
