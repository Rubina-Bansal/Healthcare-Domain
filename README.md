### Healthcare-Domain
End-to-End Project (Unsupervised Learning)

## Problem Understanding
The differential diagnosis of erythemato-squamous diseases is a real problem in dermatology. They all share the clinical features of erythema and scaling, with very little differences. The diseases in this group are psoriasis, seboreic dermatitis, lichen planus, pityriasis rosea, cronic dermatitis, and pityriasis rubra pilaris. Usually a biopsy is necessary for the diagnosis but unfortunately these diseases share many histopathological features as well. Another difficulty for the differential diagnosis is that a disease may show the features of another disease at the beginning stage and may have the characteristic features at the following stages. Patients were first evaluated clinically with 12 features. Afterwards, skin samples were taken for the evaluation of 22 histopathological features. The values of the histopathological features are determined by an analysis of the samples under a microscope.

## Objective
Using USL, tried to classify patients into different groups based on their attributes. Also, used PCA for dimensionality reduction.

### Dataset
In the dataset constructed for this domain, the family history feature has the value 1 if any of these diseases has been observed in the family, and 0 otherwise. The age feature simply represents the age of the patient. Every other feature (clinical and histopathological) was given a degree in the range of 0 to 3. Here, 0 indicates that the feature was not present, 3 indicates the largest amount possible, and 1, 2 indicate the relative intermediate values

### Attribute Information: 
**Clinical Attributes:** (take values 0, 1, 2, 3, unless otherwise indicated)   <br>
1: erythema <br>
2: scaling <br>
3: definite borders  <br> 
4: itching <br>
5: koebner phenomenon     <br> 
6: polygonal papules <br>
7: follicular papules <br>
8: oral mucosal involvement             <br> 
9: knee and elbow involvement <br>
10: scalp involvement <br>
11: family history, (0 or 1)    <br>
34: Age (linear) <br>
​<br>
**Histopathological Attributes:** (take values 0, 1, 2, 3)  <br>
​<br>
12: melanin incontinence       <br>
13: eosinophils in the infiltrate <br>
14: PNL infiltrate <br>
15: fibrosis of the papillary dermis   <br>
16: exocytosis <br>
17: acanthosis <br>
18: hyperkeratosis <br>
19: parakeratosis <br>
20: clubbing of the rete ridges <br>
21: elongation of the rete ridges <br>
22: thinning of the suprapapillary epidermis             <br> 
23: spongiform pustule <br>
24: munro microabcess <br>
25: focal hypergranulosis             <br>
26: disappearance of the granular layer         <br>
27: vacuolisation and damage of basal layer       <br>
28: spongiosis <br>
29: saw-tooth appearance of retes                  <br>
30: follicular horn plug                  <br>
31: perifollicular parakeratosis           <br>
32: inflammatory monoluclear inflitrate            <br>
33: band-like infiltrate               <br> 
35:class label <br>

#### Methodology :-
The first step taken was understanding the data and preprocessing it to make it ready for analysis. Important cheacks like missing values, outlier analysis, correlation and covariance analysis were done. Then using PCA on the dataset, determined the number of PCA components to be used so that 90% of the variance in data is explained by the same.          <br>
Optimal number of clusters were determined using KMeans(eigenvalues, eigenvectors) and Hierarchial Clustering(visualizing dendrograms) Techniques.  <br>
Final Clustering was done using Agglomerarive Clustering.               <br>

Business interpretation/explanation of the model.           <br>
So, from our analysis we could conclude that Agglomerative clustering has done a pretty good job of clustering almost all the classes except for 1 misclassification of class 3 and 1 misclassification of class 5. Both are interchanged. So the total accuracy is 355/357.
​
