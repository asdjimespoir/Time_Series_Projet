# Time_Series_Projet
Ventes de médicaments

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/asdjimespoir/Time_Series_Projet/main?labpath=Mini_Projet.ipynb)



## Plan du travail

Le Projet consiste à étudier la vente des médicaments et implémenter des modèles de prédictions pouvant permettre de préduire le comportement à l'avenir en fonction des comportements passés et actuels en utilisant des notions de séries temporelles.

Pour ce fait, nous allons parcourir différentes notions vues au cours allant de l'analyse basique des séries temporelles, à leurs modélisations avec différentes approches à savoir la méthode statisque et la méthode d'apprentissage profond. Mais aussi déffinir des mésures de précision permettant des voir quel modèle implémenté semble meilleur que l'autre en fonction des données que contient notre dataset.

Avant d'aller plus loin, il est important d'appréhender certaines notions liées à ce travail facilant sa compréhension.

**C'est quoi une série temporelle ou chronologique ?**

>`Une série chronologique` est définie comme une série de points de données enregistrés à différents intervalles de temps. L'ordre chronologique peut être quotidien, mensuel ou même annuel.

**Qu'entends-t-on par prévion des séries temporelles ?**

>`La prévision des séries temporelles` est le processus qui consiste à utiliser un modèle statistique pour prédire les valeurs futures d'une série temporelle sur la base des résultats passés. De manière plus simple, c'est l'étape où nous voulons prédire les valeurs futures que la série va prendre.

**Combien de catégories de prévisions existe-t-il ?**

>La prévision d'une série chronologique peut être divisée en deux grandes catégories.

* Si nous n'utilisons que les valeurs précédentes de la série temporelle pour prédire ses valeurs futures, il s'agit d'une `prévision de série temporelle univariée`.

* Si nous utilisons des prédicteurs autres que la série (comme les variables exogènes) pour prévoir, on parle de `prévision de séries temporelles multi-variées`.

**Table des matières**

1. [Analyse Fondamentale](#BasicAnalytics)
    * [Préparation des données](#DataPreparation)
    * [Visualisation des données](#DataVisualization)
    * [Séparation des donnnées](#DataSplitting)
    * [Décomposition des séries temporelles](#TimeSeriesDecomposition)

2. [Mesures de Précision pour les prévisions des séries temporelles](#AccuracyMetrics)

3. [Modélisation des séries chronologiques avec la méthode statistique](#TimeSeriesModelingwithStatisticalMethod)
    * [Naive Forecast](#NaiveForecast)
    * [Moyenne mobile exponentielle](#ExponentialMovingAverage)
        * [Moyenne mobile exponentielle simple (SEMA)](#SimpleExponentialMovingAverage(SEMA))
        * [Méthode de la moyenne mobile exponentielle Holt-Winters](#Holt-WintersMethod)
    * [ARIMA Forecast](#ARIMAForecast)
    * [SARIMA Forecast](#SARIMAForecast)
    
4. [Modélisation des séries temporelles avec le Deep Learning](#TimeSeriesModelingwithDeepLearning)
    * [Prétraitement des données](#Preprocessing)
    * [MLP](#MLP)
        * [Modélisation](#ModelingMLP)
        * [Formation](#TrainingMLP)
        * [Evaluation](#EvaluationMLP)
    * [LSTM](#LSTM)
        * [Modélisation](#ModelingLSTM)
        * [Formation](#TrainingLSTM)
        * [Evaluation](#EvaluationLSTM)

5. [Conclusion](#Conclusion)
