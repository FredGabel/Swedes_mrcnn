# Swedes_mcnn

# Train a new model starting from pre-trained COCO weights
python3 samples/samples/swede/swede.py train --dataset=/path/to/coco/ --model=coco

# Run trained model inference on an image folder
python samples\swede\swede.py detect --weights=mask_rcnn_swede.h5 --image=images\
