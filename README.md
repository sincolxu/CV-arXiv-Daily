# CV-arXiv-Daily

**分享计算机视觉每天的arXiv文章，主要集中在目标检测，单目标跟踪，多目标跟踪，人体行为识别，人体姿态估计与跟踪，行人重识别，模型搜索等。每周周末会将本周的Archive起来**

[2019-01-23~2019-01-26](2019/2019.01.23-2019.01.26.md)

[2019-01-28~2019-02-01](2019/2019.01.28-2019.02.01.md)

[2019-02-04~2019-02-08](2019/2019.02.04-2019.02.08.md)

[2019-02-11~2019-02-15](2019/2019.02.11-2019.02.15.md)

**2019-02-28**

[1] CVPR2019 Video Caption新文

论文题目：Spatio-Temporal Dynamics and Semantic Attribute Enriched Visual Encoding for Video Captioning

作者：Nayyer Aafaq, Naveed Akhtar, Wei Liu, Syed Zulqarnain Gilani, Ajmal Mian

论文链接：https://arxiv.org/abs/1902.10322

摘要: Automatic generation of video captions is a fundamental challenge in computer vision. Recent techniques typically employ a combination of Convolutional Neural Networks (CNNs) and Recursive Neural Networks (RNNs) for video captioning. These methods mainly focus on tailoring sequence learning through RNNs for better caption generation, whereas off-the-shelf visual features are borrowed from CNNs. We argue that careful designing of visual features for this task is equally important, and present a visual feature encoding technique to generate semantically rich captions using Gated Recurrent Units (GRUs). Our method embeds rich temporal dynamics in visual features by hierarchically applying Short Fourier Transform to CNN features of the whole video. It additionally derives high level semantics from an object detector to enrich the representation with spatial dynamics of the detected objects. The final representation is projected to a compact space and fed to a language model. By learning a relatively simple language model comprising two GRU layers, we establish new state-of-the-art on MSVD and MSR-VTT datasets for METEOR and ROUGE_L metrics.

[2] CVPR2019 弱监督语义分割新文

论文题目：FickleNet: Weakly and Semi-supervised Semantic Image Segmentation using Stochastic Inference

作者：Jungbeom Lee, Eunji Kim, Sungmin Lee, Jangho Lee, Sungroh Yoon

论文链接：https://arxiv.org/abs/1902.10421

摘要: The main obstacle to weakly supervised semantic image segmentation is the difficulty of obtaining pixel-level information from coarse image-level annotations. Most methods based on image-level annotations use localization maps obtained from the classifier, but these only focus on the small discriminative parts of objects and do not capture precise boundaries. FickleNet explores diverse combinations of locations on feature maps created by generic deep neural networks. It selects hidden units randomly and then uses them to obtain activation scores for image classification. FickleNet implicitly learns the coherence of each location in the feature maps, resulting in a localization map which identifies both discriminative and other parts of objects. The ensemble effects are obtained from a single network by selecting random hidden unit pairs, which means that a variety of localization maps are generated from a single image. Our approach does not require any additional training steps and only adds a simple layer to a standard convolutional neural network; nevertheless it outperforms recent comparable techniques on the Pascal VOC 2012 benchmark in both weakly and semi-supervised settings.

[3] CVPR2019 视频处理新文

论文题目：Single-frame Regularization for Temporally Stable CNNs

作者：Gabriel Eilertsen, Rafa? K. Mantiuk, Jonas Unger

论文链接：https://arxiv.org/abs/1902.10424

摘要: Convolutional neural networks (CNNs) can model complicated non-linear relations between images. However, they are notoriously sensitive to small changes in the input. Most CNNs trained to describe image-to-image mappings generate temporally unstable results when applied to video sequences, leading to flickering artifacts and other inconsistencies over time. In order to use CNNs for video material, previous methods have relied on estimating dense frame-to-frame motion information (optical flow) in the training and/or the inference phase, or by exploring recurrent learning structures. We take a different approach to the problem, posing temporal stability as a regularization of the cost function. The regularization is formulated to account for different types of motion that can occur between frames, so that temporally stable CNNs can be trained without the need for video material or expensive motion estimation. The training can be performed as a fine-tuning operation, without architectural modifications of the CNN. Our evaluation shows that the training strategy leads to large improvements in temporal smoothness. Moreover, in situations where the quantity of training data is limited, the regularization can help in boosting the generalization performance to a much larger extent than what is possible with na?ve augmentation strategies.

[4] CVPR2019 多视几何新文

论文题目：Recurrent MVSNet for High-resolution Multi-view Stereo Depth Inference

作者：Yao Yao, Zixin Luo, Shiwei Li, Tianwei Shen, Tian Fang, Long Quan

论文链接：https://arxiv.org/abs/1902.10556

代码链接：https://github.com/YoYo000/MVSNet

摘要: Deep learning has recently demonstrated its excellent performance for multi-view stereo (MVS). However, one major limitation of current learned MVS approaches is the scalability: the memory-consuming cost volume regularization makes the learned MVS hard to be applied to high-resolution scenes. In this paper, we introduce a scalable multi-view stereo framework based on the recurrent neural network. Instead of regularizing the entire 3D cost volume in one go, the proposed Recurrent Multi-view Stereo Network (R-MVSNet) sequentially regularizes the 2D cost maps along the depth direction via the gated recurrent unit (GRU). This reduces dramatically the memory consumption and makes high-resolution reconstruction feasible. We first show the state-of-the-art performance achieved by the proposed R-MVSNet on the recent MVS benchmarks. Then, we further demonstrate the scalability of the proposed method on several large-scale scenarios, where previous learned approaches often fail due to the memory constraint. 

[5] CVPR2019 Video Classification新文

论文题目：Efficient Video Classification Using Fewer Frames

作者：Shweta Bhardwaj, Mukundhan Srinivasan, Mitesh M. Khapra

论文链接：https://arxiv.org/abs/1902.10640

摘要: Recently,there has been a lot of interest in building compact models for video classification which have a small memory footprint (<1 GB). While these models are compact, they typically operate by repeated application of a small weight matrix to all the frames in a video. E.g. recurrent neural network based methods compute a hidden state for every frame of the video using a recurrent weight matrix. Similarly, cluster-and-aggregate based methods such as NetVLAD, have a learnable clustering matrix which is used to assign soft-clusters to every frame in the video. Since these models look at every frame in the video, the number of floating point operations (FLOPs) is still large even though the memory footprint is small. We focus on building compute-efficient video classification models which process fewer frames and hence have less number of FLOPs. Similar to memory efficient models, we use the idea of distillation albeit in a different setting. Specifically, in our case, a compute-heavy teacher which looks at all the frames in the video is used to train a compute-efficient student which looks at only a small fraction of frames in the video. This is in contrast to a typical memory efficient Teacher-Student setting, wherein both the teacher and the student look at all the frames in the video but the student has fewer parameters. Our work thus complements the research on memory efficient video classification. We do an extensive evaluation with three types of models for video classification,viz.(i) recurrent models (ii) cluster-and-aggregate models and (iii) memory-efficient cluster-and-aggregate models and show that in each of these cases, a see-it-all teacher can be used to train a compute efficient see-very-little student. We show that the proposed student network can reduce the inference time by 30% and the number of FLOPs by approximately 90% with a negligible drop in the performance.

**2019-02-27**

[1] CVPR2019 检测新文

