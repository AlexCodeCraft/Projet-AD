# Projet Active Directory / Gestion des utilisateurs

## Objectif

Mettre en place un environnement Active Directory simple dans une machine virtuelle Windows Server.
Créer un domaine, ajouter des utilisateurs et des groupes, puis appliquer une stratégie de groupe (GPO).

## Étapes réalisées

### 1. Création de la machine virtuelle

* Machine virtuelle installée sur VirtualBox avec Windows Server.
* Configuration : 4 Go RAM, 50 Go disque, réseau interne.
* **Capture :** `01_Creation_VM.png`

### 2. Installation et connexion administrateur

* Installation de Windows Server avec interface graphique.
* Première connexion avec le compte administrateur.
* **Capture :** `02_Login_Admin.png`

### 3. Création du domaine Active Directory

* Ajout du rôle AD DS.
* Promotion du serveur en contrôleur de domaine `test.local`.
* **Captures :**

  * `03_ADDS_Installation.png`
  * `04_Creation_Domaine.png`

### 4. Création des utilisateurs et groupes

* Création des utilisateurs : User1 → User5.
* Création de deux groupes : **RH** et **Finance**.
* Attribution des membres aux groupes.
* **Captures :**

  * `05_Creation_Utilisateurs.png`
  * `06_Groupe_RH_Membres.png`
  * `07_Groupe_Finance_Membres.png`

### 5. Mise en place d’une GPO

* Création d’une GPO nommée `Restriction_PC`.
* Paramètres appliqués :

  * Interdiction de l’invite de commandes (cmd).
  * Interdiction du panneau de configuration.
* **Captures :**

  * `08_GPO_Restriction_PC.png`
  * `09_Interdire_Acces_Cmd.png`
  * `10_Interdire_Acces_PanneauConfig.png`

### 6. Tests de la GPO

* Connexion avec un utilisateur de test (User2).
* Résultat attendu :

  * L’invite de commandes est bloquée.
  * Le panneau de configuration est inaccessible.
* **Captures :**

  * `11_Test_User2_Cmd_Bloque.png`
  * `12_Test_User2_PanneauConfig_Bloque.png`

## Résultat final

* Domaine `test.local` créé et fonctionnel.
* 5 utilisateurs et 2 groupes configurés (RH, Finance).
* GPO appliquée à tous les utilisateurs avec restrictions sur cmd et panneau de configuration.
* Documentation complète avec captures disponible dans le dossier `/screenshots`.

## Captures

Toutes les captures d’écran sont disponibles dans le dossier `/screenshots`.
