# Project Overview

This repository contains the work for the course "Programming Integration - Overall (CO3101)" conducted at Ho Chi Minh City University of Technology (HCMUT). The core focus of the project is to develop an image captioning system specifically tailored for radiological brain images.

## About the Project

The essence of this project is to pioneer in the realm of medical imaging by using advanced deep learning techniques for captioning radiology images, with a prime spotlight on brain scans. We aim to leverage this technology to assist radiologists in interpreting scans more efficiently and to contribute to automated reporting systems in the medical field. 

## Data Organization

The dataset used for this project can be found in the `Data` directory of this repository. We curated the required images from the larger ROCO (Radiology Objects in COntext) Dataset [1], selectively focusing on brain images. This was accomplished by meticulously filtering the dataset to include only those images which have captions relevant to brain radiology.

## Model Training Environment

To train our state-of-the-art model, we've utilized the robust computational infrastructure provided by Kaggle, incorporating the use of two T4 GPUs for an optimized training experience.

## Model Architecture

Our model is constructed using PyTorch, a cutting-edge machine learning library. The architecture is grounded on Microsoft's innovative GIT (Generative Image Transformer) Model from Hugging Face [2], which has showcased remarkable performance in generating descriptive texts for images.

## Usage

To employ the pre-trained weights of this model, users can load them from the `Model` folder. This can be seamlessly done by using the `load_state_dict` function from PyTorch to initialize the model with these weights.

## Results

The model's performance, evaluated on various metrics, is reported as follows:

- Average BLEU score with 2-grams: 0.2244085083222495
- Average BLEU score with 3-grams: 0.17153852520756194
- Average BLEU score with 4-grams: 0.17153852520756194
- Average ROUGE-1 F1 score: 0.25079220372713634
- Average ROUGE-2 F1 score: 0.08076691711377516
- Average ROUGE-L F1 score: 0.22913274358404553

We use some famous LLMs model to evaluate our model, using a prompt in slide representation, we ask these model to give the evaluation scores about the similarity of the expected captions and our model's caption

- Bard: 0.41044776119402987
- GPT-3.5: 0.26336633663366343
- GPT-4: 0.2780487804878049

## Citations

[1] To cite the ROCO dataset, please use:

```bibtex
@inproceedings{roco_dataset,
  title={ROCO: a dataset of images with radiology reports in context},
  booktitle = {Lecture Notes in Computer Science},
  series = {Lecture Notes in Computer Science},
  volume = {11043},
  pages = {180--189},
  editor = {Stoyanov, D., et al.},
  organization = {Springer},
  doi = {10.1007/978-3-030-01364-6_20},
  year = {2018}
}
@article{Microsoft_git,
  title={GIT: A Generative Image-to-Text Transformer for Vision and Language},
  author={Jianfeng Wang and Zhengyuan Yang and Xiaowei Hu and Linjie Li and Kevin Lin and Zhe Gan and Zicheng Liu and Ce Liu and Lijuan Wang},
  journal={arXiv preprint arXiv:2205.14100},
  year={2022},
  url={https://doi.org/10.48550/arXiv.2205.14100}
}

