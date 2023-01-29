Image-to-Image Translation with Generative Adversarial Networks
---------------------------------------------------------------------------------------------------------------------------
Keras implementation for learning an image-to-image translation (i.e. pix2pix) without input-output pairs.

This package includes GAN_model, GAN_satellite2maproutes, instancenormalization.
The code was written by Pankaj Kumar Magar and Vedant Parwal.

Setup
---------------------------------------------------------------------------------------------------------------------------
Prerequisites

	Linux or OSX
	NVIDIA GPU + CUDA CuDNN (CPU mode and CUDA without CuDNN may work with minimal modification, but untested)

Dependecies
---------------------------------------------------------------------------------------------------------------------------
	Install Keras and dependencies
	Install tensorflow

Download the dataset
---------------------------------------------------------------------------------------------------------------------------
	Download dataset from https://people.eecs.berkeley.edu/~taesung_park/CycleGAN/datasets/maps.zip.
	Set dataset path as path = 'maps/'

Train the model
---------------------------------------------------------------------------------------------------------------------------
	To train model from scratch just run the GAN_satellite2maproutes.py.
	To use pretrain weights specify in load_model path as follow: 
		model_AtoB = load_model('GAN_SatelliteToMaps/Pretrain_Weights/g_model_AtoB_002500.h5', cust)
		model_BtoA = load_model('GAN_SatelliteToMaps/Pretrain_Weights/g_model_BtoA_002500.h5', cust)
	
Acknowledgments
---------------------------------------------------------------------------------------------------------------------------
	Some part of code is borrowed from pix2pix and DCGAN. The code is modified to work for unpaired images and both 
way translation using resnet architecture. The generative network is adopted from neural-style with Instance Normalization.


