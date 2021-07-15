# Lung pneumonia classification with ResNet18! (PyTorch)
####
## __This is a notebook of a PyTorch lung pneumonia classification with ResNet18!__ 
## The dataset is __[CoronaHack -Chest X-Ray-Dataset from Kaggle](https://www.kaggle.com/praveengovi/coronahack-chest-xraydataset)__.
## Was built in __[Google Colab](https://colab.research.google.com/)__ environment, so make any adjustments needed for it to work on your machine.
## You can find code and detailed project analysis in __[Lung_pneumonia_classifier.ipynb](https://github.com/NikitaBezukhov/Pneumonia_classifier_ResNet18/blob/main/Lung_pneumonia_classifier.ipynb)__ notebook.
## The results of the training will be presented below.
### Dataset consists of 4910 unique X-rays of patients with and without Pneumonia.
### Model was trained for 19 epochs with early stopping point at 9 epochs. Model fit very fast even with random data augmentations, looks like this kind of problem is pretty easy for this deep of a model. 
### Resulting training metrics were:
![Screenshot_1](https://user-images.githubusercontent.com/74721678/125760484-ab64c234-5ab1-49c6-8a65-201219a05175.png)
![Screenshot_6](https://user-images.githubusercontent.com/74721678/125760545-e623008a-7326-4c75-9c8b-311ee0de7066.png)
![Screenshot_2](https://user-images.githubusercontent.com/74721678/125760516-e2792165-e120-4e2b-a598-f5af1011bebb.png)
### We were able to achieve 98% True positive rate with 15% False positive rate and 95% F1 score for pneumonia detection with threshold of 0.5!
### Lets look at ROC curve with AUC.
![Screenshot_3](https://user-images.githubusercontent.com/74721678/125760956-0a038d7f-9343-4ee4-b5ac-b443373d6ce2.png)
### AUC = 97.64, which is a pretty good result. ROC lets us choose different desicion boundary thresholds depending on how many False positives we can afford. But we can also calculate the best threshold as argmin(TPR-(1-FPR)). It will be:
![Screenshot_5](https://user-images.githubusercontent.com/74721678/125761027-a0f26c63-35e1-4ee2-a803-48f68f2ac87b.png)
### Metrics with a new threshold:
![Screenshot_4](https://user-images.githubusercontent.com/74721678/125761047-355ec466-2718-4988-80a2-5465bfcd3be2.png)




