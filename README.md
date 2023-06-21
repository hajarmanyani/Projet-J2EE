<h2>Projet de fin de semestre: E-Banking App</h2>
<h2>Encadrant : Professeur Mohamed YOUSSFI<h2>
<h2>Ce projet vise à développer une application de gestion de comptes bancaires en utilisant le framework Spring Boot. L'objectif est de permettre aux utilisateurs de gérer facilement leurs comptes, effectuer des opérations de débit et de crédit, ainsi que consulter les informations relatives à leurs comptes. Le projet est structuré en deux composantes principales : la couche DAO (Data Access Object) qui gère l'accès aux données, et la couche service qui gère la logique métier, les objets de transfert de données (DTOs) et les contrôleurs REST (RestController).</h2>

<h1>Partie 01 : La couche DAO</h1>

-La création des entités JPA (Java Persistence API) est une étape essentielle dans la mise en place de la persistance des données dans une application Java. Les entités JPA représentent les classes qui sont persistées dans une base de données relationnelle, et elles permettent de manipuler ces données de manière transparente en utilisant les fonctionnalités de JPA.
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/4750544e-7137-48fb-9b6d-85dac59bbb9b)

-Utiliser la stratégie Single Table comme type d'héritage pour modéliser une hiérarchie de classes en utilisant une seule table dans la base de données pour stocker toutes les données des sous-classes
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/80a39fde-6a31-4cef-9752-277d2c8222c2)

-Ajouter interfaces AccountOperationRepository, BankAccountRepository et CustomerRepository qui héritent de l'interface JpaRepository  fournie par Spring Data. L'utilisation de l'interface 'JpaRepository' permet de bénéficier des fonctionnalités de base pour l'accès aux données, telles que les opérations CRUD (Create, Read, Update, Delete) et d'autres opérations courantes.
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/ba41c736-e66c-4a01-a3fc-0b784a11c4d0)

-Configurer la base de données 
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/cd35b01c-8d6c-443e-9647-bcceb87f9fe8)

-Visualiser les tables sur la plateforme H2 Database. En utilisant l'interface web de H2 Database,on peut facilement visualiser les tables de votre base de données H2, parcourir les données qu'elles contiennent, exécuter des requêtes SQL et effectuer d'autres opérations de gestion de la base de données.
![2](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/59589703-3872-4a94-9b46-3c02ce9a2c70)

-Ajouter les clients en utilisant l'interface BankAccountService
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/55e23512-cffc-4f09-a51e-997a86814203)

-Ajouter les comptes des deux types CurrentBankAccount et SavingBankAccount pour toute la liste des clients
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/62056e76-f386-45cb-89c6-fb8c06f0a8d7)

-Ajouter les opérations et les sauvegarder à l'aide de l'utilisation de l'interface AccountOperationRepository
![7](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/7627c787-2444-4678-a66b-ab9b7df84ab1)
![8](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/54f2c6ed-9038-43e0-8aab-19cea5d68595)

-Visualiser la liste des clients avec les informations relatives à leurs comptes et les opérations qu'ils ont effectuées
![10](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/29f6eb0b-fd08-4384-ae75-afcddaedc514)

-Visualiser les données sur la plateforme PhpMyAdmin
![mysql](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/617bb1d3-ca9e-4af8-8ad0-0fceda3102b3)

<h1>Partie 02 : Tester la couche DAO</h1>

-Créer l'interface BankAccountService afin de définir les méthodes de création de comptes et les opérations nécessaires telles que le débit, le crédit et le transfert
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/e0c79e58-3c83-4079-ab9b-6fa5fc33b140)

-Créer une classe appelée BankAccountServiceImpl pour implémenter les méthodes déjà citées
![3](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/edad1819-81f5-423c-8593-06195a3b7ccd)

-Créer des classes personnalisées au niveau du package exceptions pour générer des exceptions métier
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/2466059b-ecab-4d7d-8dbc-3a42ab21b486)

-Pour ajouter des clients, des comptes et des opérations associées en utilisant l'interface BankAccountService, on utilise une implémentation concrète de cette interface, telle que BankAccountServiceImpl. Cette classe permet de créer de nouveaux clients, de créer des comptes pour ces clients, et d'effectuer des opérations telles que les dépôts et les retraits sur les comptes existants. 
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/7dca3a8e-883d-45d7-860d-44a5a796a775)

