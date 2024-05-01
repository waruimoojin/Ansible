<<<<<<< HEAD
# Projet DevOps - Déploiement Automatisé avec Ansible

# Auteur
Chakib Ayan

## Description
Ce projet vise à automatiser le déploiement de deux environnements distincts (production et staging) en utilisant Ansible. Les environnements comprennent un serveur web (nginx), une base de données (MySQL) et PHP. Une page PHP "Hello World" est déployée sur chaque environnement, avec une connexion réussie à la base de données pour vérifier la fonctionnalité de l'environnement.

## Structure du Projet
- **ansible.cfg**: Fichier de configuration Ansible.
- **inventory**: Fichier d'inventaire Ansible définissant les serveurs dans les environnements de production et de staging.
- **production.yml**: Playbook Ansible principal pour le déploiement des environnements.
- **vars/credentials.yml**: Fichier chiffré contenant les informations sensibles comme les noms d'utilisateur et les mots de passe pour MySQL.
- **files/**: Contient les fichiers de configuration et les templates utilisés par les rôles Ansible.


## Instructions d'Utilisation
1. Cloner le dépôt depuis GitHub :
  
   git clone https://github.com/waruimoojin/Ansible.git
   
   
3. Exécuter le playbook Ansible en spécifiant le mot de passe pour déchiffrer les informations sensibles :
   
   ansible-playbook -i inventory/hosts.ini --extra-vars="env=staging" staging.yml --ask-become-pass --ask-vault-pass
   ansible-playbook -i inventory/hosts.ini --extra-vars="env=production" production.yml --ask-become-pass --ask-vault-pass

   les mots de passe sont : 123456
   

=======
# Ansible
>>>>>>> d72b48a (project done)
