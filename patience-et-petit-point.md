Harroch Rina 

4IW3

28/06/22

# Test de performance sur un site à faible trafic

Projet à tester : "patience et petits points"

Groupe : Naty Ghanem, Rina-Myriam Harroch

## Préambule

- Description globale du projet: 

    Le site https://patience-et-petits-points.fr/ est un blog qui inclut une boutique en ligne. Sur le même site il y a un onglet boutique et blog.

- Objectif de l'application : 

    Le but est de vendre des patrons de broderie et des articles de mercerie comme des aiguilles ou du tissus. 
    On peut aussi laisser un commentaire sur les articles du blog pour partager des astuces.

- Type d'utilisateurs prévus :

    La cible est principalement les débutants dans la couture et les passionés.
    L'utilisateur peut faire des achats après s'être connecté ou seulement visiterle blog. 

- Toute autre information que vous jugez pertinente:

    Le but étant de vérifier le comportement du site lorsqu'il a un nombre de visiteur d'un jour normal. Etant donné que le site n'a pas un nombre de visiteur haut, un load testing est le test le plus adapté.

## Architecture de l'application

- Résumé de l'architecture globale

- Technologies/Langages utilisés
    Le site a utilisé un thème 
    - Wordpress
    - Apache 
    - Hébergé par OVH

- Composants/Services  

## Exigences du test

Nous allons donc voir si le site se comporte normalement dans des conditions normales. 
On va se concentrer sur la partie connexion/ inscription, ajout/validation du panier ainsi que l'ajout d'un commentaire.


| Business Transactions | User Load | Response Time | Transactions per hour |
|--------------|:-----------:|:------------:|:------------:|
| Access login page |  |  |  |
| Access register page |  |  | |
| Item page |  |  | |
| Cart page |  |  | |
| Delivery page |  |  | |
| Payment page |  |  | |
| Comment section |  |  | |

## Environnement de test
Environnement de test:

- CPU, Memoire : Intel Core i5-10210U CPU @ 1.60GHz   2.11 GHz, 8 Go RAM
- OS : Windows
- Software pertinent : VsCode

Aucune donné sur l'environnement de production. Aucune comparaison possible avec l'environnement de test.

## Planification des tests

1. Les limitations sont iconnues, on prendra une valeur de 500 utilisateurs
2. Comprendre/Prévoir le modèle de charge en production et l'adapter au modèle des tests.//TODO
3. Type de test nécessaire : load testing
4. Les métriques que l'on souhaite tester sont les temps de reponse dû aux nombres de connexion et vérifier l'utilisation du CPU. 
5. Les métriques qui définiront la réussite ou l'échec du test.//TODO


## 7. Etapes des tests


| Step # | Business Process Name : Product Ordering |
|--------------|:-----------:|
| 1 | Home Page |
| 2 | Login |
| 3 | Search Product |
| 4 | Add Product to Cart|
| 5 | Cart page |
| 6 | Delivery  |
| 7 | Payment |
| 8 | Add comment on the blog|
| 9 | Logout |

Le proscess necessite des données cloner de la prod.

Indiquez comment se fait la préparation de la donnée.//TODO

## 8. Execution des tests

On va se baser sur un niveau de visite de 500 utilisateurs.

| Test Run | Test Scenario Summary |
|--------------|:-----------:|
| Smoke Test | To validate the performance test scripts and monitors |
| Cycle 1 - Run 1 | Load Test - 1 Minute test with 20% of 500 users |
| Cycle 1 - Run 2 |Load Test - 1 Minute test with 50% of 500 users |
| Cycle 1 - Run 3 | Load Test - 1 Minute test with 80% of 500 users |
| Cycle 1 - Run 4 | Load Test - 1 hour test with 100% of 500 users |
| Cycle 1 - Run 5 | Load Test - 1 hour test with 100% of 500 users |
| Cycle 1 - Run 6 | Load Test - login and add a product in cart |
| Cycle 1 - Run 7 | Load Test - validate cart and do payment |
| Cycle 2 - Run 1 | Load Test - logout and login |
| Cycle 2 - Run 2 | Load Test - add a comment on the blog section |
| Cycle 2 - Run 3 | Load Test - 1 Minute test with 70% of 500 users |
| Cycle 2 - Run 4 | Load Test - 1 Minute test with 50% of 500 users |
| Cycle 2 - Run 5 | Load Test - 1 Minute test with 20% of 500 users |

//TODO
Ensuite, détaillez chaque scénario comme l'exemple suivant (pour le Load Test) :

|  | Test Details |
|--------------|:-----------:|
| **Purpose** | Peak hour transaction processing will be under examination to <br/> determine if the system can maintain response times <br/> under the highest anticipated load. <br/> This test is designed to collect performance <br/> metrics on transaction throughput, response times, <br/> and system resource utilization, <br/> in comparison to Performance requirements. |
| **No. of Tests** | 4 (2 tests per cycle) |
| **Duration** | Ramp-up: 5 minutes - Steady State: 1 hour - Ramp-down: 5 minutes |
| **Scripts** | 1. Testing cart - 2. Testing adding comment |
| **Scenario Name** | Load Test Scenario |
| **User Load / Volume** | 500 Vusers (Threads) Load |
| **Entry Criteria** | 1. The code should be stable and functionally verified <br/> 2. Test Environment should be stable and ready to use <br/> 3. Test Data should be available <br/> 4. All the NFRs should be agreed with the project <br/> 5. Test scripts should be ready to use |
| **Validation Criteria** | 1. The mean of the response time should be below 1.5 sec <br/> 2. The error rate should be below 5% |

## Résultats des tests
NaN

## Analyses et Optimisations proposées

 NaN
