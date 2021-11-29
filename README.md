# Ansible
Ce projet GITHUB correspond à un ensemble de TP autour du fonctionnement de l'outil Ansible.

Le but étant de créer une architecture de 5 serveurs avec deux serveurs webs, deux serveurs de BDD répliqués et un serveur Syslog. L'ensemble des configuration se paramétrerons majoritairement sur Ansible.

Dans le cas ou le premier serveur de base de données et le premier serveur web s'avéreraient ne plus fonctionner, le deux serveur de replication prendraient le relait et le SI fonctionnerait toujours.

Les outils utilisés pour mener à bien ce projet sont:
- Oracle VM Virtualbox 
- Ubuntu 20.10
- GIT
- Ansible
- IntelliJ
  - Plugin Ansible et GIT
- Apache
- Heartbeat
- Mariadb
- Rsyslog

Ordre d'éxécution des commandes :

Vérifier les fichiers d'inventaire "host" sous Hosts/ et la correspondance avec les serveurs appelés dans les différents playbooks.
Lancer le playbook Hosts/Playbook_Host/playbook_sshkey.yml pour permettre un accès admin sur les systèmes.

Pour les serveurs Web
- Webserver/Playbook_WEBSERVER/playbook_apache.yml
- Webserver/Playbook_WEBSERVER/playbook_php.yml
- Webserver/Playbook_WEBSERVER/playbook_glpi.yml
- Heartbeat/Playbook_Heatbeat/playbook_Heartbeat.yml

Pour les serveurs BDD
- BDD/Playbook_BDD/playbook_mariadb_conf.yml
- BDD/Playbook_BDD/playbook_iptables_ports.yml

Pour le serveur Syslog
- SYSLOG/Playbook_SYSLOG/playbook_syslog.yml


