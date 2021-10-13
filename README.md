# SpectralClassifier

Repository for the paper "A new automated tool for the spectral classification of OB stars"\
Astronomy & Astrophysics, accepted\
ArXiv:xxxxxxxx

**Authors:**\
Elias Kyritsis, Grigoris Maravelias, Andreas Zezas, Paolo Bonfini, Konstantinos Kovlakas, Pablo Reig

### Abstract 
**Context**:As an increasing number of spectroscopic surveys become available, an automated approach in spectral classification be-comes necessary. Due to the significance of the massive stars it is of great importance to identify the phenomenological parameters ofthese stars (e.g., the spectral type ) which can be used as proxies to their physical parameters (e.g mass, temperature).Aims.In this work, we use the Random Forest (RF) algorithm to develop a tool for the automated spectral classification of OB-typestars according to their sub-types.\
**Methods**:We use the regular RF algorithm, the Probabilistic RF (PRF) which is an extension of RF that incorporates uncertainties,and we introduce the KDE - RF method which is a combination of the Kernel-Density Estimation and the RF algorithm. We train thealgorithms on the Equivalent Width (EW) of characteristic absorption lines measured in high-quality spectra (S/N ratio (>∼50) fromlarge Galactic (LAMOST, GOSSS) and extragalactic surveys (2dF, VFTS) with available spectral-types and luminosity classes. By following an adaptive binning approach we group the labels of these data in 11 spectral classes within the range O2-B9. We examined which of the characteristic spectral lines (features) are more important for the classification based on a number of feature selectionmethods and we searched for the optimal hyper-parameters of the classifiers to achieve the best performance.\
**Results**: From the feature-screening process we find that the full set of 17 spectral lines is needed to reach the maximum performanceper spectral class. We find that the overall accuracy score is∼70% with similar results across all approaches. We apply our modelin other observational data sets providing examples of potential application of our classifier on real science cases. We find that it performs well for both single massive stars and for the companion massive stars in Be X-ray binaries, especially for data of similarquality as the training sample. In addition, we propose a reduced 10-features scheme that can be applied to large data sets with lowerS/N ratio∼20−50.\
**Conclusions**: The similarity in the performances of our models indicates the robustness and the reliability of the RF algorithm whenit is used for the spectral classification of early-type stars. The score of∼70% is high if we consider (a) the complexity of such multi-class classification problems (i.e. 11 classes), (b) the intrinsic scatter of the EW distributions within the examined spectral classes, and(c) the diversity of the training set since we use data obtained from different surveys with different observing strategies. In addition,the approach presented in this work, is applicable to products from different surveys in terms of quality (e.g different resolution), andof different format (e.g., absolute or normalized flux) while our classifier is agnostic to the Luminosity Class of a star and ,as much aspossible, metallicity independent.


### Application of the models
In this repository you will find all the needed jupyter notebooks and the pre-trained models for the different implementations of RF algorithm presented in the paper. As an example dataset we use the file *test_sample* . When you use your own dataset just change this file. If you want to use a different format for your input data you can do it **but remember** that you have change the jupyter notebooks accordingly.  
- **Application of RF model**\
In case you would like to use the RF implementation in order to get the predictions for your dataset you have to download locally the files: *RF_application.ipynb* and *RF_best_model_17_lines_FINAL.joblib* . Do not forget to change the *path* destination with your local working directory path. 
- **Application of KDE-RF model**\
In case you would like to use the KDE-RF implementation in order to get the predictions for your dataset you have to download locally the files: *KDE-RF_application.ipynb* and *KDE-RF_best_model_17_lines_FINAL.joblib* . Do not forget to change the *path* destination with your local working directory path. 
- **Application of PRF model**\
In case you would like to use the PRF implementation in order to get the predictions for your dataset you have to download locally the files: *PRF_application.ipynb* and *PRF_best_model_17_lines_FINAL.joblib* . Do not forget to change the *path* destination with your local working directory path. In addition, in this case you will also need to install on your machine the implementation of PRF algorithm which can be found __[here](https://github.com/ireis/PRF)__ .
