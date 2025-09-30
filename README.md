# Projet Active Directory / Gestion des utilisateurs

## Objectif

Mettre en place un environnement Active Directory simple dans une machine virtuelle Windows Server.
Créer un domaine, ajouter des utilisateurs et des groupes, puis appliquer une stratégie de groupe (GPO).

## Étapes réalisées

### 1. Création de la machine virtuelle

* Machine virtuelle installée sur VirtualBox avec Windows Server.
* Configuration : 4 Go RAM, 50 Go disque, réseau interne.
* **Capture :** `CreationVM.png`

### 2. Installation et connexion administrateur

* Installation de Windows Server avec interface graphique.
* Première connexion avec le compte administrateur.
* **Capture :** `LoginAdmin.png`

### 3. Création du domaine Active Directory

* Ajout du rôle AD DS.
* Promotion du serveur en contrôleur de domaine `test.local`.
* **Captures :**

  * `Capture AD DS cocher pour installation.png`
  * `creationDomain.png`

### 4. Création des utilisateurs et groupes

* Création des utilisateurs : User1 → User5.
* Création de deux groupes : **RH** et **Finance**.
* Attribution des membres aux groupes.
* **Captures :**

  * `creationUser.png`
  * `RH et menbre.png`
  * `GroupeFinance et menbre.png`

### 5. Mise en place d’une GPO

* Création d’une GPO nommée `Restriction_PC`.
* Paramètres appliqués :

  * Interdiction de l’invite de commandes (cmd).
  * Interdiction du panneau de configuration.
* **Captures :**

  * `Capture de ma gpo Restriction_Pc et ses parametre cmdbloque.png`
  * `interdire cmd.png`
  * `interdire panneaux de config.png`

### 6. Tests de la GPO

* Connexion avec un utilisateur de test (User2).
* Résultat attendu :

  * L’invite de commandes est bloquée.
  * Le panneau de configuration est inaccessible.
* **Capture :**

  * `panneau config bloque.png`

## Résultat final

* Domaine `test.local` créé et fonctionnel.
* 5 utilisateurs et 2 groupes configurés (RH, Finance).
* GPO appliquée à tous les utilisateurs avec restrictions sur cmd et panneau de configuration.
* Documentation complète avec captures disponible dans le dossier `/screenshots`.

## Captures

Toutes les captures d’écran sont disponibles dans le dossier `/screenshots`.
