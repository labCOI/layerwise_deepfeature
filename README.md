 #layerwise_deepfeature
Layer-wise Deep Feature Extraction 

Introduction:

Recent advancements in digital image processing and machine learning have led to the development of computer-aided diagnosis (CAD) systems that help improve consistency and efficiency. Current research shows that convolutional neural networks (CNNs) outperform traditional methods for BC classification, offering faster and more reliable results. However, limited medical image data often prevents effective training of CNNs from scratch. To address this, pre-trained networks are used for feature extraction. While it is commonly believed that features from the last layer of a CNN provide the best results, studies show that relying solely on these features can reduce performance. Therefore, it is crucial to consider features from multiple layers. This study proposes a method to select and use the most relevant features from different layers to improve malignancy diagnosis in histopathology images.

Objective:

The objective of this study is to use multi-layer deep features to enhance Breast Cancer classification. Effective layers of pre-trained networks are selected based on maximum value of the mutual information (MI) calculated between each layer's features and the true labels for feature extraction. Then, features refined by principal component analysis (PCA) according to the optimum cumulative explained variance (CEV) to prevent overfitting and followed by a support vector machine (SVM) classifier. The results of the proposed method using VGG19, DenseNet, and ConvNextTiny networks on the BreakHis and ICIAR/BACH datasets demonstrate a high level of performance.

Methods:

This research proposes a method for selecting effective layers and combining distinctive deep features from those layers to improve the classification of tumorous and healthy tissues. Features were extracted from the pre-trained VGG19, DenseNet, and ConvNextTiny networks using transfer learning. To measure the effectiveness of the features extracted from each layer, the mutual information (MI) between each layer’s features and the set of true labels was computed, and a set of layers based on the maximum MI was selected. To reduce the high dimensionality of the feature vectors, PCA was used to select the optimal number of principal components based on CEV. The transformed features from selected layers were then concatenated and fed into an SVM classifier for final classification.

Results:

The classification accuracy of the proposed method outperforms the baseline for all three networks that were analyzed using the BreakHis dataset. For the ICIAR/BACH dataset the proposed method improved all the evaluated metrics across all three networks, VGG19, DenseNet, and ConvNextTiny. 

Conclusion:

This study proposes a method that uses MI to identify the most effective layers for feature extraction in pre-trained networks to improve performance in the classification of BC histopathology images. As MI between each layer’s features and true labels is calculated, this approach eliminates the need for classification with features from every individual layer that is investigated, thereby speeding up the process. Moreover, This approach proved particularly effective in the ICIAR/BACH classification, where PCA led to some information loss. ConvNextTiny consistently achieves better performance by effectively capturing intricate patterns in histopathology images. 
