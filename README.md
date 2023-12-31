# FairerOPTH
This is the official code of the paper:

**Fairer AI in Ophthalmology via Implicit Fairness Learning for Mitigating Sexism and Ageism**
## Abstract
The transformative impact of artificial intelligence (AI) in various domains determines that it should not only be accurate but also objective and fair. Unfair AI systems in ophthalmology pose huge challenges that may impact the delivery of fair and unbiased healthcare. Here, we propose a fairer AI model (called FairerOPTH) to mitigate AI sexism and ageism due to the inherent biases in eye disease incidence for patients of different ages and genders. Specifically, we incorporate the causal relationship between fundus features and disease diagnosis into the AI model learning, where the causal relationship is invariant to sensitive attributes such as race, gender, age, etc. To evaluate this implicit fairness learning method based on the causal relationship, we additionally collect the largest and most diverse fundus dataset from over 12,405 patients across a wide age range (0 to 90 years). The fundus dataset contains the advanced ultra-widefield and regular narrow-angle two types of fundus imaging datasets, where the ultra-widefield imaging dataset contains 16,530 fundus images annotated with 38 ophthalmic diseases and 67 fundus features, and the narrow-angle imaging dataset contains 4,550 fundus images annotated with 16 ophthalmic diseases and 20 fundus features. Through extensive evaluation and comparison with state-of-the-art approaches, we demonstrate the significant effect of the FairerOPTH in mitigating sexism and ageism. We also mathematically proved that incorporating the causal relationship can indeed improve the performance of the fundus disease identification model using the Shannon entropy theory. Our results highlight the potential of the implicit fairness learning method to promote fair and inclusive ophthalmological care, ensuring equitable treatment for patients irrespective of their gender or age.

## Codes and Models:
### Requirement:
* **PyTorch 1.10.1, torchvision 0.11.2. The code is tested with python=3.7, cuda=11.4.**

### Train:
#### for ultra-widefield
* **Run `OculoScope_train.py` to perform training. Checkpoint will be saved to  `./checkpoints/OculoScope/`.**
#### for narrow-angle
* **Run `MixNAF_train.py` to perform training. Checkpoint will be saved to  `./checkpoints/MixNAF/`.**

### Test:
#### for ultra-widefield
* **Run `OculoScope_val.py` to get the results of the accuracy experiment.**
* **Run `OculoScope_fairness_analysis.py` to get the results of age and gender fairness experiments.**
#### for narrow-angle
* **Run `MixNAF_val.py` to get the results of the accuracy experiment.**
