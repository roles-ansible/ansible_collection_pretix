[![l3d.pretix.postgres](https://ansible.l3d.space/svg/l3d.pretix.postgres_ansible-role.svg)](https://galaxy.ansible.com/ui/repo/published/l3d/pretix/content/role/postgres/)
[![License](https://ansible.l3d.space/svg/l3d.pretix_license_collection.svg)](LICENSE)
[![Maintainance](https://ansible.l3d.space/svg/l3d.pretix_maintainance_collection.svg)](https://ansible.l3d.space/#l3d.pretix)

 Pretix Ansible Role
=====================

Ansible role ``l3d.pretix.postgres`` to install postgres for our pretix installation.

This role is part of the l3d.pretix Collection. [![collection l3d.pretix](https://ansible.l3d.space/svg/l3d.pretix_ansible-collection_collection.svg)](https://galaxy.ansible.com/ui/repo/published/l3d/pretix/)

 Requirements
--------------
None

 Variables
----------

| Variable | Value | Description |
| --- | --- | --- |
│ ``postgres__user`` | ``pretix`` | Pretix Database User |
│ ``postgres__database`` | ``pretix`` | Pretix Database Name |
│ ``postgres__password`` | | Set your secure postgres password. Make sure you use this password at the l3d.pretix.pretix role too.
| ``submodules_versioncheck`` | ``false`` | Optional versioncheck |

 Author
--------
L3D <l3d@c3woc.de> and Contibutors
