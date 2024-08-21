# ISIC 2024 - Skin Cancer Detection with 3D-TBP

## Goal

<a href ="https://www.kaggle.com/competitions/isic-2024-challenge">ISIC 2024 - Skin Cancer Detection with 3D-TBP </a> **Top 5%**

---

Identify cancers among skin lesions cropped from 3D total body photographs.

In this competition, you'll develop image-based algorithms to identify histologically confirmed skin cancer cases with single-lesion crops from 3D total body photos (TBP). 

The image quality resembles close-up smartphone photos, which are regularly submitted for telehealth purposes. 

Bbinary classification algorithm could be used in settings without access to specialized care and improve triage for early skin cancer detection.

3D TBD에서 잘라낸 피부 병변 중 암을 식별하는 것이 목표이다. 

3D total body photos (TBP)에서 single-lesion crops을 사용해 조직학적으로 확인된 피부암 사례를 식별하는 image-based algorithms을 개발한다. 

## Definition

## Overview

### **Evaluation**

**Primary Scoring Metric**

Submissions are evaluated on [partial area under the ROC curve (pAUC)](https://en.wikipedia.org/wiki/Partial_Area_Under_the_ROC_Curve) above 80% true positive rate (TPR) for binary classification of malignant examples. (See the implementation in the notebook [ISIC pAUC-aboveTPR](https://www.kaggle.com/code/metric/isic-pauc-abovetpr).)

pAUC는 ROC 곡선의 특정 부분, 즉 TPR(참 양성 비율)이 80% 이상인 영역을 평가한다. 

이는 높은 민감도를 요구하는 실제 임상 환경을 반영하기 위함이다. 

점수는 [0.0, 0.2] 범위 내에서 주어지며, TPR 80% 이상에서의 분류 성능을 강조한다. Image에서 파란색과 빨간색 영역이 각각 두 Algorithm의 pAUC를 나타낸다. 

![image](https://github.com/user-attachments/assets/ae199c45-0137-4efd-ad6d-a48757546501)

### **Dataset**

### **Submission**

For each image (`isic_id`) in the test set, you must predict the probability (`target`) that the lesion is **malignant**. The file should contain a header and have the following format:

Test Set에 포함된 Image(’isic_id’)에 대해 **malignant**(악성)일 확률(’target’)을 예측해야 한다. 

Submission File에는 Header가 포함되어야 하며, 아래와 같은 형식이다. 

```python
isic_id,target
ISIC_0015657,0.7
ISIC_0015729,0.9
ISIC_0015740,0.8
etc.
```

### **Timeline**

- **June 26, 2024** - Start Date.
- **August 30, 2024** - Entry Deadline. You must accept the competition rules before this date in order to compete.
- **August 30, 2024** - Team Merger Deadline. This is the last day participants may join or merge teams.
- **September 6, 2024** - Final Submission Deadline.
- **September 20, 2024** - Deadline for potential prize-winners to publish their solution code and write-ups.

All deadlines are at 11:59 PM UTC on the corresponding day unless otherwise noted. The competition organizers reserve the right to update the contest timeline if they deem it necessary.

## Technical Stack

`Python` `TensorFlow` `PyTorch`