-Créer les deux classes 'BankAccountRestApi' et 'CustomerRestApiController' au niveau du package web; La classe 'BankAccountRestApi' peut fournir des méthodes pour créer de nouveaux comptes, effectuer des dépôts et des retraits, obtenir des informations sur les comptes, etc. Cette classe peut interagir avec l'implémentation de 'BankAccountService' pour exécuter les opérations bancaires correspondantes. La classe 'CustomerRestApiController', quant à elle, peut être utilisée pour la création de nouveaux clients, la récupération des détails des clients, la mise à jour des informations des clients, etc. Cette classe peut également interagir avec l'implémentation de 'BankAccountService' pour effectuer les opérations liées aux clients.
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/c1cea7a0-da4e-4d3f-8a7b-47a6a2685901)
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/b82c7fb3-bb17-43ca-90fa-b37a3fc3fc0a)

<br>-Afficher les clients<br>
![4](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/bc35a8d0-b083-4006-ae6a-b12c2d99ef4b)

<h3>Introduire le pattern DTO</h3>

-Au niveau du package DTO, on crée des classes qui serviront à représenter les objets de transfert de données (DTO) utilisés pour échanger des informations entre différentes couches de votre application. 
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/541dc337-62fc-4433-96ef-eb54125ad11e)

<br>-Tester l'API<br>
![api-docs](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/84ba2cb0-ac5d-4ce0-aad7-c8b9c73d8339)

-Tester les méthodes de l'API sur Swagger Ui; Swagger UI est un outil pratique pour tester les méthodes de votre API REST. En accédant à l'interface Swagger UI via votre navigateur, vous pouvez explorer les différentes ressources et méthodes disponibles.
![6](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/a7491f8d-1302-4ff2-8956-fe8e8a0c030f)
![7](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/cff81f93-2b7f-443f-9dfa-7ee4f3066246)
![8](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/633d1b17-6377-4d0b-8f2b-b0b2aeebb3e3)

-Ajouter la pagination
![pagination](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/a7470b01-1165-4e7a-ba6c-cd5a8e929cf2)

<h1>Partie 03 : Client Angular</h1>

-Créer un projet angular avec l'installation de l'invite de commande d'Angular (CLI)
![1](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/c9c819ae-fbdf-49d7-829b-72d334307072)

-Pour ecécuter le projet, on exécute la commande 'ng serve' à partir de la racine du projet. Cette commande compile e code source du projet pour transpiler le code TypeScript en JavaScript et en meme temps démarre un serveur web local basé sur NodeJs pour déployer l'application localement.
![2](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/006dd050-1bcb-4945-9915-e3ab3babaeec)

-Générer les composants nécessaires à l'aide de la commande "ng g c navbar" par exemple
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/dc0388e5-d16f-45f1-93da-f7a91ba1ebf7)

-Ajouter une barre de navigation
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/cd4ebc5c-a557-4cfa-a9e9-b5eba1d78447)

-Configurer le système de routage pour naviguer entre les composants
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/e8695100-67d9-4c35-8071-ad98a4d02ac5)

-Pour afficher la liste des clients, on doit installer le module HttpClientModule pour intéragir avec la partie Backend et pouvoir charger les données
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/2c74e35b-07d4-4ec7-8c10-7cd893519d8b)

-Afficher la liste des clients à l'aide du code HTML
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/ae141a9b-8b22-42f0-9318-0157f8eb9cd4)

-Installer et utiliser CORS pour le transfert de données entre le backend et le frontend
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/28a02006-7909-4fb8-8c3c-0296ecb02c10)

-Créer les deux services appelés CustomerService et AccountService pour pouvoir les injecter dans n'importe quel composant
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/df18c451-86a7-4822-8fe2-af4096fea97e)
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/1cdd1019-d467-41fa-80e0-099fe2d4fc2a)

-Créer des classes sous le paquet models qui représentent le modèle
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/5a4723b2-be8a-44cd-8dcb-1bcea9b7ad95)
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/3859f109-a95f-4d03-a1aa-919fb86e1b1b)

-Créer un fomulaire pour la recherche des clients
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/0d3490ab-070c-42aa-bfe4-de6c22e9684f)

<h2>Test</h2>

![f1](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/9bb532df-eeef-46b3-84e5-33950f549883)

![f2](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/3ed59810-9598-4f1e-bca2-ef0b3889e421)













