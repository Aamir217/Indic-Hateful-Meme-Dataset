# Indic Hateful Meme dataset

## Overview
IndicHate presents a multimodal, multilingual approach for detecting hateful memes in Indic languages by jointly leveraging visual and textual cues.
The accompanying IndicHMHate GitHub repository serves as the reference implementation, supporting experiments in English, Hindi, and Bengali to mitigate the limited resources available for Indic hate meme detection.

## Motivation
Hateful memes combine text and images, making them challenging for unimodal systems. Most existing approaches are English-centric and do not generalize well to Indic languages. IndicHate aims to bridge this gap by providing a unified multilingual and multimodal framework.

## Dataset
The dataset consists of annotated memes in English, Hindi, and Bengali. Each sample contains a meme image, associated text (OCR or caption), and a binary hate label. Language-wise stratified splits are used for training, validation, and testing.

## Models and Methodology
Text Models: MuRIL, mBERT, XLM-R  
Vision Models: ViT, ConvNeXt  

The framework employs independent image and text encoders, projection layers to a shared embedding space, joint feature fusion, and a binary classification head for hateful meme detection.

Evaluation:  
python evaluate.py --checkpoint best_model.pth  

Inference:  
python inference.py --image path/to/image --text "meme caption"

## Folder Structure
data/ – Dataset and preprocessing  
src/ – Model, training, and evaluation code  
figures/ – Plots and visualizations  
models/ – Saved checkpoints  
configs/ – Configuration files  

## Reproducibility
Fixed random seeds, language-wise stratified splits, and standard evaluation metrics (Accuracy, Precision, Recall, F1).
