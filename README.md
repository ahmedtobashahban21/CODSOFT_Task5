# CODSOFT_Task5


# TrOCR Model - IAM Dataset Fine-Tuned

## Table of Contents

- [1.0 Introduction](#10-introduction)
    - [1.1 Model Description](#11-model-description)
    - [1.2 Import Requirements](#12-import-requirements)
    - [1.3 Using the Model](#13-using-the-model)
    - [1.4 Evaluating the Model](#14-evaluating-the-model)
- [2.0 Model Link](#20-model-link)

##  Introduction

Welcome to the TrOCR model repository! This model is a powerful optical character recognition (OCR) tool, fine-tuned on the IAM dataset. TrOCR is a state-of-the-art solution that utilizes transformer-based architecture to convert handwritten text images into machine-readable text. It was introduced in the paper "TrOCR: Transformer-based Optical Character Recognition with Pre-trained Models" by Li et al. and is now available in this repository.

###  Model Description

The TrOCR model is designed as an encoder-decoder model. It consists of the following components:

- **Image Transformer as Encoder**: This component processes input images. It was initialized with the weights of DeiT, making it an effective feature extractor for images.

- **Text Transformer as Decoder**: This component decodes the extracted features and generates textual output. It was initialized with the weights of UniLM.

The OCR process involves presenting images to the model as a sequence of fixed-size patches with a resolution of 16x16. These patches are linearly embedded, and absolute position embeddings are added before being passed through the Transformer encoder layers. The Transformer text decoder operates in an autoregressive manner to generate text tokens.