论文题目：Generalized Intersection over Union: A Metric and A Loss for Bounding Box Regression

作者：Hamid Rezatofighi, Nathan Tsoi, JunYoung Gwak, Amir Sadeghian, Ian Reid, Silvio Savarese

论文链接：https://arxiv.org/abs/1902.09630

摘要: Intersection over Union (IoU) is the most popular evaluation metric used in the object detection benchmarks. However, there is a gap between optimizing the commonly used distance losses for regressing the parameters of a bounding box and maximizing this metric value. The optimal objective for a metric is the metric itself. In the case of axis-aligned 2D bounding boxes, it can be shown that IoU can be directly used as a regression loss. However, IoU has a plateau making it infeasible to optimize in the case of non-overlapping bounding boxes. In this paper, we address the weaknesses of IoU by introducing a generalized version as both a new loss and a new metric. By incorporating this generalized IoU (GIoU) as a loss into the state-of-the art object detection frameworks, we show a consistent improvement on their performance using both the standard, IoU based, and new, GIoU based, performance measures on popular object detection benchmarks such as PASCAL VOC and MS COCO.

[2] CVPR2019 分类新文

论文题目：Learning a Deep ConvNet for Multi-label Classification with Partial Labels

作者：Thibaut Durand, Nazanin Mehrasa, Greg Mori

论文链接：https://arxiv.org/abs/1902.09720

摘要: Deep ConvNets have shown great performance for single-label image classification (e.g. ImageNet), but it is necessary to move beyond the single-label classification task because pictures of everyday life are inherently multi-label. Multi-label classification is a more difficult task than single-label classification because both the input images and output label spaces are more complex. Furthermore, collecting clean multi-label annotations is more difficult to scale-up than single-label annotations. To reduce the annotation cost, we propose to train a model with partial labels i.e. only some labels are known per image. We first empirically compare different labeling strategies to show the potential for using partial labels on multi-label datasets. Then to learn with partial labels, we introduce a new classification loss that exploits the proportion of known labels per example. Our approach allows the use of the same training settings as when learning with all the annotations. We further explore several curriculum learning based strategies to predict missing labels. Experiments are performed on three large-scale multi-label datasets: MS COCO, NUS-WIDE and Open Images.

[3] CVPR2019 3D detection新文

论文题目：Stereo R-CNN based 3D Object Detection for Autonomous Driving

作者：Peiliang Li, Xiaozhi Chen, Shaojie Shen

论文链接：https://arxiv.org/abs/1902.09738

摘要: We propose a 3D object detection method for autonomous driving by fully exploiting the sparse and dense, semantic and geometry information in stereo imagery. Our method, called Stereo R-CNN, extends Faster R-CNN for stereo inputs to simultaneously detect and associate object in left and right images. We add extra branches after stereo Region Proposal Network (RPN) to predict sparse keypoints, viewpoints, and object dimensions, which are combined with 2D left-right boxes to calculate a coarse 3D object bounding box. We then recover the accurate 3D bounding box by a region-based photometric alignment using left and right RoIs. Our method does not require depth input and 3D position supervision, however, outperforms all existing fully supervised image-based methods. Experiments on the challenging KITTI dataset show that our method outperforms the state-of-the-art stereo-based method by around 30% AP on both 3D detection and 3D localization tasks. Code will be made publicly available.

[4] CVPR2019 3D Reconstruction新文

论文题目：Single-Image Piece-wise Planar 3D Reconstruction via Associative Embedding

作者：Zehao Yu, Jia Zheng, Dongze Lian, Zihan Zhou, Shenghua Gao

论文链接：https://arxiv.org/abs/1902.09777

代码链接：https://github.com/svip-lab/PlanarReconstruction

摘要: Single-image piece-wise planar 3D reconstruction aims to simultaneously segment plane instances and recover 3D plane parameters from an image. Most recent approaches leverage convolutional neural networks (CNNs) and achieve promising results. However, these methods are limited to detecting a fixed number of planes with certain learned order. To tackle this problem, we propose a novel two-stage method based on associative embedding, inspired by its recent success in instance segmentation. In the first stage, we train a CNN to map each pixel to an embedding space where pixels from the same plane instance have similar embeddings. Then, the plane instances are obtained by grouping the embedding vectors in planar regions via an efficient mean shift clustering algorithm. In the second stage, we estimate the parameter for each plane instance by considering both pixel-level and instance-level consistencies. With the proposed method, we are able to detect an arbitrary number of planes. Extensive experiments on public datasets validate the effectiveness and efficiency of our method. Furthermore, our method runs at 30 fps at the testing time, thus could facilitate many real-time applications such as visual SLAM and human-robot interaction.

[5] CVPR2019 点云分割新文

论文题目：Associatively Segmenting Instances and Semantics in Point Clouds

作者：Xinlong Wang, Shu Liu, Xiaoyong Shen, Chunhua Shen, Jiaya Jia

论文链接：https://arxiv.org/abs/1902.09852

代码链接：https://github.com/WXinlong/ASIS

摘要: A 3D point cloud describes the real scene precisely and intuitively.To date how to segment diversified elements in such an informative 3D scene is rarely discussed. In this paper, we first introduce a simple and flexible framework to segment instances and semantics in point clouds simultaneously. Then, we propose two approaches which make the two tasks take advantage of each other, leading to a win-win situation. Specifically, we make instance segmentation benefit from semantic segmentation through learning semantic-aware point-level instance embedding. Meanwhile, semantic features of the points belonging to the same instance are fused together to make more accurate per-point semantic predictions. Our method largely outperforms the state-of-the-art method in 3D instance segmentation along with a significant improvement in 3D semantic segmentation.

[6] CVPR2019 3D Human Pose Estimation新文

论文题目：RepNet: Weakly Supervised Training of an Adversarial Reprojection Network for 3D Human Pose Estimation

作者：Bastian Wandt, Bodo Rosenhahn

论文链接：https://arxiv.org/abs/1902.09868

摘要: This paper addresses the problem of 3D human pose estimation from single images. While for a long time human skeletons were parameterized and fitted to the observation by satisfying a reprojection error, nowadays researchers directly use neural networks to infer the 3D pose from the observations. However, most of these approaches ignore the fact that a reprojection constraint has to be satisfied and are sensitive to overfitting. We tackle the overfitting problem by ignoring 2D to 3D correspondences. This efficiently avoids a simple memorization of the training data and allows for a weakly supervised training. One part of the proposed reprojection network (RepNet) learns a mapping from a distribution of 2D poses to a distribution of 3D poses using an adversarial training approach. Another part of the network estimates the camera. This allows for the definition of a network layer that performs the reprojection of the estimated 3D pose back to 2D which results in a reprojection loss function. Our experiments show that RepNet generalizes well to unknown data and outperforms state-of-the-art methods when applied to unseen data. Moreover, our implementation runs in real-time on a standard desktop PC.

[7] CVPR2019 3D Face新文

论文题目：Disentangled Representation Learning for 3D Face Shape

作者：Zi-Hang Jiang, Qianyi Wu, Keyu Chen, Juyong Zhang

论文链接：https://arxiv.org/abs/1902.09887

