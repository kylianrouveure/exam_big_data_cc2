# Exam Big Data
## ROUVEURE Kylian

## 5 - Mise en pratique (Examen)

1. **Trouvez combien de tags chaque film possède ?**

```bash
hdfs dfs -put ml-25m/tags.csv data/datasets/movies-2/ //
hdfs fsck ml-25m/tags.csv -files -blocks
```

Résultats :
<a href="Exam-resultats/question-5.1.md" >click here</a>

2. **Trouvez combien de tags chaque utilisateur a ajoutés ?**

Résultats :
<a href="Exam-resultats/question-5.2.md" >click here</a>

3. **Combien de blocs occupe le fichier dans HDFS dans chacune des configurations ?**

Résultats :
<a href="Exam-resultats/question-5.3.md" >click here</a>

4. **Trouvez combien de fois chaque tag a été utilisé pour taguer un film ?**

Résultats :
<a href="Exam-resultats/question-5.4.md" >click here</a>

5. **Bonus : Trouvez pour chaque film combien de tag le même utilisateur à introduit.**

Résultats :
<a href="Exam-resultats/question-5.bonus.md" >click here</a>
