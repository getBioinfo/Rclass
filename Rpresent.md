

Genotyping by DNA Amplicon Melting Analysis
========================================================
author: Hong Xu
date: 12/10/2014

DNA Melting Curve
========================================================

Different DNA fragments can have different melting curve characteristics during heating, which forms the base of genotyping by DNA amplicon melting analysis. 

***

![plot of chunk unnamed-chunk-1](Rpresent-figure/unnamed-chunk-1-1.png) 


Preprocessing DNA Melting Curve Data
========================================================

Different DNA fragments have close melting curve data. Preprocess melting curve raw data by getting their negative first derivative, which can improve the performance of some machine learning algorithms.  

***

![plot of chunk unnamed-chunk-2](Rpresent-figure/unnamed-chunk-2-1.png) 


Machine Learning Algorithm
========================================================

- [Linear Discriminant Analysis (LDA)](http://en.wikipedia.org/wiki/Linear_discriminant_analysis): use a linear combination of features to separate two or more classes of objects.
- [Naive Bayes (naiveBayes)](http://en.wikipedia.org/wiki/Naive_Bayes_classifier): use Bayesian theorem with strong (naive) independence assumptions to classify different classes of objects. 
- [Boosted Logistic Regression (LogitBoost)](http://en.wikipedia.org/wiki/LogitBoost): use boosting algorithm to optimize logistic regression, which then classify different classes of objects.


Conclusion
========================================================

- Linear Discriminant Analysis (LDA): work well with both raw melting data and the first derivative of melting data. 
- Naive Bayes (naiveBayes): work better with the first derivative of melting data than with raw melting data. 
- Boosted Logistic Regression (LogitBoost): work better with the first derivative of melting data than with raw melting data.