摘要: In this paper, we present a novel strategy to design disentangled 3D face shape representation. Specifically, a given 3D face shape is decomposed into identity part and expression part, which are both encoded and decoded in a nonlinear way. To solve this problem, we propose an attribute decomposition framework for 3D face mesh. To better represent face shapes which are usually nonlinear deformed between each other, the face shapes are represented by a vertex based deformation representation rather than Euclidean coordinates. The experimental results demonstrate that our method has better performance than existing methods on decomposing the identity and expression parts. Moreover, more natural expression transfer results can be achieved with our method than existing methods.

**2019-02-26**

[1] CVPR 2019 Pose estimation文章，目前SOTA,已经开源

论文题目：Deep High-Resolution Representation Learning for Human Pose Estimation

作者：Ke Sun, Bin Xiao, Dong Liu, Jingdong Wang

论文链接：https://arxiv.org/abs/1902.09212

代码链接：https://github.com/leoxiaobin/deep-high-resolution-net.pytorch

摘要: This is an official pytorch implementation of Deep High-Resolution Representation Learning for Human Pose Estimation. In this work, we are interested in the human pose estimation problem with a focus on learning reliable high-resolution representations. Most existing methods recover high-resolution representations from low-resolution representations produced by a high-to-low resolution network. Instead, our proposed network maintains high-resolution representations through the whole process. We start from a high-resolution subnetwork as the first stage, gradually add high-to-low resolution subnetworks one by one to form more stages, and connect the mutli-resolution subnetworks in parallel. We conduct repeated multi-scale fusions such that each of the high-to-low resolution representations receives information from other parallel representations over and over, leading to rich high-resolution representations. As a result, the predicted keypoint heatmap is potentially more accurate and spatially more precise. We empirically demonstrate the effectiveness of our network through the superior pose estimation results over two benchmark datasets: the COCO keypoint detection dataset and the MPII Human Pose dataset.

[2] CVPR2019 VOS文章

论文题目：FEELVOS: Fast End-to-End Embedding Learning for Video Object Segmentation

作者：Paul Voigtlaender, Yuning Chai, Florian Schroff, Hartwig Adam, Bastian Leibe, Liang-Chieh Chen

论文链接：https://arxiv.org/abs/1902.09513

摘要: Many of the recent successful methods for video object segmentation (VOS) are overly complicated, heavily rely on fine-tuning on the first frame, and/or are slow, and are hence of limited practical use. In this work, we propose FEELVOS as a simple and fast method which does not rely on fine-tuning. In order to segment a video, for each frame FEELVOS uses a semantic pixel-wise embedding together with a global and a local matching mechanism to transfer information from the first frame and from the previous frame of the video to the current frame. In contrast to previous work, our embedding is only used as an internal guidance of a convolutional network. Our novel dynamic segmentation head allows us to train the network, including the embedding, end-to-end for the multiple object segmentation task with a cross entropy loss. We achieve a new state of the art in video object segmentation without fine-tuning on the DAVIS 2017 validation set with a J&F measure of 69.1%.

[3] U-Net+

论文题目：U-NetPlus: A Modified Encoder-Decoder U-Net Architecture for Semantic and Instance Segmentation of Surgical Instrument

作者：S. M. Kamrul Hasan, Cristian A. Linte

论文链接：https://arxiv.org/abs/1902.08994

摘要: Conventional therapy approaches limit surgeons' dexterity control due to limited field-of-view. With the advent of robot-assisted surgery, there has been a paradigm shift in medical technology for minimally invasive surgery. However, it is very challenging to track the position of the surgical instruments in a surgical scene, and accurate detection & identification of surgical tools is paramount. Deep learning-based semantic segmentation in frames of surgery videos has the potential to facilitate this task. In this work, we modify the U-Net architecture named U-NetPlus, by introducing a pre-trained encoder and re-design the decoder part, by replacing the transposed convolution operation with an upsampling operation based on nearest-neighbor (NN) interpolation. To further improve performance, we also employ a very fast and flexible data augmentation technique. We trained the framework on 8 x 225 frame sequences of robotic surgical videos, available through the MICCAI 2017 EndoVis Challenge dataset and tested it on 8 x 75 frame and 2 x 300 frame videos. Using our U-NetPlus architecture, we report a 90.20% DICE for binary segmentation, 76.26% DICE for instrument part segmentation, and 46.07% for instrument type (i.e., all instruments) segmentation, outperforming the results of previous techniques implemented and tested on these data.

[4] Pedestrian Detection文章

论文题目：SSA-CNN: Semantic Self-Attention CNN for Pedestrian Detection

作者：Chengju Zhou, Meiqing Wu, Siew-Kei Lam

论文链接：https://arxiv.org/abs/1902.09080

摘要: Pedestrian detection plays an important role in many applications such as autonomous driving. We propose a method that explores semantic segmentation results as self-attention cues to significantly improve the pedestrian detection performance. Specifically, a multi-task network is designed to jointly learn semantic segmentation and pedestrian detection from image datasets with weak box-wise annotations. The semantic segmentation feature maps are concatenated with corresponding convolution features maps to provide more discriminative features for pedestrian detection and pedestrian classification. By jointly learning segmentation and detection, our proposed pedestrian self-attention mechanism can effectively identify pedestrian regions and suppress backgrounds. In addition, we propose to incorporate semantic attention information from multi-scale layers into deep convolution neural network to boost pedestrian detection. Experiment results show that the proposed method achieves the best detection performance with MR of 6.27% on Caltech dataset and obtain competitive performance on CityPersons dataset while maintaining high computational efficiency.

[5] ICRA2019 机器人Ego-Motion Estimation文章

论文题目：Beyond Photometric Loss for Self-Supervised Ego-Motion Estimation

作者：Tianwei Shen, Zixin Luo, Lei Zhou, Hanyu Deng, Runze Zhang, Tian Fang, Long Quan

论文链接：https://arxiv.org/abs/1902.09103

代码链接：https://github.com/hlzz/DeepMatchVO

摘要: Accurate relative pose is one of the key components in visual odometry (VO) and simultaneous localization and mapping (SLAM). Recently, the self-supervised learning framework that jointly optimizes the relative pose and target image depth has attracted the attention of the community. Previous works rely on the photometric error generated from depths and poses between adjacent frames, which contains large systematic error under realistic scenes due to reflective surfaces and occlusions. In this paper, we bridge the gap between geometric loss and photometric loss by introducing the matching loss constrained by epipolar geometry in a self-supervised framework. Evaluated on the KITTI dataset, our method outperforms the state-of-the-art unsupervised ego-motion estimation methods by a large margin.

[6] Semantic Edge Detection文章

论文题目：Dynamic Feature Fusion for Semantic Edge Detection

作者：Yuan Hu, Yunpeng Chen, Xiang Li, Jiashi Feng

论文链接：https://arxiv.org/abs/1902.09104

摘要: Features from multiple scales can greatly benefit the semantic edge detection task if they are well fused. However, the prevalent semantic edge detection methods apply a fixed weight fusion strategy where images with different semantics are forced to share the same weights, resulting in universal fusion weights for all images and locations regardless of their different semantics or local context. In this work, we propose a novel dynamic feature fusion strategy that assigns different fusion weights for different input images and locations adaptively. This is achieved by a proposed weight learner to infer proper fusion weights over multi-level features for each location of the feature map, conditioned on the specific input. In this way, the heterogeneity in contributions made by different locations of feature maps and input images can be better considered and thus help produce more accurate and sharper edge predictions. We show that our model with the novel dynamic feature fusion is superior to fixed weight fusion and also the naïve location-invariant weight fusion methods, via comprehensive experiments on benchmarks Cityscapes and SBD. In particular, our method outperforms all existing well established methods and achieves new state-of-the-art.

