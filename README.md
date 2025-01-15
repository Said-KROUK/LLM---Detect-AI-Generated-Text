Ce projet vise à détecter les textes générés par des modèles de langage en arabe en utilisant un modèle BERT combiné avec un classificateur SVM. Le projet est implémenté en Python et utilise des bibliothèques populaires comme transformers, scikit-learn, et pandas.

Table des matières
Aperçu

Installation

Utilisation

Structure du projet

Résultats

Contribuer

Licence

Aperçu
Le projet se concentre sur la détection de textes générés par des modèles de langage en arabe. Il utilise un modèle BERT pré-entraîné pour extraire des embeddings de texte, puis un classificateur SVM pour prédire si un texte donné est généré par une IA ou écrit par un humain.

Installation
Pour installer les dépendances nécessaires, exécutez la commande suivante :

bash
Copy
pip install -r requirements.txt
Les principales dépendances incluent :

transformers

scikit-learn

pandas

torch

nltk

pyarabic

farasapy

Utilisation
Préparation des données : Les données sont chargées à partir de fichiers CSV contenant des textes en arabe. Les textes sont ensuite prétraités pour enlever les stop words, normaliser le texte, et appliquer des techniques de stemming.

Extraction des embeddings : Le modèle BERT est utilisé pour extraire des embeddings de texte. Ces embeddings sont ensuite aplatis et normalisés.

Entraînement du modèle : Un classificateur SVM est entraîné sur les embeddings extraits pour prédire si un texte est généré par une IA ou non.

Évaluation : Le modèle est évalué sur un ensemble de développement pour mesurer sa précision, son rappel, et son F1-score.

Prédiction : Le modèle entraîné est utilisé pour prédire les labels sur un ensemble de test, et les résultats sont sauvegardés dans un fichier CSV.

Structure du projet
bert-svm.ipynb : Le notebook Jupyter contenant le code complet du projet.

train_set.csv : Fichier CSV contenant les données d'entraînement.

dev_set.csv : Fichier CSV contenant les données de développement.

test_set.csv : Fichier CSV contenant les données de test.

submission.csv : Fichier CSV contenant les prédictions sur l'ensemble de test.

svm_model_V2.pkl : Le modèle SVM entraîné sauvegardé en format pickle.

Résultats
Le modèle a atteint une précision de 99.79% sur l'ensemble de développement, avec un F1-score de 1.00 pour les deux classes (texte généré par IA et texte humain).

plaintext
Copy
Development Set Evaluation:
Accuracy: 0.9979310344827587
Classification Report:
              precision    recall  f1-score   support

           0       1.00      1.00      1.00       707
           1       1.00      1.00      1.00       743

    accuracy                           1.00      1450
   macro avg       1.00      1.00      1.00      1450
weighted avg       1.00      1.00      1.00      1450

Confusion Matrix:
[[707   0]
 [  3 740]]
Contribuer
Les contributions sont les bienvenues ! Si vous souhaitez contribuer à ce projet, veuillez suivre les étapes suivantes :

Forkez le projet.

Créez une branche pour votre fonctionnalité (git checkout -b feature/AmazingFeature).

Committez vos changements (git commit -m 'Add some AmazingFeature').

Pushez la branche (git push origin feature/AmazingFeature).

Ouvrez une Pull Request.

Licence
Ce projet est sous licence MIT. Voir le fichier LICENSE pour plus de détails.

Ce projet a été développé dans le cadre d'une compétition Kaggle visant à détecter les textes générés par des modèles de langage en arabe. Pour plus de détails, consultez le notebook Jupyter.

Ne
