[![l3d.pretix.pretix](https://ansible.l3d.space/svg/l3d.pretix.pretix_ansible-role.svg)](https://galaxy.ansible.com/ui/repo/published/l3d/pretix/content/role/pretix/)
[![License](https://ansible.l3d.space/svg/l3d.pretix_license_collection.svg)](LICENSE)
[![Maintainance](https://ansible.l3d.space/svg/l3d.pretix_maintainance_collection.svg)](https://ansible.l3d.space/#l3d.pretix)

 Pretix Ansible Role
=====================

Ansible role ``l3d.pretix.pretix`` to install and configure [pretix](https://github.com/pretix/pretix.git), a Ticket shop application for conferences, festivals, concerts, tech events, shows, exhibitions, workshops, barcamps, etc.

This role is part of the l3d.pretix Collection. [![collection l3d.pretix](https://ansible.l3d.space/svg/l3d.pretix_ansible-collection_collection.svg)](https://galaxy.ansible.com/ui/repo/published/l3d/pretix/)

Please note, there are other roles in this collection that are needed to install all requirements for pretix.

 Requirements
--------------
- [![l3d.pretix.postgres](https://ansible.l3d.space/svg/l3d.pretix.postgres_ansible-role.svg)](https://galaxy.ansible.com/ui/repo/published/l3d/pretix/content/role/postgres/) or a postgres database for pretix
- [![l3d.pretix.nodejs](https://ansible.l3d.space/svg/l3d.pretix.nodejs_ansible-role.svg)](https://galaxy.ansible.com/ui/repo/published/l3d/pretix/content/role/nodejs/) or nodejs for pretix
- [![l3d.pretix.redis](https://ansible.l3d.space/svg/l3d.pretix.redis_ansible-role.svg)](https://galaxy.ansible.com/ui/repo/published/l3d/pretix/content/role/redis/) or redis for pretix

 Variables
----------

| Variable | Value | Description |
| --- | --- | --- |
| ``pretix__user`` | ``pretix`` | Unix User for Pretix |
| ``pretix__group`` | pretix__user | Unix Group for Pretix |
| ``pretix__home`` | ``/var/lib/pretix`` | Unix home for pretix |
| ``pretix__data`` | ``/var/pretix`` | Pretix data root path |
| ``pretix__name`` | ``My Pretix`` | Pretix Server Name |
| ``pretix__address`` | ``https://{{ inventory_hostname }}`` | Pretix Web-Address |
| ``pretix__currency`` | ``EUR`` | default currency |
| ``pretix__datadir`` | ``{{ pretix__data }}/data`` | Pretix Application-Data |
| ``pretix__db_backend`` | ``postgresql`` | Database backend *(only postgres is tested)* |
| ``pretix__db_name`` | ``pretix`` | Database name |
| ``pretix__db_user`` | ``pretix`` | Database User |
| ``pretix__db_password`` | | Your secure database password |
| ``pretix__db_host`` | ``localhost`` | Postgres Server |
| ``pretix__web_workers`` | ``5`` | Web Workers for Pretix |
| ``pretix__web_loglevel```| ``info`` | Log Level |
| ``pretix__web_bind`` | ``127.0.0.1:8345`` | Webserver bind - TLS reverse proxy recomended |
| ``pretix__web_oncalendar`` | ``*-*-* *:00:00`` | Pretix Cron time |
| ``pretix__web_timer_delay`` | ``1800`` | Pretix Cron random delay |
| ``submodules_versioncheck`` | ``false`` | Optional versioncheck |

 Author
--------
L3D <l3d@c3woc.de> and Contibutors
