# Thesis Project
This is my thesis project as a graduation requirement. I combined sentence embedding by SBERT and K-Means Clustering by SKLearn to create an extractive summarization model using contextual embeddings.

Supervised by: [Dr. Hapnes Toba, M. Sc., IPM](https://it.maranatha.edu/resume/dr-hapnes-toba-m-sc/) and [Prof. Dr. Ir. Mewati Ayub, M.T.](https://it.maranatha.edu/resume/mewati-ayub/)

## Abstract
This study aims to propose methods and models for extractive text summarization with contextual embedding. To build this model, a combination of traditional machine learning algorithms such as K-Means Clustering and the latest BERT-based architectures such as Sentence-BERT (SBERT) is carried out. The contextual embedding process will be carried out at the sentence level by SBERT. Embedded sentences will be clustered and the distance calculated from the centroid. The top sentences from each cluster will be used as summary candidates. The dataset used in this study is a collection of scientific journals from NeurIPS. Performance evaluation carried out with ROUGE-L gave a result of 15.52% and a BERTScore of 85.55%. This result surpasses several previous models such as PyTextRank and BERT Extractive Summarizer. The results of these measurements prove that the use of contextual embedding is very good if applied to extractive text summarization which is generally done at the sentence level.

## Published Paper:
Published Paper: [Jurnal Teknik Informatika dan Sistem Informasi (JuTISI) (April 29, 2022)](https://journal.maranatha.edu/index.php/jutisi/article/view/4474)

## Dataset:
https://www.kaggle.com/rowhitswami/nips-papers-1987-2019-updated
