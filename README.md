# Adversarial-Machine-Learning-for-Text-Classification
Synonym-Based Adversarial Attack and Defense in Natural Language Processing

Team Members:
Jhansi Lakshmi Kaligineedi
Simran Sunil
Lalithya Manasa Patri
Venkata Mohana Rao Nandigam

Below are the steps for performing the HQA Attack:

Download the dataset 
http://ai.stanford.edu/~amaas/data/sentiment/aclImdb_v1.tar.gz

Download the Glove
http://nlp.stanford.edu/data/glove.840B.300d.zip

Download the counter fitted vector
https://raw.githubusercontent.com/nmrksic/counter-fitting/master/word_vectors/counter-fitted-vectors.txt.zip

Preprocessing and Setup
After downloading the required dataset, glove set , counter fitted vector set from the above run the  below file  build_embeddings.py

Train the model - train_model.py

Language Model and Distance Matrix – run the file compute_dist_mat.py for computing the distance matrix.

Evaluation and Attacks – to evaluate attack and investigate the attack results run HQA_Attack_Demo.ipynb

Below are the steps for performing the Defense:

Synonym Based Defense Technique

# Prerequisites
After setting up attack requirements and running the attack model, proceed with defense setup by running:
build_embeddings.py for embedding initialization

Defense Model Training 
Initialize and train the defense model by running: 
Synonym_Defense_Demo.ipynb

Model Evaluation
The above defense notebook shall:
- Train the defense model 
- Calculate defense accuracy
- Visualize defense results against attacks
- Generate comparison metrics between original and defended models

Results Analysis
View detailed defense results including:
- Normal Model Accuracy
- Model Accuracy with SEM Defense 
- Attack Accuracy with SEM Defense


Below are the attached results upon performing HQA Attack without any defense technique applied

 


There are 20 such attack demos displayed in the Text_Attack_Demo.ipynb
 
 

 


 

 


Below are attached results upon training the model with Synonym Base Defense technique 

 


There are 20 such attack demos displayed in the Synonym_Defense_Demo.ipynb 


 

 

 

 

 


Result Insights:

Adversarial Attacks are Effective Without Defense:
The adversarial manipulations demonstrate a high attack success rate (89%), which implies that without defensive methods, adversaries can successfully manipulate sentiment analysis predictions with minimal text perturbations.

Synonym based Defense Reduces Adversarial Manipulation Impact:
With the defense, the attack accuracy drops significantly to 20%.
This indicates that defense acts as a robust mechanism to detect and counteract adversarial manipulations by identifying small perturbations or semantic inconsistencies.

Minimal Perturbations Are Enough to Cause Significant Prediction Changes:
The median and mean values of text modifications (6.45% median and 9.14% mean) show that adversaries can exploit relatively small changes to flip a model's decision-making.

Without defense, adversarial manipulations are very effective and can alter model predictions significantly with minimal text changes.
The synonym-based defense mechanism is effective at reducing the success rate of adversarial attacks. Preventing the prediction changes induced by minimal perturbations.
Allowing the model to return to stable, correct predictions with defense mechanisms enabled.

