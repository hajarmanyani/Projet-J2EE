<h2>Ce projet vise à développer une application de gestion de comptes bancaires en utilisant le framework Spring Boot. L'objectif est de permettre aux utilisateurs de gérer facilement leurs comptes, effectuer des opérations de débit et de crédit, ainsi que consulter les informations relatives à leurs comptes. Le projet est structuré en deux composantes principales : la couche DAO (Data Access Object) qui gère l'accès aux données, et la couche service qui gère la logique métier, les objets de transfert de données (DTOs) et les contrôleurs REST (RestController).</h2>

<h1>Partie 01 : La couche DAO</h1>

-La création des entités JPA (Java Persistence API) est une étape essentielle dans la mise en place de la persistance des données dans une application Java. Les entités JPA représentent les classes qui sont persistées dans une base de données relationnelle, et elles permettent de manipuler ces données de manière transparente en utilisant les fonctionnalités de JPA.
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/4750544e-7137-48fb-9b6d-85dac59bbb9b)

-Utiliser la stratégie Single Table comme type d'héritage pour modéliser une hiérarchie de classes en utilisant une seule table dans la base de données pour stocker toutes les données des sous-classes
![image](https://github.com/hajarmanyani/Projet-J2EE/assets/93662714/80a39fde-6a31-4cef-9752-277d2c8222c2)

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









