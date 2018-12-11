# Guide d’utilisation de l’application

- [Règles de fonctionnement général](#reglesgeneral)
- [Onglet 1 : Accueil](#onglet1) 
- [Onglet 2 : Graphiques et données](#onglet2) 
- [Onglet 3 : Modèle démographique](#onglet3) 
    - [Menu de gauche](#onglet3menu)
    - [Bloc 1 : Évolution chronologique](#onglet3bloc1)
    - [Bloc 2 : Comparaison par campagne](#onglet3bloc2)
    - [Bloc 3 : Représentation mensuelle par catégorie](#onglet3bloc3)
- [Onglet 4 : Méthodes de prévision](#onglet4) 


--------------------------


## <div id="reglesgeneral">Règles de fonctionnement général</div>

L'accès public (non connecté) est possible. Cependant il donne mois d'accès que les autres types d'accès. 
De manière générale, l'accès public ne permet pas de visualiser les résultats du modèle de prévision, ni de télécharger les données. 

Les règles d'accès sont définies par login, par l'administrateur de l'application.
> Eva Groshens  : <Eva.Groshens@idele.fr>

De manière générale, tout ce qui est présenté dans ce guide et qui concerne autre chose que les données observées non transformées (résultats du modèle, calculs spécifiques, ...) ne seront pas accessibles pour un utilisateur non connecté. 

--------------------------

## <div id="onglet1">Onglet 1 : Accueil</div>

Cet onglet présente le projet Modemo ainsi que l'application de mise à disposition des résultats du modèle développé pour ce projet. 

On y trouve également les notes de mise à jour, qui seront alimentées au fur et à mesure (nouvelles données disponibles, méthode de prévision améliorée, ...).

--------------------------

## <div id="onglet2">Onglet 2 : Graphiques et données</div>

Via cet onglet, on peut visualiser les données issues du projet MODEMO, par des graphiques ou des tableaux. 
Le menu de gauche permet de sélectionner les composantes du modèle de prévision à représenter. 
La page principale présente trois blocs de graphique et données. Ces blocs peuvent se plier/déplier en utilisant le bouton en haut à droite du bloc.

### <div id="onglet3menu">Menu de gauche : Options de filtre sur les composantes du modèle</div>


- Périmètre
- Race
- Indicateur
- Détail des catégories concernées par l’indicateur
- Nombre de mois de l'horizon de prévision [1-12] - *si autorisé*

![menu gauche](img/bloc_gauche.png)

Le choix du périmètre influe sur la liste des races : ne sont affichées que les races pour lesquelles on a des données dans ce périmètre (i.e. pour lesquelles la prévision a été jugée pertinente et calculée).
Attention, compte tenu des imports/exports, le périmètre France n'est pas une somme des autres périmètres.

Il est possile de **sélectionner plusieurs races** en cliquant sur plusieurs d'entre elles dans la liste déroulante. 

<span style="color:#b30000">**Attention cela peut être long. Il est conseillé, jusqu'à la fin du chargement des données correspondant à la liste des races choisies, de ne pas modifier d'autre paramètres. Dans certains cas, cela cause un chargement infini : le graphique s'affiche, se recharge, puis s'affiche, et se recharge, ... Si cela arrive, il faut redémarrer l'application (rafraichir la page).**</span>

Les indicateurs proposés sont ceux autorisés pour le profil (public si non connecté). Le choix de l'indicateur influe sur la liste des catégories proposées en dessous. En effet, les catégories affichées sont celles présentes dans les données, correspondant à l'indicateur choisi. Ce sont les niveaux de détail disponibles.

### <div id="onglet3bloc1">Bloc 1 : Évolution chronologique</div>

Ce bloc contient un graphique et une table de données qui permettent de faire une **analyse historique** des composantes du modèle, ainsi que d'évaluer la qualité du modèle proposé en observant les rétro-simulations.
Pour un accès public, seules quelques composants du modèle sont proposées mais il ne sera pas possible d'analyser la qualité du modèle car c'est réservé à des utilisateurs avertis. 

Les valeurs affichés à l'écran, sont en fait une somme ou une moyenne pondérée (selon la pertinence) de l'indicateur sur les categories sélectionnées (menu de gauche).  
Les effectifs sont sommés, tandis que les taux et ratios sont rendus en moyenne pondérée par l'effectif de référence. 

![bloc 1](img/bloc1.png)

**Options :**
>
>- il est possible de choisir la période d'affichage du graphique et des données grace au slider.
- en modifiant les paramètres sous le graphique, il est possible de changer les couleurs et d'afficher : 
    - les retro-simulations
    - les prévisions
    - les moyenne mobile = -+5 mois
    - les médianes par mois sur les 24 mois précédents
    - les médianes par mois sur les 36 mois précédents
    - les prévisions selon les autres scénarios précalculés.

### <div id="onglet3bloc3">Bloc 2 : Comparaison par campagne</div>

Ce bloc contient un graphique et une table de données qui permettent de comparer des campagnes entre elles.

Les données sont sensiblement les même que sur le bloc précédent, mais présentées différemment : les valeurs affichés à l'écran, sont en fait une somme ou une moyenne pondérée (selon la pertinence) de l'indicateur sur les categories sélectionnées (menu de gauche). 
Les effectifs sont sommés, tandis que les taux et ratios sont rendus en moyenne pondérée par l'effectif de référence. 

Le tableau de données affiche la valeur affichée sur le graphique (N) ainsi que la valeur un an plus tôt si elle existe (<span style="color:#F00">NA</span> sinon), ainsi que le taux de variation entre les 2. 

![bloc 2](img/bloc2.png)

**Options :**
>
>- Il est possible de choisir la période d'affichage du graphique et des données grace aux cases à cocher indiquant les campagnes disponibles dans les données.
- en modifiant les paramètres sous le graphique, il est possible de changer les couleurs et :
    - choisir le mois de début de la campagne
    - choisir quoi afficher : les valeurs historiques (observées) ainsi que les prévisions (par défaut ou scénarios précalculés).

### <div id="onglet3bloc3">Bloc 3 : Représentation mensuelle par catégorie</div>

Ce bloc contient un graphique et un tableau de données qui permettent de visualiser les données des composantes du modèle en détail. En effet, pour la région, la race, l'indicateur et les catégories choisies dans le menu de gauche, il est représenté ici les données détaillées contenues dans les données par catégorie. 

Le graphique permet de comparer plusieurs dates (pour un mois données, on peut comparer plusieurs années).

Le tableau montre les valeurs présentes sur le graphique, ainsi que l'évolution entre les dates s'il y a deux années sélectionnées. 

![bloc 3](img/bloc3.png)

--------------------------

## <div id="onglet3">Onglet 3 Modèle démographique</div>

Dans cet onglet, on trouve le fonctionnement général du modèle de prévision développé pour le projet MODEMO. 

<span style="color:#F00">TODO dès mise à jour EVA</span>

--------------------------

## <div id="onglet4">Onglet 4 Méthodes de prévision</div>

Dans cet onglet, on trouve les méthodes de prévisions utilisées par le modèle de prévision.

Le tableau présente les mises à jour des méthodes pour chaque indicateur. 

Les sections en dessous explicitent chaque méthode.

Il est présenté ici les différents scénarios, qui correspondent à des conbinaisons de méthodes différentes. 