[7] CVPR2019 Action Recognition文章

论文题目：An Attention Enhanced Graph Convolutional LSTM Network for Skeleton-Based Action Recognition

作者：Chenyang Si, Wentao Chen, Wei Wang, Liang Wang, Tieniu Tan

论文链接：https://arxiv.org/abs/1902.09130

摘要: Skeleton-based action recognition is an important task that requires the adequate understanding of movement characteristics of a human action from the given skeleton sequence. Recent studies have shown that exploring spatial and temporal features of the skeleton sequence is vital for this task. Nevertheless, how to effectively extract discriminative spatial and temporal features is still a challenging problem. In this paper, we propose a novel Attention Enhanced Graph Convolutional LSTM Network (AGC-LSTM) for human action recognition from skeleton data. The proposed AGC-LSTM can not only capture discriminative features in spatial configuration and temporal dynamics but also explore the co-occurrence relationship between spatial and temporal domains. We also present a temporal hierarchical architecture to increases temporal receptive fields of the top AGC-LSTM layer, which boosts the ability to learn the high-level semantic representation and significantly reduces the computation cost. Furthermore, to select discriminative spatial information, the attention mechanism is employed to enhance information of key joints in each AGC-LSTM layer. Experimental results on two datasets are provided: NTU RGB+D dataset and Northwestern-UCLA dataset. The comparison results demonstrate the effectiveness of our approach and show that our approach outperforms the state-of-the-art methods on both datasets.

[8] AAAI2019 Optical Flow文章

论文题目：DDFlow: Learning Optical Flow with Unlabeled Data Distillation

作者：Pengpeng Liu, Irwin King, Michael R.Lyu, Jia Xu

论文链接：https://arxiv.org/abs/1902.09145

摘要: We present DDFlow, a data distillation approach to learning optical flow estimation from unlabeled data. The approach distills reliable predictions from a teacher network, and uses these predictions as annotations to guide a student network to learn optical flow. Unlike existing work relying on hand-crafted energy terms to handle occlusion, our approach is data-driven, and learns optical flow for occluded pixels. This enables us to train our model with a much simpler loss function, and achieve a much higher accuracy. We conduct a rigorous evaluation on the challenging Flying Chairs, MPI Sintel, KITTI 2012 and 2015 benchmarks, and show that our approach significantly outperforms all existing unsupervised learning methods, while running at real time.


[9] RGB to Mech 文章

论文题目：End-to-end Hand Mesh Recovery from a Monocular RGB Image

作者：Xiong Zhang, Qiang Li, Wenbo Zhang, Wen Zheng

论文链接：https://arxiv.org/abs/1902.09305

代码链接：https://github.com/MandyMo/HAMR

摘要: In this paper, we present a HAnd Mesh Recovery (HAMR) framework to tackle the problem of reconstructing the full 3D mesh of a human hand from a single RGB image. In contrast to existing research on 2D or 3D hand pose estimation from RGB or/and depth image data, HAMR can provide a more expressive and useful mesh representation for monocular hand image understanding. In particular, the mesh representation is achieved by parameterizing a generic 3D hand model with shape and relative 3D joint angles. By utilizing this mesh representation, we can easily compute the 3D joint locations via linear interpolations between the vertexes of the mesh, while obtain the 2D joint locations with a projection of the 3D joints.

**2019-02-25**

[1] MOT文章

论文题目：Online Multi-Object Tracking with Instance-Aware Tracker and Dynamic Model Refreshment

作者：Peng Chu, Heng Fan, Chiu C Tan, Haibin Ling

论文链接：https://arxiv.org/abs/1902.08231

摘要: Recent progresses in model-free single object tracking (SOT) algorithms have largely inspired applying SOT to \emph{multi-object tracking} (MOT) to improve the robustness as well as relieving dependency on external detector. However, SOT algorithms are generally designed for distinguishing a target from its environment, and hence meet problems when a target is spatially mixed with similar objects as observed frequently in MOT. To address this issue, in this paper we propose an instance-aware tracker to integrate SOT techniques for MOT by encoding awareness both within and between target models. In particular, we construct each target model by fusing information for distinguishing target both from background and other instances (tracking targets). To conserve uniqueness of all target models, our instance-aware tracker considers response maps from all target models and assigns spatial locations exclusively to optimize the overall accuracy. Another contribution we make is a dynamic model refreshing strategy learned by a convolutional neural network. This strategy helps to eliminate initialization noise as well as to adapt to the variation of target size and appearance. To show the effectiveness of the proposed approach, it is evaluated on the popular MOT15 and MOT16 challenge benchmarks. On both benchmarks, our approach achieves the best overall performances in comparison with published results.

[2] 多路胶囊网络

论文题目：The Multi-Lane Capsule Network (MLCN)

作者：Vanderson Martins do Rosario, Edson Borin, Mauricio Breternitz Jr

论文链接：https://arxiv.org/abs/1902.08431

摘要: We introduce Multi-Lane Capsule Networks (MLCN), which are a separable and resource efficient organization of Capsule Networks (CapsNet) that allows parallel processing, while achieving high accuracy at reduced cost. A MLCN is composed of a number of (distinct) parallel lanes, each contributing to a dimension of the result, trained using the routing-by-agreement organization of CapsNet. Our results indicate similar accuracy with a much reduced cost in number of parameters for the Fashion-MNIST and Cifar10 datsets. They also indicate that the MLCN outperforms the original CapsNet when using a proposed novel configuration for the lanes. MLCN also has faster training and inference times, being more than two-fold faster than the original CapsNet in the same accelerator.

[3] ICLR 2019对抗网络鲁棒性文章

论文题目：On the Sensitivity of Adversarial Robustness to Input Data Distributions

作者：Gavin Weiguang Ding, Kry Yik Chau Lui, Xiaomeng Jin, Luyu Wang, Ruitong Huang

论文链接：https://arxiv.org/abs/1902.08336

摘要: Neural networks are vulnerable to small adversarial perturbations. Existing literature largely focused on understanding and mitigating the vulnerability of learned models. In this paper, we demonstrate an intriguing phenomenon about the most popular robust training method in the literature, adversarial training: Adversarial robustness, unlike clean accuracy, is sensitive to the input data distribution. Even a semantics-preserving transformations on the input data distribution can cause a significantly different robustness for the adversarial trained model that is both trained and evaluated on the new distribution. Our discovery of such sensitivity on data distribution is based on a study which disentangles the behaviors of clean accuracy and robust accuracy of the Bayes classifier. Empirical investigations further confirm our finding. We construct semantically-identical variants for MNIST and CIFAR10 respectively, and show that standardly trained models achieve comparable clean accuracies on them, but adversarially trained models achieve significantly different robustness accuracies. This counter-intuitive phenomenon indicates that input data distribution alone can affect the adversarial robustness of trained neural networks, not necessarily the tasks themselves. Lastly, we discuss the practical implications on evaluating adversarial robustness, and make initial attempts to understand this complex phenomenon.


**2019-02-22**

[1] 眨眼检测数据集

论文题目：Towards Real-time Eyeblink Detection in The Wild:Dataset,Theory and Practices

作者：Guilei Hu, Yang Xiao, Zhiguo Cao, Lubin Meng, Zhiwen Fang, Joey Tianyi Zhou

