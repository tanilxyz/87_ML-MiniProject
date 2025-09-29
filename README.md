In observational healthcare research, adjusting for confounding variables is essential to avoid biased estimates of treatment effects. Traditional approaches rely heavily on structured data such as demographics, diagnoses, and medications coded in electronic health records (EHRs) or administrative claims. However, a vast amount of potentially valuable information exists in unstructured clinical notes, which are rarely incorporated due to challenges in extracting usable features at scale.

This paper introduces a scalable natural language processing (NLP)-based framework for feature engineering that leverages free-text notes in combination with structured claims/EHR data to improve confounding adjustment. The central idea is to generate high-dimensional proxy features from clinical text and integrate them into adjustment models, thereby capturing latent patient characteristics that are often missing in structured data alone.

The methodology follows a three-step process:

Feature Extraction: Clinical notes are transformed into large sets of sparse features using text-mining techniques such as bag-of-words and term frequency–inverse document frequency (TF-IDF). These features serve as proxies for health status, comorbidities, and care processes not explicitly coded.

Dimensionality Reduction & Selection: Because the resulting feature space is ultra-high dimensional, dimensionality reduction or penalized regression methods are applied to ensure computational feasibility and prevent overfitting.

Confounding Adjustment: The generated features are incorporated into high-dimensional adjustment models, such as high-dimensional propensity score (hdPS) frameworks or penalized logistic regression, to control for both measured and proxy confounders.

The authors demonstrate the framework across cohort studies comparing treatment effects. Their results show that adding NLP-derived features improves covariate balance between treatment groups and modestly enhances the performance of adjustment models. Importantly, this suggests that textual notes capture clinically meaningful confounding information that structured data alone may miss.

The study also highlights computational scalability: the proposed workflow can handle very large vocabularies and datasets without excessive resource demands. This makes it suitable for application in real-world healthcare databases, where millions of patients and extensive free-text corpora are common.

In conclusion, this work provides evidence that integrating NLP-based features into confounding adjustment pipelines improves the validity of observational studies. It bridges the gap between structured EHR fields and unstructured clinical narratives, paving the way for more robust comparative effectiveness and safety research in healthcare.
