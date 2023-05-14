Αν και τα περισσότερα τα γράφω στο report στέλνω τους κωδικες και τα αντίστοιχα αρχεία για επαλήθευση.
Επιπλέον όσο αφορά το ερώτημα 2 έχω γράψει αποτελέσματα για τα outliers σε κάθε ερώτημα και το feature selection το έχω κάνει σε κ΄λαυε ερώτημα ξεχωρριστά


Γενικά στα παρακάτω γράφω τη μορφή :

#Ποιο κομμάτι της εργασίας εκτελέστηκε: αρχειο.pynb(ο κώδικας που χρησιμοποιήθηκε) -> data.csv(το αρχειο data που επιλέχτηκε)

##Pre processing (jupyter)

#επιλογή στηλών και γραμμών από το δοσμένο dataset: data_selection.pynb(jupyter) -> CTG.xls

#χειρισμός outliers: imputing.pynb -> smdm_data.csv
έγιναν τρεις τρόποι για τα outliers 
τα outliers έγιναν marked ως missing values και ύστερα συμπληρώθηκαν με το mean by group του εργαστηρίου
1. ως προς class imputed_data.csv
2. ως προς NSP  clust_imputed_data.csv
3. με ΚΝΝ imputer knn_imputed.csv

#PCA : PiCiAi.pynb -> imputed_data.csv

#numerocity reduction(με ΒΙΝ) :Numerosity_Reduction.pynb -> mean_data.csv(data με PCA και imputing)

##Classification (jupyter)

#SVM στο αρχικό dataset με outliers: raw_classification_with_outliers.pynb -> sh_smdm_data.csv(το smdm data απλά με shuffle ώστε να συγκρίνω αποτελέσματα για διαφορετικές παραμέτρους)

#SVM στο αρχικό dataset χωρίς outliers: raw_classification_without_outliers.pynb -> imputed_data.csv

#SVM στο PCA dataset χωρίς outliers(11 features): classification_svm.pynb -> mean_data.csv 

##Clustering (όλα με PCA για ευκολότερο feature selection)  Colab

#K-Means with outliers: kmeans_clustering_PCA_with_outliers.ipynb -> smdm_data.csv

#Kmeans without outliers: kmeans_clustering_without_outliers.ipynb ->clust_imputed_data.csv(mean by group-NSP)

#GMM with outliers : GMM__with_PCA.ipynb -> smdm_data.csv

#GMM without outliers: GMM_with_PCA_without_outliers -> clust_imputed_data.csv

##Tensor-Keras Colab

#NN χωρίς PCA: NN.ipynb -> smdm_data.csv

#NN με PCA : NN_PCA.ipnb -> smdm.data.csv