# Papers-for-domain-adaptation
This repository contains the papers that I've read and recommended for anyone else working in domain adaptation, especially in semantic segmentation.

# Feature Adaptation

[1] ICML2018, CyCADA: Cycle-Consistent Adversarial Domain Adaptation, Link: https://arxiv.org/abs/1711.03213.
Main features: This paper combines feature adaptation with pixel adaptation, using CycleGAN as an example for pixel adaptation. Note that in this paper, pixel adaptation only is better than feature adaptation only. 

(Pixel adaptation can be implemented by any paired or unpaired image generation network or style transfer network. The main idea is to transfer source image into one that is content-consistent with source image and style-consistent with target image.)

[2] CVPR2018, Learning to Adapt Structured Output Space for Semantic Segmentation, Link: https://arxiv.org/abs/1802.10349. Main features: This paper performs multi-scale feature adaptations on the hierarchical features extracted by a backbone. Note that one way to perform multi-scale feature adaptation is single scale input on multi feature like this paper, and another way is multi scale input on single feature. Please refer to Pix2pixHD for more details.

[3] CVPR2019, Taking A Closer Look at Domain Shift: Category-level Adversaries for Semantics Consistent Domain Adaptation. Link: https://arxiv.org/abs/1809.09478?context=cs. Main features: This paper modifies the main model with two classifiers. Training two classifiers simultaneously can make two different views on the features, so that the feature is more robust. And assigning different weights to the feature maps can fix the class imbalance problem to some extent, which is still a problem in domain adaptation for semantic segmentation.

# Pixel Adaptation

[1] ECCV2016, Perceptual Losses for Real-Time Style Transfer and Super-Resolution. Link: https://arxiv.org/abs/1603.08155. Main features: This paper proposes a training loss using pretrained VGG16 network. Style-consistency can be ensured by L2-Distance of Gram Matrix on different feature maps, and Content-consistency can be ensured by L2-Distance of high-level feature maps. Simple but interpretable.

[2] CVPR2017, Image-to-Image Translation with Conditional Adversarial Networks. Link: https://arxiv.org/abs/1611.07004. Also named Pix2Pix, mainly doing paired iamge generation. You must know, unnecessary to introduce.

[3] ICCV2017, Unpaired Image-to-Image Translation using Cycle-Consistent Adversarial Networks. Link: https://arxiv.org/abs/1703.10593v4. Also named CycleGAN, doing unpaired image generation. You must know, uncessary to introduce.

[4] ECCV2018, Multimodal Unsupervised Image-to-Image Translation. Link: https://arxiv.org/abs/1804.04732. Main features: This paper decomposes an image into a style representation and a content representation, and then recontructs the image from the content representation and another style representation. Thus it can generate any style images by controlling the potential style representation.
