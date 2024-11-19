# Beach Plastic Litter Detection Using RT-DETR
Detection and classification of plastic litter on the beach is carried out using the Real-Time Detection Transformer (RT-DETR) model. RT-DETR is a transformer-based object detection architecture designed for real-time data processing with high performance, making it very suitable for application in environmental monitoring tasks like this.

## RT-DETR Architecture
![]("rtdtr_overview.jpg")

## Dataset
The plastic litter dataset used is sourced from the following link https://universe.roboflow.com/monash-ventz/beach-waste-vqths with the following data usage license explanation https://creativecommons.org/licenses/by/4.0/.
RT-DETR is trained to recognize several key labels that fall into the plastic litter category, such as:
- Bottle
- Clothes
- Metal
- Plastic
- Rope
- Styrofoam
- Wood
