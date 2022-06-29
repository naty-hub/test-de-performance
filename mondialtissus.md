28 juin 2022

Naty Ghanem 

4IW3

# Test de performance sur un site à moyen trafic 

Groupe Rina-Myriam Harroch / Naty Ghanem

Projet à tester : "Mondial tissus"

https://www.mondialtissus.fr/
## Préambule

- Description globale du projet: 

    Vente d'articles de mercerie et principalement de tissus. Il y a aussi la possibilité d'acheter des patrons ainsi que des cours de couture.

- Objectif de l'application : 

    L'objectif est de faire en sorte que les visiteurs achètent sur le site et que le site devienne la reference en terme de vente de mercerie sur internet.


- Type d'utilisateurs prévus :
    La cible est principalement les débutants ou les professionnels de la couture.
    Le site prends en compte des fonctionnalités différentes selon le statut de l'utilisateur : 
    
     - Un visiteur non connecté 
     - Un utilisateur connecté 

- Toute autre information que vous jugez pertinente :

Le but etant de vérifier les capacités de l'application à surmonté des piques d'utilisation du site. Puisque c'est un site e-commerce les utilisateurs viennent et repartent.

Le site à été developé par la société DATASOLUTION

## Architecture de l'application

- Résumé de l'architecture globale
- Technologies/Langages utilisés

    - Wordpress
    - Magento 
    - Le site est hébergé par la société ECRITEL

- Composants/Services  

## Exigences du test

Nous allons donc voir si le site arrive à performer malgré les piques de connexion. 
Pour cela on va se concentrer sur la partie connexion/ inscription et ajout/validation du panier.


| Business Transactions | User Load | Response Time | Transactions per hour |
|--------------|:-----------:|:------------:|:------------:|
| Access login page |  |  |  |
| Access register page |  |  | |
| Item page |  |  | |
| Cart page |  |  | |
| Delivery page |  |  | |
| Payment page |  |  | |

## Environnement de test
Environnement de test:

- CPU, Memoire : Intel Core i5-10210U CPU @ 1.60GHz   2.11 GHz, 8 Go RAM
- OS : Windows
- Software pertinent : VsCode

Aucune donné sur l'environnement de production. Aucune comparaison possible avec l'environnement de test.

## Planification des tests

1. Les limitations sont iconnues.
2. Comprendre/Prévoir le modèle de charge en production et l'adapter au modèle des tests.//TODO
3. Type de test nécessaire : spike testing
4. Les métriques que l'on souhaite tester sont les temps de reponse dû à de grosse quantité de connexion pour déterminer si le site fonctionne bien et vérifier l'utilisation du CPU. 
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
| 8 | Logout |

Le proscess necessite des données cloner de la prod.

Indiquez comment se fait la préparation de la donnée.//TODO

## 8. Execution des tests


| Test Run | Test Scenario Summary |
|--------------|:-----------:|
| Smoke Test | To validate the performance test scripts and monitors |
| Cycle 1 - Run 1 | Load Test - 1 Hour test with peak load |
| Cycle 1 - Run 2 | Repeat Load Test - 1 Hour test with peak load |
| Cycle 1 - Run 3 | Stress Test - 1 Hour test with 150% of peak load |
| Cycle 2 - Run 1 | Load Test - 1 Hour test with peak load |
| Cycle 2 - Run 2 | Repeat Load Test - 1 Hour test with peak load |
| Cycle 2 - Run 3 | Stress Test - 1 Hour test with 150% of peak load |

//TODO
Ensuite, détaillez chaque scénario comme l'exemple suivant (pour le Load Test) :

|  | Test Details |
|--------------|:-----------:|
| **Purpose** | Peak hour transaction processing will be under examination to <br/> determine if the system can maintain response times <br/> under the highest anticipated load. <br/> This test is designed to collect performance <br/> metrics on transaction throughput, response times, <br/> and system resource utilization, <br/> in comparison to Performance requirements. |
| **No. of Tests** | 4 (2 tests per cycle) |
| **Duration** | Ramp-up: 5 minutes - Spiky State: 1 hour - Ramp-down: 5 minutes |
| **Scripts** | 1. spikes between two hours |
| **Scenario Name** | Spike Test Scenario |
| **User Load / Volume** | 1 000 Vusers (Threads) Load |
| **Entry Criteria** | 1. The code should be stable and functionally verified <br/> 2. Test Environment should be stable and ready to use <br/> 3. Test Data should be available <br/> 4. All the NFRs should be agreed with the project <br/> 5. Test scripts should be ready to use |
| **Validation Criteria** | 1. The mean of the response time should be below 1.5 sec <br/> 2. The error rate should be below 5% |

## Résultats des tests
NaN

## Analyses et Optimisations proposées

 NaN
