Model Backend for 2026 Structural Stability Physical Reasoning AI Challenge
============================================
Summary
----------------
### We placed 25th at private LB.

This repository contains **the final version of code and models for submission** used for the 2026 Structural Stability Physical Reasoning AI Challenge hosted on DACON. ([Competition Link](https://dacon.io/competitions/official/236686))

Team Information
----------------
- **Team Name: Placeholder**
- **Public rank: 18th**
- **Private rank: 25th**
- **Private score: 0.02243**
- **Team Members: knowin_kyeong (Team Leader), 긴카호**

Directory Structure
-------------------
The base directory follows this directory structure (Simplified):

*Note: **In colab environment, you have to upload '2026PredictingStructuralStability'** on your Google Drive.*

*Note 2: **We removed /data files due to potential risks of violating DACON's data sharing policies.** Please replace it with your own copy of the dataset downloaded from DACON website.*

```
2026PredictingStructuralStability
│  requirements.txt
│  final_submission.csv
│
├─data (Place your own copy of dataset here)
│  │  dev.csv
│  │  sample_submission.csv
│  │  train.csv
|  ├─dev
|  |  ├─DEV_001
|  |  | ...
|  |  └─DEV_100
|  |─train
|  |  ├─TRAIN_0001
|  |  | ...
|  |  └─TRAIN_1000
|  |
|  └─test
|     ├─TEST_0001
|     | ...
|     └─TEST_1000
|
├─outputs
│      submission_001_convnext_tiny.csv
│
└─src
       001_convnext_tiny_fold1.pth
       001_convnext_tiny_fold2.pth
       001_convnext_tiny_fold3.pth
       001_convnext_tiny_fold4.pth
       001_convnext_tiny_fold5.pth
       001_train_convnext_tiny.ipynb
       002_postprocess.ipynb
```
**final_submission.csv** is the final submission file.

How to Run
----------
1. Place the 2026PredictingStructuralStability directory in your colab environment.
2. Set up the dataset in the **/data** directory from DACON website.
3. Run **all notebooks(001_train_convnext_tiny.ipynb, 002_postprocess.ipynb)** in the **/src** directory to train models and save the results. Note that **002_postprocess.ipynb requires prerequisite outputs from 001_train_convnext_tiny.ipynb**..
4. Submit the final submission file from **final_submission.csv** to DACON!

Requirements
------------
- All required python package is listed in **requirements.txt**.
- You need **GPU environment** to run the training notebooks.
- We tested only on **Google Colab Pro+, L4 GPU** environment. It may not work on other environments. Therefore **even though executing pip command with requirements.txt, some packages in the default colab environments is absent or have different versions, which may cause errors**. You can try to install missing packages **manually**.

Models Included
---------------
- **ConvNexT_tiny**: We used ConvNeXT_tiny architecture backbone for the main model with custom classification layer. We trained the model with 5-fold cross-validation and ensemble the results.

Reproducibility
-----------------
- All random seeds are fixed for reproducibility.

Contact
-------
If you have any questions, **please create an issue in this repository** or contact the team leader, knowin_kyeong, **via email at juwon0718@snu.ac.kr.**

Release
---------------
We released this repository to public. (2026-03-31)


