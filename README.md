# Swedes_mrcnn

Head training of MatterPort Mask-RCNN model on custom dataset of swedes production images taken from Scorpion Vision software.
Contour of the vegetable appears difficult to locate using traditionnal computer vision tools only. This model allows an accurate detection
of the contour, that is then fed back to Scorpion Vision software for geometry analysis. The whole purpose of the project is to locate and cut
both ends of the Swede (root and stem).

# Usage:

Train a new model starting from pre-trained COCO weights:
  python3 samples/samples/swede/swede.py train --dataset=/path/to/coco/ --model=coco

Labelling was done using VGG image annotator

Run trained model inference on an image folder:
  python samples\swede\swede.py detect --weights=mask_rcnn_swede.h5 --image=images\

# Results :
![image](https://user-images.githubusercontent.com/33094919/113133693-db88a280-9217-11eb-8408-04234980a27a.png)
![image](https://user-images.githubusercontent.com/33094919/113133807-fd822500-9217-11eb-9f1b-646b301c316d.png)

With SCorpion Vision software post-processing :
![image](https://user-images.githubusercontent.com/33094919/113135202-c0b72d80-9219-11eb-8060-328de2d8dd3a.png)
