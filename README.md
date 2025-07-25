Title: A Framework for Detecting Hate Speech and Offensive Language




The benchmark dataset provided by Davidson et al has been used in this study for the detection of hate speech and offensive language. This dataset consists of 24,783 English tweets categorized into three distinct classes: hate, offensive, and neither.

To address the class imbalance issue during the training phase, the number of samples in the Neither class (the neutral class) is used as a reference. This class represents the middle ground between the other two classes, Offensive (the majority class) and Hate (the minority class). The high number of samples in the Offensive class can cause the model to be biased toward this class, which disrupts the learning of patterns relevant to the other classes, especially the Hate class. Therefore, reducing the number of samples in the Offensive class is necessary. This is achieved through undersampling [32], where a random selection of samples from the Offensive class is made, and the remaining ones are discarded. The primary goal of this technique is to balance the dataset and align the sample distribution across the classes.However, the main issue still lies with the minority class, the Hate class. To compensate for this deficiency, data augmentation techniques are applied. 

Since tweets often lack standard punctuation and grammatical structure, preprocessing is performed to improve the quality of the input data. Subsequently, word embeddings are generated using the most suitable methods for this domain. Finally, to achieve optimal classification performance, several machine learning models and four deep learning models, which have demonstrated promising results in related domains, are evaluated.
