28 juin 2022

Naty Ghanem 

4IW3

# Test de performance sur un site à moyen trafic  

Groupe Rina-Myriam Harroch / Naty Ghanem

Projet à tester : "Fnac"

https://www.fnac.com/

## Préambule

- Description globale du projet: 

    Le site Fnac est une grande chaîne française de vente au détail de produits culturels et électroniques.

- Objectif de l'application : 

    Vendre des produits de type electronique et culturels tels que des livres, cd, jeux videos, consoles, télévision ...
    Il y a donc un concept de panier et achat avec des utilisateurs loggé.

- Type d'utilisateurs prévus :

    Utilisateurs avec une fibre culturels et connecté. Ciblage d'une clientèle majoritairement jeune adulte.

- Toute autre information que vous jugez pertinente:
    Le but etant de vérifier les capacité maximales du site. Etant donné que le site est habitué à des connexions moyennes et aussi à des piques de connexion dû au fuseau horaire.



## Architecture de l'application

### Architecture globale Technologies/Langages utilisés Composants/Services 

- Front ReactJs
- Back .Net (#C)
- Serveur IBM
- Plan du site: https://www.fnac.com/navigation/plan.aspx#bl=footer

## Exigences du test

Nous allons donc voir où se situe le breaking point du stress testing. 
Pour illustrer, un drop de la toute nouvelle Playstation 6 vient d'être mis sur le site.
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
2. Le modele de charge en production n'est pas connu. Cela rend difficle de l'adapter au modele de test.
3. Type de test nécessaire : stress testing
4. Les métriques que l'on souhaite tester sont les temps de reponse dû à de grosse quantité de connexion pour déterminer à quel moment le site crash et vérifier l'utilisation du CPU. 
5. Les métriques qui définiront la réussite ou l'échec du test:
    - Processor Usage
    - Memoru use
    - Memory pages/second
    - CPU interrupts per second
    - Response Time


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


## 8. Execution des tests

On va se baser sur une echelle de 10 000 utilisateurs puisque c'est la connection moyenne du site

| Test Run | Test Scenario Summary |
|--------------|:-----------:|
| Smoke Test | To validate the performance test scripts and monitors |
| Cycle 1 - Run 1 | Stress Test - 1 Minute test with 50% of 10 000 users |
| Cycle 1 - Run 2 |Stress Test - 1 Minute test with 100% of 10 000 users |
| Cycle 1 - Run 3 | Stress Test - 1 Minute test with 500% of 10 000 users |
| Cycle 1 - Run 4 | Stress Test - 1 Minute test with 1000% of 10 000 users |
| Cycle 1 - Run 5 | Stress Test - 1 Minute test with 5000% of 10 000 users |
| Cycle 1 - Run 6 | Stress Test - 1 Minute test with 10000% of 10 000 users |


|  | Test Details |
|--------------|:-----------:|
| **Purpose** | Peak user transaction processing will be under examination to <br/> determine when the system cannot maintain response times <br/> under the highest load. <br/> This test is designed to collect performance <br/> metrics on transaction throughput, response times, <br/> and system resource utilization until the website crash, <br/> in comparison to Performance requirements. |
| **No. of Tests** |  6 levels of number of visitors |
| **Duration** | Ramp-up: 2 minutes - Ramp-down: 2 minutes |
| **Scripts** | 1. load the highest number user |
| **Scenario Name** | Stress Test Scenario |
| **User Load / Volume** | 10 000 Vusers (Threads) Load |
| **Entry Criteria** | 1. The code should be stable and functionally verified <br/> 2. Test Environment should be stable and ready to use <br/> 3. Test Data should be available <br/> 4. All the NFRs should be agreed with the project <br/> 5. Test scripts should be ready to use |
| **Validation Criteria** | 1. The mean of the response time should be over 1.5 sec <br/> 2. The error rate should be over 5% |

## Résultats des tests
NaN

## Analyses et Optimisations proposées

 NaN

