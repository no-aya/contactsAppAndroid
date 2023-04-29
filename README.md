# My Contacts : Application Android

## Description
Cette application permet de gérer ses contacts. Ces contacts sont gérés dans une bd Firebase. Il suffit d'accéder à l'application avec ses coordonnées d'authentification.


https://user-images.githubusercontent.com/106016869/235281801-0123f77f-cc59-4e70-b3e9-f28efe610d4b.mp4


## Entités
- Contact
Chaques contacts possède les attributs suivants :
```java
    String contactemail, contactname, contactnumber, imageURL;
```

`imagesURL` est l'url de l'image du contact. Cette image est stockée dans le storage de Firebase.

- User
Chaque utilisateur possède les attributs suivants :
```java
    String email, name, password;
```

## Firebase
### Configuration
Pour commencer avec Firebase il faut d'abord obtenir la clé de l'application. Sur Android Studio, il faut se rendre dans Gradle, signinreport, puis double cliquer sur `signingReport`. La clé est affichée dans la console.

Il faut ensuite créer un projet sur Firebase.

Pour effectuer la relation entre l'application et la base de données, il faut ajouter le fichier `google-services.json` dans le dossier `app` du projet Android Studio.

Puis il faut ajouter les dépendances suivantes dans le fichier `build.gradle` du projet :
```java
    classpath 'com.google.gms:google-services:4.3.3'
```

Et dans le fichier `build.gradle` du module `app` :
```java
    implementation 'com.google.firebase:firebase-auth:19.3.1'
    implementation 'com.google.firebase:firebase-database:19.3.0'
    implementation 'com.google.firebase:firebase-storage:19.1.1'
```

### Console
Pour accéder à la console Firebase, il faut se rendre sur le site suivant : [Firebase](https://console.firebase.google.com/u/0/)

![image](https://user-images.githubusercontent.com/106016869/235281596-2bc99cdb-7ed8-412c-83c1-ef6edd947aed.png)

## Fonctionnalités
### Authentification
L'authentification est gérée par Firebase. L'utilisateur peut se connecter ou s'inscrire. Il peut également se déconnecter.

L'authefication est gérée par la classe `LoginActivity`.

### Signup
L'inscription est gérée par Firebase. L'utilisateur doit renseigner son nom, son email et son mot de passe. Il peut également choisir une image de profil.

L'inscription est gérée par la classe `RegisterAccount`.

### Contacts
Les contacts sont gérés par Firebase. L'utilisateur peut ajouter, modifier ou supprimer un contact. Il peut également choisir une image de profil pour le contact.

Les contacts sont gérés par la classe `ContactAdapter`.
- Ajout : `AddContact`

## Interfaces

### Login
![image](https://user-images.githubusercontent.com/106016869/235281726-807655e8-ab73-4a49-9123-92cd64c657be.png)


### Register
![image](https://user-images.githubusercontent.com/106016869/235281746-1d9b10d7-04cb-48b0-8227-0b7dc099d7a9.png)


### Contacts
![image](https://user-images.githubusercontent.com/106016869/235281770-a0a0a985-bc13-40fd-b659-1cd75d986068.png)


### AddContact
![image](https://user-images.githubusercontent.com/106016869/235281782-595d6849-829d-488b-8796-0b67b21ff996.png)


---



