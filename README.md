# NN Menu

The **Neural Network Menu\*** is a collection of software that implements Neural Networks on Greenwaves Application Processor 9 (Gap9). This repository contains common mobile and edge NN archtecture examples, NN sample applications and full flagged reference designs. Our tools maps a TFLITE model (quantized or unquantized) onto gap. There is also a flow in the ingredients directory showing how to hand map from a Pytorch Model onto GAP.

For a detailed description of the content of each project please refer to the readme inside the project folder. 

## Getting Started

To run the code in this repository you need to install and source the gap9 SDK which is accessible only to qualified customers. Please [contact us](https://greenwaves-technologies.com/contacts/) if you would like to get access.

Once the sdk is installed source the sourceme.sh in the root sdk folder and retrieve this repository with a:

```
git clone --recurse-submodules -j4 git@github.com:GreenWaves-Technologies/nn_menu_gap9.git
```

## Content of the repository

The repository is divided into 4 different folders:

#### **ingredients**
Optimized models for common mobile and edge use cases. This is a playground to start with, it shows how well known networks topologies are mapped onto gap.

Content of the folder:
- Blaze Face (Face Detector + Facial Landmarks, from Google Media Pipe)
- Efficient Net: From TFLite Hub (different sizes, quantized in TFLite) and ONNX Model zoo (Post-Training Quantization in NNTool)
- MCUNet: (V1) https://mcunet.mit.edu, Post-Training Quantization in NNTool
- Mobilenet (several versions of Mobilenet V1, V2, V3) quantized in TFLite
- Resnet: 18 and 50 from ONNX model Zoo, Post-Training Quantization in NNTool
- Squeeze Net: TFLite Hub, Post-Training Quantization in NNTool
- Yam Net: TFLite Hub, w/ MelSpectrogram preprocessing, Post-Training Quantization in NNTool

These examples take image from file with semihosting in input and output the results through the shell.

#### **starters**
Use Case specific examples that use specific datasets and shows nn running for a specific task. 

Content of the folder:
- Body Detection (custom CNN) 
- Coco Object Detetion based on Mobilenet SSD
- Face Detection (custom CNN)
- Keyword Spotting ([speech_commands](https://www.tensorflow.org/datasets/catalog/speech_commands) from Tensorflow)
- Licence Plate Recognition (Mobilenet SSDLite + LPRNet)
- People Spotting (NN from [MIT Visual Wakeup Words](https://github.com/mit-han-lab/VWW))
- Tiny Denoiser (Custon RNN, LSTM and GRU version available)
- Vehicle Spotting (Customization and embedding of a deep learning pipeline for visual object spotting)

These applications take an input from file with semihosting and output the results trough shell, they also run on our boards to be tested with input from drivers. For specific cameras configrations please check the readme in within each projects folder.  

#### **sides**

This folders contains tools related to measurments and NNTool usage

Content of the folder:
- cifar10: This project shows how to train and load post training quantization statistics from Pytorch through ONNX and Tensorflow through TFLite into NNTool and deploy on GAP. 


## Futures Releases

We are actively working in the area of RNN, LSTM and GRU. Next releases will contain new repository that will be demoing it. If you have any suggestion or willing please contact us at <support@greenwaves-technologies.com>


\* We are a french Company, so we care about food. The team is composed from people all over the world, that's why we can laugh about it :-) 
