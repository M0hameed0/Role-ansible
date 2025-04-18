# Rôle Ansible pour déployer une application Node.js avec PostgreSQL

## Description

Ce rôle déploie une application Node.js avec une base de données PostgreSQL sur un serveur Rocky Linux. Il configure tous les éléments nécessaires, installe Node.js, configure PostgreSQL, et déploie l'application. Ce rôle est conçu pour être simple à utiliser et rapide à configurer.

## Prérequis

- Une machine avec Rocky Linux 8 ou 9
- Ansible 2.9 ou plus
- Accès sudo sur le serveur cible

## Variables

Aucune variable n'est nécessaire pour le moment. Vous pouvez personnaliser l'application via le dépôt GitHub lié.


## Exemple d'utilisation

il faut cloner le repos GITHUB : https://github.com/franklin-tutorials/quiz-ansible  dans /root/config/

il faut deplacer le fichier site.yml dans le dossier playbooks
voilà l'architecture finale de projet :

/root/config/
  ├── ansible.cfg
  ├── inventaire
  ├── quiz-ansible/
  ├── playbooks/
  │   └── site.yml  (le playbook principal)
  └── roles/
      └── app/  (le rôle 'app' ici)
          ├── defaults/
          ├── files/
          ├── handlers/
          ├── meta/
          ├── tasks/
          ├── templates/
          ├── tests/
          ├── vars/


##  Execution de Playbook site.yml 
pour lancer le playbook voilà la commande : ansible-playbook -i /root/config/inventaire /root/config/playbooks/site.yml 
