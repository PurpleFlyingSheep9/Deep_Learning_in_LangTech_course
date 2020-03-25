# Text classification

This project is about text classification. You will develop a text classification system that identifies different kinds of online texts, such as news, blogs and opinionated texts. We will refer to these text categories as registers. If you want to learn more about online registers and their automatic identification, you can read, e.g., our paper [Toward Multilingual Identification of Online Registers] (https://www.aclweb.org/anthology/W19-6130/).

# Data and register labels
The data for this project consist of ~7500 documents with manual annotations on their register. You can download it from TODO. The documents are based on a (almost) random sample of the Finnish Internet. The registers are identified using a relatively detailed, hierarchical taxonomy. The taxonomy consists of 8 main categories that are divided into a large number of subregisters. The taxonomy is described at the end of this page (TODO). The table includes also the abbreviations that are used in the data.

The challenge with online documents is that it is not always easy to identify the specific registers categories of the documents. Furthermore, another issue is that a document may display characteristics of several registers. For instance, a blog post may simultaneously seem like a product review. To deal with these challenges, we have followed the following guidelines:
* For each document, the annotators have aimed at marking the specific subregister category. When this is possible, the document has two register labels: the subregister label and the main register label to which the subregister belongs. For instance, a document annotated as a news article would have the label NE for News and the corresponding higher level register label NA for Narrative. 
* In some cases, the document does not seem to fit any of the subregisters. In this case, the document can be given only one label: the main register label, such as NA for Narrative. 
* Some documents may display characteristics of several register categories. In this case, the annotator can mark several register labels for one single document. Consequently, the document may have up to four labels. This would be the case case if a document is annotated both as a Personal blog (subregister label PB + corresponding higher level register label NA) and Review (subregister label RV + corresponding higher level register label OP).

# Milestone 1: Bag-of-words classifier (multi-class)
Train a bag-of-words classifier to predict the register categories. In this milestone, the setting is multi-class, so the register label combinations form the classes, e.g. NA_NE and NA_NE_OP_OB. Evaluate your model and report your results with different hyperparameters.

# Milestone 2: Bert (multi-class)
Train a Bert classifier to predict the register categories. Similar to Milestone 1, the setting is multi-class, and the evaluations should include results with different hyperparameters.

# Milestone 3: Bert (multi-LABEL)
Train a multi-label classifier using Bert. In this setting, each label is assigned independently. Similar to milestones #1-2, the evaluations should include results with different hyperparameters.