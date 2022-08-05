# Towards High Performance One-Stage Human Pose Estimation
This is an official pytorch implementation of [*Towards High Performance One-Stage Human Pose Estimation*]. 

Making top-down human pose estimation method present both good performance and high efficiency is appealing. Mask RCNN can largely improve the efficiency by conducting person detection and pose estimation in a single framework, as the features provided by the backbone are able to be shared by the two tasks. However, the performance is not as good as traditional two-stage methods. In this paper, we aim to largely advance the human pose estimation results of Mask-RCNN and still keep the efficiency. Specifically, we make improvements on the whole process of pose estimation, which contains feature extraction, keypoint detection, and results post-processing. The part of feature extraction is ensured to get enough and valuable information of pose. Then, we introduce a Global Context Module into the keypoints detection branch to enlarge the receptive field, as it is crucial to successful human pose estimation. Lastly, the results post-processing steps are used to further improve the performance. On the COCO val2017 set, our model using the ResNet-50 backbone achieves an AP of 68.1, which is 2.6 higher than Mask RCNN (AP of 65.5). Compared to the classic two-stage top-down method SimpleBaseline, our model largely narrows the performance gap (68.1 $AP^{kp}$ vs. 68.9 $AP^{kp}$) with a much faster inference speed (77 ms vs. 168 ms), demonstrating the effectiveness of the proposed method.
