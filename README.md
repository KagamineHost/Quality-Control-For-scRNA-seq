################################################################################
README for Machine Learning Project: Predicting Neuronal Cell Types from scRNAseq data

author: Dania Annuar, Yijie Kang, Jiaxing Liu, Caichen Duan
################################################################################

==========
Background
==========
This project is looking for annotated neuron cell types based on RNA-seq data. There are two different source of data used in this project: a traditional RNA-seq data from the primary visual cortex and the anterior lateral motor cortex of mouse and Patch-seq data from visual cortical GABAergic interneurons. We built machine learning models by using data from 2018 database which separated to training and test set. As the models all worked well on test set, then they been used to predict the cell type for 2020 data which only has the RNA-seq data but not have cell type annotation. 

Data:
2020 patch-seq paper
https://www.sciencedirect.com/science/article/pii/S009286742031254X

2018 Tasic paper (to build our model)
https://www.nature.com/articles/s41586-018-0654-5

Reference:
Patch-seq
https://www.jneurosci.org/content/41/5/937 
https://www.nature.com/articles/nbt.3445


=====================================================================
1. select GABAergic cells and their cell types from 2018's data (Python) - 1102_select_cells.ipynb

2. Seurat workflow from scRNA-seq quality control, normalization to PCA (R) - ML_project.Rmd
Contains the analysis for Tasic 2018 scRNAseq data from raw counts data to PCA and clustering methods using the Seurat package.

3. Train and test the logistic and random forest model based on 2018's data (Python) - 1213_Project_model_building.ipynb

4. Simulate contaminated cells (R) - 1213_makeup_mixedcells_yagi.Rmd

5. Test the model's performance in dealing with simulated contaminate (Python) - also in 1213_Project_model_building.ipynb

6. Seurat quality control and dimension reduction for 2020's patch-seq data (R) - 1212_patchseq_seurat_yagi.Rmd
