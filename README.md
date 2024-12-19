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

# Conclusion:

-Lightweight architectures with attention mechanisms can efficiently handle small and imbalanced datasets.
-The SEBlock model provides the best trade-off between accuracy and computational efficiency.