论文链接：https://arxiv.org/abs/1902.07891

摘要: Effective and real-time eyeblink detection is of wide-range applications, such as deception detection, drive fatigue detection, face anti-spoofing, etc. Although numerous of efforts have already been paid, most of them focus on addressing the eyeblink detection problem under the constrained indoor conditions with the relative consistent subject and environment setup. Nevertheless, towards the practical applications eyeblink detection in the wild is more required, and of greater challenges. However, to our knowledge this has not been well studied before. In this paper, we shed the light to this research topic. A labelled eyeblink in the wild dataset (i.e., HUST-LEBW) of 673 eyeblink video samples (i.e., 381 positives, and 292 negatives) is first established by us. These samples are captured from the unconstrained movies, with the dramatic variation on human attribute, human pose, illumination condition, imaging configuration, etc. Then, we formulate eyeblink detection task as a spatial-temporal pattern recognition problem. After locating and tracking human eye using SeetaFace engine and KCF tracker respectively, a modified LSTM model able to capture the multi-scale temporal information is proposed to execute eyeblink verification. A feature extraction approach that reveals appearance and motion characteristics simultaneously is also proposed. The experiments on HUST-LEBW reveal the superiority and efficiency of our approach. It also verifies that, the existing eyeblink detection methods cannot achieve satisfactory performance in the wild.

[2] GAN文章

论文题目：Domain Partitioning Network

作者：Botos Csaba, Adnane Boukhayma, Viveka Kulharia, András Horváth, Philip H. S. Torr

论文链接：https://arxiv.org/abs/1902.08134

摘要: Standard adversarial training involves two agents, namely a generator and a discriminator, playing a mini-max game. However, even if the players converge to an equilibrium, the generator may only recover a part of the target data distribution, in a situation commonly referred to as mode collapse. In this work, we present the Domain Partitioning Network (DoPaNet), a new approach to deal with mode collapse in generative adversarial learning. We employ multiple discriminators, each encouraging the generator to cover a different part of the target distribution. To ensure these parts do not overlap and collapse into the same mode, we add a classifier as a third agent in the game. The classifier decides which discriminator the generator is trained against for each sample. Through experiments on toy examples and real images, we show the merits of DoPaNet in covering the real distribution and its superiority with respect to the competing methods. Besides, we also show that we can control the modes from which samples are generated using DoPaNet.

[3] SLAM开源框架

论文题目：GSLAM: A General SLAM Framework and Benchmark

作者：Yong Zhao, Shibiao Xu, Shuhui Bu, Hongkai Jiang, Pengcheng Han

论文链接：https://arxiv.org/abs/1902.07995

摘要: SLAM technology has recently seen many successes and attracted the attention of high-technological companies. However, how to unify the interface of existing or emerging algorithms, and effectively perform benchmark about the speed, robustness and portability are still problems. In this paper, we propose a novel SLAM platform named GSLAM, which not only provides evaluation functionality, but also supplies useful toolkit for researchers to quickly develop their own SLAM systems. The core contribution of GSLAM is an universal, cross-platform and full open-source SLAM interface for both research and commercial usage, which is aimed to handle interactions with input dataset, SLAM implementation, visualization and applications in an unified framework. Through this platform, users can implement their own functions for better performance with plugin form and further boost the application to practical usage of the SLAM.

**2019-02-21**

[1] adversarial research toolbox using PyTorch

论文题目：advertorch v0.1: An Adversarial Robustness Toolbox based on PyTorch

作者：Gavin Weiguang Ding, Luyu Wang, Xiaomeng Jin

论文链接：https://arxiv.org/abs/1902.07623

代码链接：https://github.com/BorealisAI/advertorch

摘要: advertorch is a toolbox for adversarial robustness research. It contains various implementations for attacks, defenses and robust training methods. advertorch is built on PyTorch (Paszke et al., 2017), and leverages the advantages of the dynamic computational graph to provide concise and efficient reference implementations. The code is licensed under the LGPL license and is open sourced

[2] 实时语义分割文章

论文题目：An efficient solution for semantic segmentation: ShuffleNet V2 with atrous separable convolutions

作者：Sercan Türkmen, Janne Heikkilä

论文链接：https://arxiv.org/abs/1902.07476

摘要: Assigning a label to each pixel in an image, namely semantic segmentation, has been an important task in computer vision, and has applications in autonomous driving, robotic navigation, localization, and scene understanding. Fully convolutional neural networks have proved to be a successful solution for the task over the years but most of the work being done focuses primarily on accuracy. In this paper, we present a computationally efficient approach to semantic segmentation, meanwhile achieving a high mIOU, 70.33% on Cityscapes challenge. The network proposed is capable of running real-time on mobile devices. In addition, we make our code and model weights publicly available.

[3] 自适应感受野网络组件

论文题目：Spatially-Adaptive Filter Units for Compact and Efficient Deep Neural Networks

作者：Domen Tabernik, Matej Kristan, Aleš Leonardis

论文链接：https://arxiv.org/abs/1902.07474

摘要: Convolutional neural networks excel in a number of computer vision tasks. One of their most crucial architectural elements is the effective receptive field size, that has to be manually set to accommodate a specific task. Standard solutions involve large kernels, down/up-sampling and dilated convolutions. These require testing a variety of dilation and down/up-sampling factors and result in non-compact representations and excessive number of parameters. We address this issue by proposing a new convolution filter composed of displaced aggregation units (DAU). DAUs learn spatial displacements and adapt the receptive field sizes of individual convolution filters to a given problem, thus eliminating the need for hand-crafted modifications. DAUs provide a seamless substitution of convolutional filters in existing state-of-the-art architectures, which we demonstrate on AlexNet, ResNet50, ResNet101, DeepLab and SRN-DeblurNet. The benefits of this design are demonstrated on a variety of computer vision tasks and datasets, such as image classification (ILSVRC 2012), semantic segmentation (PASCAL VOC 2011, Cityscape) and blind image de-blurring (GOPRO). Results show that DAUs efficiently allocate parameters resulting in up to four times more compact networks at similar or better performance.

[4] AAAI-19 Action Recognition文章

论文题目：Learning Transferable Self-attentive Representations for Action Recognition in Untrimmed Videos with Weak Supervision

作者：Xiao-Yu Zhang, Haichao Shi, Changsheng Li, Kai Zheng, Xiaobin Zhu, Lixin Duan

论文链接：https://arxiv.org/abs/1902.07370

摘要: Action recognition in videos has attracted a lot of attention in the past decade. In order to learn robust models, previous methods usually assume videos are trimmed as short sequences and require ground-truth annotations of each video frame/sequence, which is quite costly and time-consuming. In this paper, given only video-level annotations, we propose a novel weakly supervised framework to simultaneously locate action frames as well as recognize actions in untrimmed videos. Our proposed framework consists of two major components. First, for action frame localization, we take advantage of the self-attention mechanism to weight each frame, such that the influence of background frames can be effectively eliminated. Second, considering that there are trimmed videos publicly available and also they contain useful information to leverage, we present an additional module to transfer the knowledge from trimmed videos for improving the classification performance in untrimmed ones. Extensive experiments are conducted on two benchmark datasets (i.e., THUMOS14 and ActivityNet1.3), and experimental results clearly corroborate the efficacy of our method.

[5] AAAI-19 Motion Prediction文章

