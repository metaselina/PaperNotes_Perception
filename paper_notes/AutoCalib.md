# [Automatic Surround Camera Calibration Method in Road Scene forSelf-driving Car ](https://arxiv.org/abs/2305.16840)

_February 2024_

tl;dr: A method for introducing robust automatic multi-camera (pinhole or fisheye camera) calibration and refinement in road scenes

#### Overall impression
Describe the overall impression of the paper. 

#### Key ideas
- In the paper, a fully automatic and target-free calibration method for external parameter calibration of a surround view camera based on photometric errors in overlapping regions under bird's eye view in a road scene is proposed;
- A stochastic search strategy from coarse to fine is used in the paper, which can adapt to large initial external parameter errors. This strategy, in principle, will give better results than non-linear optimisation


#### Technical details
- Compared to other calibration schemes, the paper uses texture features extracted in the consensus region of the camera, assuming the a priori condition of parallel lane lines;
- A rotation and translation up to a fixed pixel step is used to compute the photometric loss value in a way similar to gradient descent, but instead of giving a search range based on the gradient, so it is able to avoid falling into local optima

#### Notes
- The reasons for the value of the fixed threshold, and how much of an effect modifying the parameter has, are not given in the text;
- A key to automatic calibration is real-time, but no experimental data on the time-consuming nature of the algorithm is given in the text;
- The effectiveness of the algorithm is debatable for the consensus region where the texture features are not obvious or less textured or for extreme road conditions
