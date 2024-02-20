# [DMPR-PS: A Novel Approach for Parking-Slot Detection Using Directional Marking-Point Regression](https://github.com/Teoge/DMPR-PS)

_February 2024_        

tl;dr: A parking-slot detection method using directional marking-point regression.

#### Overall impression
Based on the CNN network of key point detection, the input image format is AVM image, and the feature information is the corner pair information at the entrance end of the parking space.

The pre-processing includes data augmentation and data enhancement, and the post-processing matches the corner pairs of parking spaces according to the model output and combines the parking spaces

#### Key ideas
- The pre-processed image is partitioned, and the parking space corners must fall inside different sub-blocks
- The information of the feature point includes, coordinates, direction, and type
- In post-processing, the pair types are fixed to 16 categories
- Corner pairs are matched a priori with a distance limit and no other points exist in the candidate pairs

#### Technical details
- The condition that a feature falls into a subblock is designed to participate in the loss function

#### Notes
- There are fewer types of parking spaces considered, and diagonal parking spaces and U-shaped parking spaces are not considered
- The judgment conditions at the entrance end of the parking space are not sufficient, and the information of the parking space division line is not fully utilized