论文题目：Human Motion Prediction via Learning Local Structure Representations and Temporal Dependencies

作者：Xiao Guo, Jongmoo Choi

论文链接：https://arxiv.org/abs/1902.07367

摘要: Human motion prediction from motion capture data is a classical problem in the computer vision, and conventional methods take the holistic human body as input. These methods ignore the fact that, in various human activities, different body components (limbs and the torso) have distinctive characteristics in terms of the moving pattern. In this paper, we argue local representations on different body components should be learned separately and, based on such idea, propose a network, Skeleton Network (SkelNet), for long-term human motion prediction. Specifically, at each time-step, local structure representations of input (human body) are obtained via SkelNet's branches of component-specific layers, then the shared layer uses local spatial representations to predict the future human pose. Our SkelNet is the first to use local structure representations for predicting the human motion. Then, for short-term human motion prediction, we propose the second network, named as Skeleton Temporal Network (Skel-TNet). Skel-TNet consists of three components: SkelNet and a Recurrent Neural Network, they have advantages in learning spatial and temporal dependencies for predicting human motion, respectively; a feed-forward network that outputs the final estimation. Our methods achieve promising results on the Human3.6M dataset and the CMU motion capture dataset.

[6] 针对小目标检测的数据增强方式

论文题目：Augmentation for small object detection

作者：Mate Kisantal, Zbigniew Wojna, Jakub Murawski, Jacek Naruniec, Kyunghyun Cho

论文链接：https://arxiv.org/abs/1902.07296

摘要: In recent years, object detection has experienced impressive progress. Despite these improvements, there is still a significant gap in the performance between the detection of small and large objects. We analyze the current state-of-the-art model, Mask-RCNN, on a challenging dataset, MS COCO. We show that the overlap between small ground-truth objects and the predicted anchors is much lower than the expected IoU threshold. We conjecture this is due to two factors; (1) only a few images are containing small objects, and (2) small objects do not appear enough even within each image containing them. We thus propose to oversample those images with small objects and augment each of those images by copy-pasting small objects many times. It allows us to trade off the quality of the detector on large objects with that on small objects. We evaluate different pasting augmentation strategies, and ultimately, we achieve 9.7\% relative improvement on the instance segmentation and 7.1\% on the object detection of small objects, compared to the current state of the art method on MS COCO.

**2019-02-20**

[1] 分割图像标注工具FreeLabel

论文题目：FreeLabel: A Publicly Available Annotation Tool based on Freehand Traces

作者：Philipe A. Dias, Zhou Shen, Amy Tabb, Henry Medeiros

论文链接：https://arxiv.org/abs/1902.06806

摘要: Large-scale annotation of image segmentation datasets is often prohibitively expensive, as it usually requires a huge number of worker hours to obtain high-quality results. Abundant and reliable data has been, however, crucial for the advances on image understanding tasks achieved by deep learning models. In this paper, we introduce FreeLabel, an intuitive open-source web interface that allows users to obtain high-quality segmentation masks with just a few freehand scribbles, in a matter of seconds. The efficacy of FreeLabel is quantitatively demonstrated by experimental results on the PASCAL dataset as well as on a dataset from the agricultural domain. Designed to benefit the computer vision community, FreeLabel can be used for both crowdsourced or private annotation and has a modular structure that can be easily adapted for any image dataset.


[2] 一分半钟训练AlexNet

论文题目：Optimizing Network Performance for Distributed DNN Training on GPU Clusters: ImageNet/AlexNet Training in 1.5 Minutes

作者：Peng Sun, Wansen Feng, Ruobing Han, Shengen Yan, Yonggang Wen

论文链接：https://arxiv.org/abs/1902.06855

摘要: It is important to scale out deep neural network (DNN) training for reducing model training time. The high communication overhead is one of the major performance bottlenecks for distributed DNN training across multiple GPUs. Our investigations have shown that popular open-source DNN systems could only achieve 2.5 speedup ratio on 64 GPUs connected by 56 Gbps network. To address this problem, we propose a communication backend named GradientFlow for distributed DNN training, and employ a set of network optimization techniques. First, we integrate ring-based allreduce, mixed-precision training, and computation/communication overlap into GradientFlow. Second, we propose lazy allreduce to improve network throughput by fusing multiple communication operations into a single one, and design coarse-grained sparse communication to reduce network traffic by only transmitting important gradient chunks. When training ImageNet/AlexNet on 512 GPUs, our approach achieves 410.2 speedup ratio and completes 95-epoch training in 1.5 minutes, which outperforms existing approaches.

[3] WIDER Face and Pedestrian Challenge 2018官方报告

论文题目：WIDER Face and Pedestrian Challenge 2018: Methods and Results

作者：Chen Change Loy等

论文链接：https://arxiv.org/abs/1902.06854

摘要: This paper presents a review of the 2018 WIDER Challenge on Face and Pedestrian. The challenge focuses on the problem of precise localization of human faces and bodies, and accurate association of identities. It comprises of three tracks: (i) WIDER Face which aims at soliciting new approaches to advance the state-of-the-art in face detection, (ii) WIDER Pedestrian which aims to find effective and efficient approaches to address the problem of pedestrian detection in unconstrained environments, and (iii) WIDER Person Search which presents an exciting challenge of searching persons across 192 movies. In total, 73 teams made valid submissions to the challenge tracks. We summarize the winning solutions for all three tracks. and present discussions on open problems and potential research directions in these topics.

[4] 人体部件检测文章

论文题目：Detector-in-Detector: Multi-Level Analysis for Human-Parts

作者：Xiaojie Li, Lu Yang, Qing Song, Fuqiang Zhou

论文链接：https://arxiv.org/abs/1902.07017

摘要: Vision-based person, hand or face detection approaches have achieved incredible success in recent years with the development of deep convolutional neural network (CNN). In this paper, we take the inherent correlation between the body and body parts into account and propose a new framework to boost up the detection performance of the multi-level objects. In particular, we adopt a region-based object detection structure with two carefully designed detectors to separately pay attention to the human body and body parts in a coarse-to-fine manner, which we call Detector-in-Detector network (DID-Net). The first detector is designed to detect human body, hand, and face. The second detector, based on the body detection results of the first detector, mainly focus on the detection of small hand and face inside each body. The framework is trained in an end-to-end way by optimizing a multi-task loss. Due to the lack of human body, face and hand detection dataset, we have collected and labeled a new large dataset named Human-Parts with 14,962 images and 106,879 annotations. Experiments show that our method can achieve excellent performance on Human-Parts.

**2019-02-19**

[1] 遥感图像目标检测

论文题目：R2-CNN: Fast Tiny Object Detection in Large-scale Remote Sensing Images

作者：Jiangmiao Pang, Cong Li, Jianping Shi, Zhihai Xu, Huajun Feng

论文链接：https://arxiv.org/abs/1902.06042

