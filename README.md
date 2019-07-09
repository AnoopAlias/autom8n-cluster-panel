# autom8n-cluster-panel
StandAlone Autom8n WebOps control panel

#Core Features

Servers: 

Apache httpd

Nginx 

gdnsd

MariaDB

MaxScale

Redis

Unison

Csync2

Netdata

Firehol

Borg/Borgmatic backups

Vsftpd

Deployed using Ansible 

Email is not a planned feature for now as users are encouraged to use Cloud Email services like GoogleMail / Hosted Outlook etc
In future if this is required we will use PostFix+Dovecot + dsync/dovecot-sync 

# Design


The control panel will use 

BACKEND
------------
Python Celery+RabbitMQ (as a task queue) Coupled with Ansible for Idempotent execution of tasks, The celery works will run as root and accept tasks submitted from a non privileged web application

FRONTEND
------------
Python Flask UI and a Python Flask REST api providing end user/api control 



