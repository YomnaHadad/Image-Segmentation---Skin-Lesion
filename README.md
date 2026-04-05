# **Skin Lesion Segmentation (U-Net Vs SegNet)**

This project focuses on automated skin lesion segmentation using deep learning techniques. 

Two publicly available datasets
**<[Resized Dataset for Skin Lesion Segmentation](https://www.kaggle.com/datasets/apurboshahidshawon/resized-dataset-for-skin-lesion-segmentation-new)>**
**<[Skin Cancer HAM10000 (Raw and Lesion Segmentation)](https://www.kaggle.com/datasets/mfazrinizar/skin-cancer-ham10000-raw-and-lesion-segmentation
)>**

were combined to create a more diverse and robust training set. The merged dataset enhances variability in lesion shapes, sizes, and textures, improving model generalization.

## **Methodology**

The preprocessing pipeline included dataset merging, image resizing, normalization, and alignment of corresponding segmentation masks. Two convolutional neural network architectures were implemented and compared:

* **SegNet Architecture**: A deep encoder-decoder network designed for pixel-wise segmentation tasks.
    **<[Kaggle Notebook](  https://www.kaggle.com/code/yomnaelhadad/imagesegmentation-skinlesion-98#Model-Architecture)>**

* **U-Net Architecture**: A widely used biomedical segmentation model featuring skip connections to preserve spatial information.

Both models were trained to perform binary segmentation, identifying lesion regions from dermoscopic images.

## **Evaluation Metrics**

Model performance was evaluated using:

* **Accuracy**
* **Dice Coefficient (F1 Score for segmentation)**
* **Loss**

## **Results**
* **SegNet Model**

  * Validation Accuracy: **0.9592**
  * Dice Coefficient: **0.8091**
  * Loss: **0.1909**

* **U-Net Model**

  * Accuracy: **0.9946**
  * Dice Coefficient: **0.8302**
  * Loss: **0.1698**

## **Conclusion**
The U-Net model outperformed SegNet across all evaluation metrics, achieving higher accuracy and Dice coefficient with lower loss. This improvement is primarily attributed to U-Net’s skip connections, which help retain fine-grained spatial details critical for precise lesion boundary detection.

## **Impact**
This work demonstrates the effectiveness of deep learning in medical image segmentation and highlights the importance of architecture selection. The results suggest that U-Net is better suited for skin lesion segmentation tasks and could be further optimized for real-world clinical applications.

* Add **technical stack (TensorFlow/PyTorch, etc.)**
* Or make it sound more like a **research paper abstract**