摘要: Recently, convolutional neural network has brought impressive improvements for object detection. However, detecting tiny objects in large-scale remote sensing images still remains challenging. Firstly, the extreme large input size makes existing object detection solutions too slow for practical use. Secondly, the massive and complex backgrounds cause serious false alarms. Moreover, the ultra tiny objects increase the difficulty of accurate detection. To tackle these problems, we propose a unified and self-reinforced network called R2-CNN: Remote sensing Region-based Convolutional Neural Network, composing of backbone Tiny-Net, intermediate global attention block, and final classifier and detector. Tiny-Net is a lightweight residual structure which enables fast and powerful features extraction from inputs. Global attention block is built upon Tiny-Net to inhibit false positives. Classifier is then used to predict the existence of target in each patch, and detector is followed to locate them accurately if available. The classifier and detector are mutually reinforced with end-to-end training, which further speed-up the process and avoid false alarms. Effectiveness of R2-CNN is validated on hundreds of GF-1 images and GF-2 images, which are 18000×18192 pixels, 2.0m resolution, and 27620×29200 pixels, 0.8m resolution respectively. Specifically, we can process a GF-1 image in 29.4s on Titian X just with single thread. According to our knowledge, no previous solution can detect tiny object on such huge remote sensing images gracefully. We believe that it is a significant step towards practical real-time remote sensing systems.

[2] TPAMI弱监督目标检测

论文题目：Min-Entropy Latent Model for Weakly Supervised Object Detection

作者：Fang Wan, Pengxu Wei, Zhenjun Han, Jianbin Jiao, Qixiang Ye

论文链接：https://arxiv.org/abs/1902.06057

摘要: Weakly supervised object detection is a challenging task when provided with image category supervision but required to learn, at the same time, object locations and object detectors. The inconsistency between the weak supervision and learning objectives introduces significant randomness to object locations and ambiguity to detectors. In this paper, a min-entropy latent model (MELM) is proposed for weakly supervised object detection. Min-entropy serves as a model to learn object locations and a metric to measure the randomness of object localization during learning. It aims to principally reduce the variance of learned instances and alleviate the ambiguity of detectors. MELM is decomposed into three components including proposal clique partition, object clique discovery, and object localization. MELM is optimized with a recurrent learning algorithm, which leverages continuation optimization to solve the challenging non-convexity problem. Experiments demonstrate that MELM significantly improves the performance of weakly supervised object detection, weakly supervised object localization, and image classification, against the state-of-the-art approaches.

[3] RES-SE-NET

论文题目：RES-SE-NET: Boosting Performance of Resnets by Enhancing Bridge-connections

作者：Varshaneya V, Balasubramanian S, Darshan Gera

论文链接：https://arxiv.org/abs/1902.06066

摘要: One of the ways to train deep neural networks effectively is to use residual connections. Residual connections can be classified as being either identity connections or bridge-connections with a reshaping convolution. Empirical observations on CIFAR-10 and CIFAR-100 datasets using a baseline Resnet model, with bridge-connections removed, have shown a significant reduction in accuracy. This reduction is due to lack of contribution, in the form of feature maps, by the bridge-connections. Hence bridge-connections are vital for Resnet. However, all feature maps in the bridge-connections are considered to be equally important. In this work, an upgraded architecture "Res-SE-Net" is proposed to further strengthen the contribution from the bridge-connections by quantifying the importance of each feature map and weighting them accordingly using Squeeze-and-Excitation (SE) block. It is demonstrated that Res-SE-Net generalizes much better than Resnet and SE-Resnet on the benchmark CIFAR-10 and CIFAR-100 datasets.

[4] 超分辨率综述

论文题目：Deep Learning for Image Super-resolution: A Survey

作者：Zhihao Wang, Jian Chen, Steven C.H. Hoi

论文链接：https://arxiv.org/abs/1902.06068

摘要: Image Super-Resolution (SR) is an important class of image processing techniques to enhance the resolution of images and videos in computer vision. Recent years have witnessed remarkable progress of image super-resolution using deep learning techniques. In this survey, we aim to give a survey on recent advances of image super-resolution techniques using deep learning approaches in a systematic way. In general, we can roughly group the existing studies of SR techniques into three major categories: supervised SR, unsupervised SR, and domain-specific SR. In addition, we also cover some other important issues, such as publicly available benchmark datasets and performance evaluation metrics. Finally, we conclude this survey by highlighting several future directions and open issues which should be further addressed by the community in the future.

[5] 遥感图像理解数据集

论文题目：BigEarthNet: A Large-Scale Benchmark Archive For Remote Sensing Image Understanding

作者：Gencer Sumbul, Marcela Charfuelan, Begüm Demir, Volker Markl

论文链接：https://arxiv.org/abs/1902.06148

摘要: This paper presents a new large-scale multi-label Sentinel-2 benchmark archive, named BigEarthNet. Our archive consists of 590,326 Sentinel-2 image patches, each of which has 10, 20 and 60 meter image bands associated to the pixel sizes of 120x120, 60x60 and 20x20, respectively. Unlike most of the existing archives, each image patch is annotated by multiple land-cover classes (i.e., multi-labels) that are provided from the CORINE Land Cover database of the year 2018 (CLC 2018). The BigEarthNet is 20 times larger than the existing archives in remote sensing (RS) and thus is much more convenient to be used as a training source in the context of deep learning. This paper first addresses the limitations of the existing archives and then describes properties of our archive. Experimental results obtained in the framework of RS image scene classification problems show that a shallow Convolutional Neural Network (CNN) architecture trained on the BigEarthNet provides very high accuracy compared to a state-of-the-art CNN model pre-trained on the ImageNet (which is a very popular large-scale benchmark archive in computer vision). The BigEarthNet opens up promising directions to advance operational RS applications and research in massive Sentinel-2 image archives.

[6] 无监督学习综述

论文题目：Self-supervised Visual Feature Learning with Deep Neural Networks: A Survey

作者：Longlong Jing, Yingli Tian

论文链接：https://arxiv.org/abs/1902.06162

摘要: Large-scale labeled data are generally required to train deep neural networks in order to obtain better performance in visual feature learning from images or videos for computer vision applications. To avoid extensive cost of collecting and annotating large-scale datasets, as a subset of unsupervised learning methods, self-supervised learning methods are proposed to learn general image and video features from large-scale unlabeled data without using any human-annotated labels. This paper provides an extensive review of deep learning-based self-supervised general visual feature learning methods from images or videos. First, the motivation, general pipeline, and terminologies of this field are described. Then the common deep neural network architectures that used for self-supervised learning are summarized. Next, the main components and evaluation metrics of self-supervised learning methods are reviewed followed by the commonly used image and video datasets and the existing self-supervised visual feature learning methods. Finally, quantitative performance comparisons of the reviewed methods on benchmark datasets are summarized and discussed for both image and video feature learning. At last, this paper is concluded and lists a set of promising future directions for self-supervised visual feature learning.

[7] Image attribute transfer文章

论文题目：Fully-Featured Attribute Transfer

作者：De Xie, Muli Yang, Cheng Deng, Wei Liu, Dacheng Tao

论文链接：https://arxiv.org/abs/1902.06258

摘要: Image attribute transfer aims to change an input image to a target one with expected attributes, which has received significant attention in recent years. However, most of the existing methods lack the ability to de-correlate the target attributes and irrelevant information, i.e., the other attributes and background information, thus often suffering from blurs and artifacts. To address these issues, we propose a novel Attribute Manifold Encoding GAN (AME-GAN) for fully-featured attribute transfer, which can modify and adjust every detail in the images. Specifically, our method divides the input image into image attribute part and image background part on manifolds, which are controlled by attribute latent variables and background latent variables respectively. Through enforcing attribute latent variables to Gaussian distributions and background latent variables to uniform distributions respectively, the attribute transfer procedure becomes controllable and image generation is more photo-realistic. Furthermore, we adopt a conditional multi-scale discriminator to render accurate and high-quality target attribute images. Experimental results on three popular datasets demonstrate the superiority of our proposed method in both performances of the attribute transfer and image generation quality.

