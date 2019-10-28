# Papers-for-domain-adaptation
This repository contains the papers that I've read and recommended for anyone else working in domain adaptation, especially in semantic segmentation.

# Feature Adaptation

[1] ICML2018, CyCADA: Cycle-Consistent Adversarial Domain Adaptation, Link: https://arxiv.org/abs/1711.03213.
Main features: This paper combines feature adaptation with pixel adaptation, using CycleGAN as an example for pixel adaptation. Note that in this paper, pixel adaptation only is better than feature adaptation only. 

(Pixel adaptation can be implemented by any paired or unpaired image generation network or style transfer network. The main idea is to transfer source image into one that is content-consistent with source image and style-consistent with target image.)

[2] CVPR2018, Learning to Adapt Structured Output Space for Semantic Segmentation, Link: https://arxiv.org/abs/1802.10349. Main features: This paper performs multi-scale feature adaptations on the hierarchical features extracted by a backbone. Note that one way to perform multi-scale feature adaptation is single scale input on multi feature like this paper, and another way is multi scale input on single feature. Please to Pix2pixHD for more details.

[3] CVPR2019, Taking A Closer Look at Domain Shift: Category-level Adversaries for Semantics Consistent Domain Adaptation. Link: https://arxiv.org/abs/1809.09478?context=cs. Main features: This paper modifies the main model with two classifiers. Training two classifiers simultaneously can make two different views on the features, so that the feature is more robust. And assigning different weights to the feature maps can fix the class imbalance problem to some extent, which is still a problem in domain adaptation for semantic segmentation.

# Pixel Adaptation

