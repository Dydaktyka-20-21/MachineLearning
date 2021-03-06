# Probabilistics methods 

## Content 

### Probability, discrete_random_variables,  continuous_random_variables

In this notebooks I recollect basic concepts of probability calculus. It also introduces some popular probability distributions for further reference. 

### Binary classification

This notebook contains  definitions of various metrics used to rate performance of binary classifiers. This includes ROC (receiver operational characteristic) curves. 


### Bayesian analysis*

Generative methods that are the subject of this chapter require estimation of the parameters of probability distributions. This is a domain of _statistics_. In this notebook I introduce the concepts of Baysian statistics. While we will not be using any advanced techniques, the concepts of  prior and posterior probability distributions are very important and are widly refered in many ML tasks.  

You can skip the A/B testing example on the first reading. 

### Classification Naive Bayes

In this notebook we will  actually for the first time start training the classifiers i.e. get to the "learning"  part in Machine Learning. We will reimplement the "sex from height" classifier this times basing on data.

We will also add weight as an additional feature and introduce Naive Bayes classifier. 


### Categorical

While in classification and classification_naive_bayes notebooks we have constructed classifiers with continous features, in this notebook we will play with an example  of 
classifier with solely categorical (nominal) features. This will also give us oportunity to use the tools for constructing classifiers  provided in the scickit-learn library. We will also learn to measure the performance of non-binary classifiers. 

### Text analysis

This notebook introduces very simple text classification based on Multinomial Naive Bayes. We will learn how to use text preprocesing tools from scikit-learn library and apply them to predict ratings of amazon reviews.

We will also start doing some hyperparameters tuning, that is the parameters that control how the classifiers learn. 


### Gaussian (quadratic) Discriminative Analysis

This notebook describes   classification method based, in spite of the name, on the same generative principle. In this approach the  sampling distribution for each class is assumed to be Multivariate Normal (Gaussian). This leads to classification regions being bounded by quadratic surfaces (curves), hence also the name Quadratic Discriminative Analysis. 
This  method encompasses as specialisation also Gaussian Naive Bayes and Linear Discriminative Analysis. 

### Calibration of classifiers

So far we have tried hard to estimate the probability of examplar belonging to class  _c_ given the features  __x__ 
but to some  we have not actually made use of the fact that this is a probability. We have treated the output of the classifier as a score that we used for thresholding. While the ultimate goal of the classfier is to classify, we can treat the probabilistic classifiers presented so far as doing regression i.e. learning a function. In this case the function is the conditional probability presented above. We have also concentrated solely on measuring classification performance, but we can also ask how well is the classifier predicting the probabilities? This is a question about the calibration of the classifier and this is the subject of this notebook. 


### Gausian Mixture Models and  EM algorith

When the requirement that features distribution in each class is multivariate normal is too restrictive, we can use the Gaussian Mixture Model (GMM) to estimate the density in each class. This notebook provides an introduction to Estimation-Maximization algorihm used for fitting sych models. 


### Gausian Mixture Models Discriminative Analysis

This notebook contains implementation  of Gausian Mixture Models Discriminative classifier conforming to scikit-learn interface. 


### Gaussian Mixture Models for clustering

In the gaussian mixture models - EM notebook we have used the mixture models for _density estimation_ e.g. modeling the  distribution of features in each class. Another common application is _clustering_. 


While technically the procedure of fitting is similar to supervised learning with gaussian mixture discriminative analysis (GMDA) the crucial difference lies in the interpretation. 

In GMDA the clusters are only a mean to better approximation of the class probability densities and their interpretation is irrelevant for the functioning of the classifier. We can choose the number of clusters that gives best classification results, because we have clear metrics to measure the performance.

In clustering we usually want to discover the structure of data and assign some interpretation to discovered clusters. But the  number of clusters is an input parameter. In the height-weight examples we knew that  this was two so the results were good. And we have used the real labels to check that. 

But this is not a case in general. We could experiment with different number of clusters but we need the criteria for evaluating the quality of clustering in absence of real labels. 

In this notebook we will discuss how the estimate the "best" number of clusters. 

### Probabilistic Graphical Models (PGM)

The probabilistic approach to Machine Learning is all about probability distributions. With many  variables the joint probability distribution quickly becomes intractable. However often not all variables are dependent on each other. Exploating the (in)dependence structure of the model can reducer the number of parameters by several orders of magnitude. Graphical models give a very intuitive way to represent such structure. This notebook is a short introduction to this topic. 