[8] 机器人视觉伺服文章

论文题目：DIViS: Domain Invariant Visual Servoing for Collision-Free Goal Reaching

作者：Fereshteh Sadeghi

论文链接：https://arxiv.org/abs/1902.05947

摘要: Robots should understand both semantics and physics to be functional in the real world. While robot platforms provide means for interacting with the physical world they cannot autonomously acquire object-level semantics without needing human. In this paper, we investigate how to minimize human effort and intervention to teach robots perform real world tasks that incorporate semantics. We study this question in the context of visual servoing of mobile robots and propose DIViS, a Domain Invariant policy learning approach for collision free Visual Servoing. DIViS incorporates high level semantics from previously collected static human-labeled datasets and learns collision free servoing entirely in simulation and without any real robot data. However, DIViS can directly be deployed on a real robot and is capable of servoing to the user-specified object categories while avoiding collisions in the real world. DIViS is not constrained to be queried by the final view of goal but rather is robust to servo to image goals taken from initial robot view with high occlusions without this impairing its ability to maintain a collision free path. We show the generalization capability of DIViS on real mobile robots in more than 90 real world test scenarios with various unseen object goals in unstructured environments. DIViS is compared to prior approaches via real world experiments and rigorous tests in simulation. 

**2019-02-18**

[1] Lipschitz GAN

论文题目：Lipschitz Generative Adversarial Nets

作者：Zhiming Zhou, Jiadong Liang, Yuxuan Song, Lantao Yu, Hongwei Wang, Weinan Zhang, Yong Yu, Zhihua Zhang

论文链接：https://arxiv.org/abs/1902.05687

摘要: In this paper we study the convergence of generative adversarial networks (GANs) from the perspective of the informativeness of the gradient of the optimal discriminative function. We show that GANs without restriction on the discriminative function space commonly suffer from the problem that the gradient produced by the discriminator is uninformative to guide the generator. By contrast, Wasserstein GAN (WGAN), where the discriminative function is restricted to 1-Lipschitz, does not suffer from such a gradient uninformativeness problem. We further show in the paper that the model with a compact dual form of Wasserstein distance, where the Lipschitz condition is relaxed, also suffers from this issue. This implies the importance of Lipschitz condition and motivates us to study the general formulation of GANs with Lipschitz constraint, which leads to a new family of GANs that we call Lipschitz GANs (LGANs). We show that LGANs guarantee the existence and uniqueness of the optimal discriminative function as well as the existence of a unique Nash equilibrium. We prove that LGANs are generally capable of eliminating the gradient uninformativeness problem. According to our empirical analysis, LGANs are more stable and generate consistently higher quality samples compared with WGAN.

[2] 医学图像分析综述

论文题目：Going Deep in Medical Image Analysis: Concepts, Methods, Challenges and Future Directions

作者：Fouzia Altaf, Syed M. S. Islam, Naveed Akhtar, Naeem K. Janjua

论文链接：https://arxiv.org/abs/1902.05655

摘要: Medical Image Analysis is currently experiencing a paradigm shift due to Deep Learning. This technology has recently attracted so much interest of the Medical Imaging community that it led to a specialized conference in `Medical Imaging with Deep Learning' in the year 2018. This article surveys the recent developments in this direction, and provides a critical review of the related major aspects. We organize the reviewed literature according to the underlying Pattern Recognition tasks, and further sub-categorize it following a taxonomy based on human anatomy. This article does not assume prior knowledge of Deep Learning and makes a significant contribution in explaining the core Deep Learning concepts to the non-experts in the Medical community. Unique to this study is the Computer Vision/Machine Learning perspective taken on the advances of Deep Learning in Medical Imaging. This enables us to single out `lack of appropriately annotated large-scale datasets' as the core challenge (among other challenges) in this research direction. We draw on the insights from the sister research fields of Computer Vision, Pattern Recognition and Machine Learning etc.; where the techniques of dealing with such challenges have already matured, to provide promising directions for the Medical Imaging community to fully harness Deep Learning in the future.

[3] 街景异常事件检测数据集

论文题目：Street Scene: A new dataset and evaluation protocol for video anomaly detection

作者：Barathkumar Ramachandra, Michael Jones

论文链接：https://arxiv.org/abs/1902.05872

摘要: Progress in video anomaly detection research is currently slowed by small datasets that lack a wide variety of activities as well as flawed evaluation criteria. This paper aims to help move this research effort forward by introducing a large and varied new dataset called Street Scene, as well as two new evaluation criteria that provide a better estimate of how an algorithm will perform in practice. In addition to the new dataset and evaluation criteria, we present two variations of a novel baseline video anomaly detection algorithm and show they are much more accurate on Street Scene than two state-of-the-art algorithms from the literature.

[4] 超分辨率文章

论文题目：Lightweight Feature Fusion Network for Single Image Super-Resolution

作者：Wenming Yang, Wei Wang, Xuechen Zhang, Shuifa Sun, Qingmin Liao

论文链接：https://arxiv.org/abs/1902.05694

摘要: Single image super-resolution(SISR) has witnessed great progress as convolutional neural network(CNN) gets deeper and wider. However, enormous parameters hinder its application to real world problems. In this letter, We propose a lightweight feature fusion network (LFFN) that can fully explore multi-scale contextual information and greatly reduce network parameters while maximizing SISR results. LFFN is built on spindle blocks and a softmax feature fusion module (SFFM). Specifically, a spindle block is composed of a dimension extension unit, a feature exploration unit and a feature refinement unit. The dimension extension layer expands low dimension to high dimension and implicitly learns the feature maps which is suitable for the next unit. The feature exploration unit performs linear and nonlinear feature exploration aimed at different feature maps. The feature refinement layer is used to fuse and refine features. SFFM fuses the features from different modules in a self-adaptive learning manner with softmax function, making full use of hierarchical information with a small amount of parameter cost. Both qualitative and quantitative experiments on benchmark datasets show that LFFN achieves favorable performance against state-of-the-art methods with similar parameters.

[5] VQA文章

论文题目：Cycle-Consistency for Robust Visual Question Answering

作者：Meet Shah, Xinlei Chen, Marcus Rohrbach, Devi Parikh

论文链接：https://arxiv.org/abs/1902.05660

摘要: Despite significant progress in Visual Question Answering over the years, robustness of today's VQA models leave much to be desired. We introduce a new evaluation protocol and associated dataset (VQA-Rephrasings) and show that state-of-the-art VQA models are notoriously brittle to linguistic variations in questions. VQA-Rephrasings contains 3 human-provided rephrasings for 40k questions spanning 40k images from the VQA v2.0 validation dataset. As a step towards improving robustness of VQA models, we propose a model-agnostic framework that exploits cycle consistency. Specifically, we train a model to not only answer a question, but also generate a question conditioned on the answer, such that the answer predicted for the generated question is the same as the ground truth answer to the original question. Without the use of additional annotations, we show that our approach is significantly more robust to linguistic variations than state-of-the-art VQA models, when evaluated on the VQA-Rephrasings dataset. In addition, our approach outperforms state-of-the-art approaches on the standard VQA and Visual Question Generation tasks on the challenging VQA v2.0 dataset.














