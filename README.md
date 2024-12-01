# Beach Litter Detection Using RT-DETR
<p> Miftahul Huda<sup>1</sup> &nbsp;&nbsp;&nbsp; Dimas Rizky Ramadhani<sup>2</sup> &nbsp;&nbsp;&nbsp; Nabila Azhari<sup>3</sup> &nbsp;&nbsp;&nbsp; Arsyiah Azahra<sup>4</sup> &nbsp;&nbsp;&nbsp; Putri Maulida Chairani<sup>5</sup> </p>
<br>
Detection and classification of litter on the beach is carried out using the Real-Time Detection Transformer (RT-DETR) model. RT-DETR is a transformer-based object detection architecture designed for real-time data processing with high performance https://arxiv.org/abs/2304.08069, making it very suitable for application in environmental monitoring tasks like this.

## RT-DETR Architecture
![arsitektur](RT-DETR_Arsitektur.png)
reference: https://arxiv.org/abs/2304.08069 and https://github.com/ultralytics/ultralytics/tree/main/ultralytics

## Dataset
The plastic litter dataset used is sourced from the following link https://universe.roboflow.com/monash-ventz/beach-waste-vqths with the following data usage license explanation https://creativecommons.org/licenses/by/4.0/.
RT-DETR was trained using 2675 training data to recognize several main labels included in the plastic waste category, such as:
- Bottle
- Clothes
- Metal
- Plastic
- Rope
- Styrofoam
- Wood

## Evaluation Results
There are 561 validation data without wood and clothes category for evaluation

| Class        | Images | Instances | Precision | Recall | mAP@IoU[50] | mAP@IoU[50-95] |
|--------------|--------|-----------|-----------|--------|-------------|----------------|
| **All**      | 561    | 2558      | 0.848     | 0.744  | 0.810       | 0.606          |
| **Bottle**   | 366    | 874       | 0.906     | 0.814  | 0.872       | 0.638          |
| **Metal**    | 228    | 458       | 0.882     | 0.852  | 0.878       | 0.648          |
| **Plastic**  | 331    | 603       | 0.838     | 0.776  | 0.819       | 0.636          |
| **Rope**     | 155    | 205       | 0.709     | 0.512  | 0.619       | 0.409          |
| **Styrofoam**| 195    | 418       | 0.904     | 0.765  | 0.861       | 0.697          |

![cm](confusion_matrix.png)

## Inference
![inf](inference.png)
![inf](output1.png)

## Reference
[1] Monash, "Beach Waste Dataset," *Roboflow Universe*. Roboflow, Oct. 2024. [Online]. Available: [https://universe.roboflow.com/monash-ventz/beach-waste-vqths](https://universe.roboflow.com/monash-ventz/beach-waste-vqths). Accessed: Nov. 19, 2024.

[2] Y. Zhao, W. Lv, S. Xu, J. Wei, G. Wang, Q. Dang, Y. Liu, and J. Chen, "DETRs Beat YOLOs on Real-time Object Detection," *arXiv preprint*, 2024. [Online]. Available: [https://arxiv.org/abs/2304.08069](https://arxiv.org/abs/2304.08069).

[3] Ultralytics, "Ultralytics Neural Network Modules," GitHub repository, 2024. [Online]. Available: https://github.com/ultralytics/ultralytics/tree/main/ultralytics/nn/modules. [Accessed: Dec. 1, 2024].

