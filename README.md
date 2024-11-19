# Beach Plastic Litter Detection Using RT-DETR
Detection and classification of plastic litter on the beach is carried out using the Real-Time Detection Transformer (RT-DETR) model. RT-DETR is a transformer-based object detection architecture designed for real-time data processing with high performance https://arxiv.org/abs/2304.08069, making it very suitable for application in environmental monitoring tasks like this.

## RT-DETR Architecture
![arsitektur](rtdetr_overview_page-0001.jpg)

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
