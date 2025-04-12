[![collection l3d.pretix](https://ansible.l3d.space/svg/l3d.pretix_ansible-collection_collection.svg)](https://galaxy.ansible.com/ui/repo/published/l3d/pretix/)
[![Maintainance](https://ansible.l3d.space/svg/l3d.pretix_maintainance_collection.svg)](https://ansible.l3d.space/#l3d.pretix)
[![License](https://ansible.l3d.space/svg/l3d.pretix_license_collection.svg)](LICENSE)

 Ansible Collection - l3d.pretix
============================

This is the Ansible Collection ``l3d.pretix``. A collection to to install pretix-ui on linux servers.
It is inspired by [this install guide](https://docs.pretix.eu/en/latest/admin/installation/manual_smallscale.html) from docs.pretix.eu.

## Ansible Roles in l3d.pretix
- [![l3d.pretix.pretix](https://ansible.l3d.space/svg/l3d.pretix.pretix_ansible-role.svg)](https://galaxy.ansible.com/ui/repo/published/l3d/pretix/content/role/pretix/) - Ansible role to install pretix
- [![l3d.pretix.postgres](https://ansible.l3d.space/svg/l3d.pretix.postgres_ansible-role.svg)](https://galaxy.ansible.com/ui/repo/published/l3d/pretix/content/role/postgres/) - Ansible role to install postgres - optimized for pretix
- [![l3d.pretix.nodejs](https://ansible.l3d.space/svg/l3d.pretix.nodejs_ansible-role.svg)](https://galaxy.ansible.com/ui/repo/published/l3d/pretix/content/role/nodejs/) - Ansible role to install nodejs - optimized for pretix
- [![l3d.pretix.redis](https://ansible.l3d.space/svg/l3d.pretix.redis_ansible-role.svg)](https://galaxy.ansible.com/ui/repo/published/l3d/pretix/content/role/redis/) - Ansible role to install redis - optimized for pretix

## Hint
The roles ``l3d.pretix.nodejs``, ``l3d.pretix.postgres`` and ``l3d.pretix.redis`` are needed to install all requirements for Pretix. The You can install pretix using ``l3d.pretix.pretix``.

## Using this Collection
You can install the collection using ansible-galaxy by running:
```bash
ansible-galaxy collection install l3d.pretix:1.0.1
```

Remember you can to Upgrade to the latest version of the l3d.pretix collection using the ``--upgrade`` parameter:
```bash
ansible-galaxy collection install l3d.pretix --upgrade
```

Or you could clone this collection in your local ansible project for example to ``collections/ansible_collections/l3d.pretix/``. Make sure you checkout [git submodules](https://git-scm.com/docs/git-submodule) too. Example:
```
# Clone git Repo with submodules to specified path
git clone --recursive https://github.com/roles-ansible/ansible_collection_pretix.git collections/ansible_collections/l3d/pretix/

# change directory
cd collections/ansible_collections/l3d.pretix/

# optionally init git submodules
git submodule update --init --recursive

# optionally install all requirements
ansible-galaxy collection install -r requirements.yml --upgrade
```

You can also list a collection in ``requirements.yml``:
```yaml
---
collections:
  - name: l3d.pretix
    version: ">=1.0.1"
```

## Example Playbook
Example Playbook to install Pretix:

```yaml
---
- name: Setup Pretix at pretix.example.org
  hosts: pretix.example.org
  become: true
  roles:
    - {role: l3d.pretix.postgres, tags: pretix}
    - {role: l3d.pretix.redis, tags: pretix}
    - {role: l3d.pretix.nodejs, tags: pretix}
    - {role: l3d.pretix.pretix, tags: pretix}
  vars:
    pretix__db_password: 'T0ll3s_P@ssw0rt'
```

## Requirements
The roles in this collection using the ``community.general`` and ``community.postgresql`` ansible Collections.

 Author
--------
L3D <l3d@c3woc.de> and Contibutors
