# Cross-domain Prerequisite Chain Learning using HeterogeneousVariational Graph Autoencoders (H-VGAE)
This repo contains code and data for Vanessa Yan's final project for the Advanced Natural Language Processing class at Yale University. Irene Li and Vanessa Yan collaborated on this project. The writeup was written by Vanessa Yan.


## To run the code
For H-GVAE code, run "python3 train.py"
For baselines, open the jupyter notebook titled "trainBaselines.ipynb"

## Dataset- aka LectureBank3.0
The /data repo has two subrepos /CV and /NLP. 

The /data/CV repo contains 5 training and testing sets consisting of Computer Vision concepts pairs and their corresponding prerequisite annotation. These sets were created with 5 different random seeds in /data/splitAnno.py. The full set of CV topics can be found in /data/CV/final.CV151topics.tsv. The full set of CV annotations can be found in /data/CV/final.CV.annotation.csv. The full set of CV lecture slides can be found in /data/CV/final.CV1024slides.tsv. Within the /data/NLP repo, you will find the full list of NLP topics in /final.NLP322topics.tsv, the full set of NLP annotations in /final.NLP.annotation.csv, and the full set of NLP lecture slides in /final.NLP1717slides.tsv.

In the /concepts repo , you will find a file /combined_concepts.tsv which is a combined list of the NLP and CV concepts. /cv_annotations.csv is a fullset of the CV annotations. The full set of the CV concepts is also available in both .csv and .txt format in this folder.

## TFIDF
The /edges/tfidf.py file is used to prepare the adjacency matrix A. 

## BERT finetuning
The /transformers and /finetuning_BERT repos are used for finetuning BERT embeddings via the masked language modeling task on our own corpus. The repo /combined-test-mlm stores the finetuned BERT model.

## Model Architecture
train.py, model.py, layers.py optimizer.py, utils.py, and myutils.py make up the implementation of the H-VGAE model.


