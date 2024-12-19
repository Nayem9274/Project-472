# Title: Lightweight Deep Learning Models for Histopathological Cancer Cell Classification
# Problem Statement:

-Develop lightweight models to classify histopathological cancer cells efficiently, addressing the challenges of small and imbalanced datasets.

-Use transfer learning and data augmentation to improve classification accuracy.

# Datasets:

-CRC-VAL-HE-7K: Contains 7180 colorectal cancer patches with 9 tissue classes.

-PathMNIST: 100K histological patches for pretraining.

# Proposed Models:

# 1. SEBlock Integration:
-Focus on channel-wise attention using Squeeze-and-Excitation (SE) blocks.

-Improves performance by recalibrating important feature channels.
# 2. MSFF Integration:
-Captures multi-scale spatial features through Adaptive Average Pooling.

-Balances local and global spatial information.
# 3. CBAM Integration:
-Combines channel and spatial attention for better feature refinement.

# Key Results:

-SEBlock Model achieved the best accuracy (98%) due to its simplicity and robust feature focus.

-MSFF and CBAM also performed well but showed variability in performance due to sensitivity to domain shifts and dataset size.

# Experimenting with original DeepCMorph and modified DeepCMorph model(classification module only):

- Added "Residual Blocks" to improve feature learning by preserving input information and mitigating the vanishing gradient problem.

- Added "Squeeze-and-Excitation (SE) Attention" for focusing on channel recalibration to boost important features.

- The updated DeepCMorph model demonstrates a significant performance boost due to the addition of residual blocks, SE attention.


# Conclusion:

-Lightweight architectures with attention mechanisms can efficiently handle small and imbalanced datasets.

-The SEBlock model provides the best trade-off between accuracy and computational efficiency.

# Description of notebooks:

In **A.ipynb**, we have 2 lightweight models (B0+SE & B0+MSFF) and experiment on them using the CRC-VAL-HE-7K and PathMNIST(CRC-100K) datasets. We did 4 experiments. They are: 1. Train and Test on CRC-VAL-HE-7K, 2. Train and Test on CRC-VAL-HE-7K (with augmentation), 3. Train and Test on PathMNIST dataset. 4. Train on PathMNIST+ Finetuning on CRC-VAL-HE-7K. Another model (B0+CBB) is on the second notebook(**B.ipynb**).

Finally, we did some experiment on the original model of the paper (DeepCMorph). This model has 2 modules: segmentation and classification module. For simplicity purpose, we worked with only the 'classification' module. We used the CRC-VAL-HE-7K for training and testing purpose. We then modified DeepCMorph Model by adding residual blocks and SE block (for attention purpose).

Experiment notes:

-We used cross-entropy/Focal loss.

-We used patience=5 for early stopping in order to avoid overfitting.
