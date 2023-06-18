
## Biosonar - Odontoceti Click Detection
#### Contributors: ABABII Anisoara et MOUSSA Yasmina, Université Paris 1 Pantheon Sorbonne

To use this project, you must make the follow commands:

pip install -r requirements.txt
If you use conda virtual env:

conda env create -f environment.yml
conda activate paraphrase-identification

## Project

Le projet est basé sur un challenge de l'ENS nommé "Biosonar - Odontoceti Click Detection" par l'Université de Toulon. Les données sont des enregistrements d'audios de sons de dauphins et des sons d'autres animaux marins. Le but du projet est de répondre à la question suivante: l'audio est-il un biosonar (son de dauphin) ou un son perturbateur (autres animaux marins)? Pour résoudre cette problématique, nous allons prendre en input les audios dans différents modèles de Machine Learning et Deep Learning.

Le jeu de données est composé de fichier audio wav pour l'ensemble d'entraînement pour l'ensemble de test. 
les données sont disponibles sur le site: https://challengedata.ens.fr/participants/challenges/85/ 
Le dosier à télécharger : x_train

Chaque fichier audio wav de 200 millisecondes contient un clic de biosonar ou un bruit de fond avec des transitoires. Le clic/transitoire potentiel est centré dans le signal. Il peut y en avoir un seul ou plusieurs. Chaque fichier wav est dynamique sur 16 bits, avec une fréquence d'échantillonnage de 256 000 Hz. Les fichiers audio d'entraînement sont dans le dossier X_train.zip. Ce dossier contient environ  8 000 fichiers et environ 6 000 fichiers pour le test.

Format de Y_train.csv :
[id, pos_label]
1250-JAM, 0
1251-JAM, 1
1252-BON, 1

Description de l'ID :
L'ID correspond au nom du fichier audio. Il est composé d'un index d'enregistrement et du nom de la session d'enregistrement. Le format de l'ID est le suivant :
[INDEX]-[RECCODING_SESSION]

Les noms de session d'enregistrement sont :
"JAM", "BON", "BAHAMAS", "GUA", "ARUBA", "StEUS", "StMARTIN", "BAHAMAS"

Pendant la phase d'évaluation, nous avons procedé à un split en train_test_split a partir de dosier téléchargé.

Description de l'étiquette :

pos_label = 1 : "X contient un biosonar détecté (dauphin, delphinidé)"
pos_label = 0 : "X ne contient pas de biosonar détecté (bruit)"

### La structure du projet est la suivante : 
- I Préparation du dataset
- II Classification avec modele benchmark et deep learning
- III Conclusion


