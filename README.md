# Pràctica Kaggle APC UAB 2021-22
### Nom: Arnau Cruz Gargallo
### DATASET: Email Spam Classification Dataset CSV
### URL: [kaggle](https://www.kaggle.com/balaka18/email-spam-classification-dataset-csv)
## Resum
El dataset conté 5172 files, on cada fila representa un correu electronic.
El dataset conté 3002 columnes,
La primera columna indica el número de correu.
La ultima columna indica si el correu és spam o no.
Les 3000 columnes restants representen una paraula i el número de vegades que apareix aquesta paraula en el mail corresponent.

### Objectius del dataset
L'objectiu d'aquest dataset és poder classificar si un mail és spam o no, per a poder classificar-lo ho realitzarem mitjançant les paraules que apareixen en els correus.

## Experiments
Hem vist quines són les paraules que més apareixen i les que menys, la paraula que més apareix és "e" que apareix un total de 438561 vegades, mentre que la que menys apareix es "felipe" amb un total de 21 vegades.

Hem vist que el nostre dataset no contenia cap valor null.
Hem vist que les dades tenien una certa diferencia entre les que eren spam i les que no ho eren, pero no eren suficients per a dir que les dades no estan balacejades.

### Preprocessat
Al tractar-se de 3000 atributs ens és practicament impossible eliminar atributs que estiguin relacionats entre ells, es per això que simplement hem eliminat outliers i valors nulls i hem normalitzat les dades per a millorar el rendiment dels diferents models.

Com a variable X(predictores) hem escollit de la columan 2 fins la columna 3001.
Com a variable y(objectiu) hem escollit la ultima columna que contenia si un mail era spam o no.

### Model
| Model | Hiperparametres | Accuracy | F1-score | RMSE |
| -- | -- | -- | -- |
| Regressió Logística | solver: lbfgs | 96.26% | 93.22% | 0.037 |
| Random Forest | trees: 100 | 93.55% | 88.00% | 0.064 |
| Naive Bayes | modedl: MultinomialNB | 92.59% | 86.64% | 0.074 |
| SVC | kernel: lineal C:10 | 72.03% | 01.80% | 0.279 |
| -- | -- | -- | -- |

## Conclusions
El millor model que s'ha aconseguit ha estat el de regressió logística, seguit de Random Forest i Naive Bayes a un nivell molt similar els tres, ja que els tres son uns bons models quan es tracta d'una regressió binària.
El pitjor model amb diferencia ha estat el SVC, ja que aquest model és millor quan es tracta d'un problema amb dimensionalitats més altes.

## Idees per treballar en un futur
Crec que seria interesant realitzar un estudi tenint en compte altres aspectes dels correus electronics no solament les paraules.
Algun dels aspectes que podriem tenir en compte alhora de realitzar un altre estudi sobre eles correus spam serien el nombre de lletres que apareixen en majuscules en un correu, l'aparició d'emojis, les lletres de colors, aparició de signes com "%" o "!".

## Llicencia
El projecte s’ha desenvolupat sota llicència d'Arnau Cruz Gargallo.
