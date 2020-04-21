Role Name
=========

Ce role permet d'installer l'antivrius Clamav sur une machine Centos

Requirements
------------
Testé sur Centos 7


Role Variables
--------------

update_pkg: à mettre **True** pour mettre à jour les paquets du système.
freshclam_cron (optionnel): pour personaliser le cron freshclam

Autres variables sont indiquées dans default/main.yml avec des exemples de valeurs possibles.


**Remarque :** Toutes les variables sont facultatives. Si aucune n'est choisie, l'installation se fait avec les configurations par défaut.

Dependencies
------------
Le rôle peut être intégré facilement dans d'autres projets. Pour ce faire :
- créer un fichier **requirements.yml** avec le contenu ci-dessous :
```
---
- name : auditd
  src : https://github.com/tassyk/ansible-clamav.git
  scm: git
  version : origin/master
```
- Installer le rôle avec ansible Galaxy :
```
ansible-galaxy install -r requirements.yml -p /chemin/repertoire/roles
```
Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      remote_user: user
      become: True
      roles:
      - ansible-clamav

Exemple d'exécution du playbook :
```
ansible-playbook clamav.yml -i hosts -u user
```

License
-------

BSD

Author Information
------------------
Tassyk
