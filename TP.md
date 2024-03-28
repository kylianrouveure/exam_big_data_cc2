# TP Big Data
## ROUVEURE Kylian

## 3.1 - Prise en main Commandes HDFS

<a href="TP-parties/P3-1.md" >Voir la partie</a>


## 3.2 - Importer et exporter des données

<a href="TP-parties/P3-2.md" >Voir la partie</a>


## 3.3 - Manipulation des données dans HDFS

<a href="TP-parties/P3-3.md" >Voir la partie</a>


## 3.4 - Manipulation de fichiers télécharger depuis un serveur

<a href="TP-parties/P3-4.md" >Voir la partie</a>

## 3.5 - Fichiers de configuration HDFS

<a href="TP-parties/P3-5.md" >Voir la partie</a>

## 4.1 - Préparation de la vm (MrJob, Python ...)

yum et pip sont utilisés pour installer les packages nécessaires comme MrJob, Python, et Nano.

1. **Mise à jour de la SandBox HDP**

```bash
sudo yum-config-manager --save --setopt=HDP-SOLR-2.6-100.skip_if_unavailable=true
sudo yum install https://repo.ius.io/ius-release-el7.rpm https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
```

2. **Installation de python-pip**

```bash
sudo yum install python-pip
```

3. **Installation de MrJob**

```bash
sudo pip install pathlib
sudo pip install mrjob==0.7.4
sudo pip install PyYAML==5.4.1
```

4. **Installation de Nano**

```bash
sudo yum install nano
```

## 4.2 - Execution du MapReduce en local

Le script filmEvaluation.py est exécuté en local puis sur Hadoop pour analyser un fichier de données (evaluation.data). Les résultats montrent le nombre d'évaluations par note (de 1 à 5), démontrant la capacité de MapReduce à traiter et agréger de grandes quantités de données distribuées.

1. **Récuperation du code**

```bash
wget https://github.com/juba-agoun/iut-hadoop/raw/main/filmEvaluation.py
wget https://github.com/juba-agoun/iut-hadoop/raw/main/evaluation.data

sudo python filmEvaluation.py evaluation.data
```

## 4.3 - Execution du MapReduce en local

```bash
sudo python filmEvaluation.py -r hadoop --hadoop-streaming-jar /usr/hdp/current/hadoop-mapreduce-client/hadoop-streaming.jar evaluation.data
```

Résultat
```bash
"1"     6111
"2"     11370
"3"     27145
"4"     34174
"5"     21203
```
