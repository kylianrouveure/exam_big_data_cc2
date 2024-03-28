# Exam Big Data
## ROUVEURE Kylian

## 5 - Mise en pratique (Examen)

Pour les question 1, 2 et 4, nous avons créé un fichier de traitement en python, on enregistre puis on laisse le traitement. Puis dans les fichiers de réponses respectives, on aura le code de traitement python, la requete pour ouvrir les résultats et l'extrait des résultats.

1. **Trouvez combien de tags chaque film possède ?**

```bash
vi tags_par_utilisateur.py // Créer le fichier python

*** Copier le code qui est dans Exam-resultats/R5-1.md ***
:wq // Enregistrement du fichiers

sudo python tags_par_film.py -r hadoop --hadoop-streaming-jar /usr/hdp/current/hadoop-mapreduce-client/hadoop-streaming.jar hdfs:///data/datasets/movies-2/tags.csv -o hdfs:///data/datasets/movies-2/tags_par_film
```

Résultats :
<a href="Exam-resultats/R5-1.md" >click here</a>

2. **Trouvez combien de tags chaque utilisateur a ajoutés ?**

```bash
vi tags_par_utilisateur.py // Créer le fichier python

*** Copier le code qui est dans Exam-resultats/R5-2.md ***
:wq // Enregistrement du fichiers

sudo python tags_par_utilisateur.py -r hadoop --hadoop-streaming-jar /usr/hdp/current/hadoop-mapreduce-client/hadoop-streaming.jar hdfs:///data/datasets/movies-2/tags.csv -o hdfs:///data/datasets/movies-2/tags_par_utilisateur
```

Résultats :
<a href="Exam-resultats/R5-2.md" >click here</a>

3. **Combien de blocs occupe le fichier dans HDFS dans chacune des configurations ?**

```bash
hdfs fsck / -files -blocks
```

Requete pour avoir avoir les blocs du dossier racine du HDFS

Résultats :
```bash
Total blocks (validated):  1152 (avg. block size 2510786 B) (Total open file blocks (not validated): 1)
```

4. **Trouvez combien de fois chaque tag a été utilisé pour taguer un film ?**

```bash
vi tags_uniques_par_films.py // Créer le fichier python

*** Copier le code qui est dans Exam-resultats/R5-4.md ***
:wq // Enregistrement du fichiers

sudo python tags_uniques_par_films.py -r hadoop --hadoop-streaming-jar /usr/hdp/current/hadoop-mapreduce-client/hadoop-streaming.jar hdfs:///data/datasets/movies-2/tags.csv -o hdfs:///data/datasets/movies-2/tags_uniques_par_films
```

Résultats :
<a href="Exam-resultats/R5-4.md" >click here</a>
