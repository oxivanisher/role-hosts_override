hosts_override
==============

Add and remove some hosts to `/etc/hosts`.

Role Variables
--------------

| Name          | Comment                              | Default value |
|---------------|--------------------------------------|---------------|
| hosts_override_local_domain  | Domain for localhost entries i.e. `example.lan` | `local`          |
| hosts_override_add  | List of hosts and IPs to be added containing hostname, IP key pairs. | `[]`          |
| hosts_override_remove  | List of hosts and IPs to be removed containing hostname, IP key pairs. | `local`          |

This is a example config:

```yaml
hosts_override_local_domain: example.lan
hosts_override_add:
  hosta: 10.0.0.5
  hosta: 10.0.0.6
hosts_override_remove:
  oldhost: 10.0.0.7
```

Example Playbook
----------------
```yaml
- name: Configure hosts override
  hosts: road_warrior
  collections:
    - oxivanisher.linux_base
  roles:
    - role: oxivanisher.linux_base.hosts_override
```

License
-------

BSD

Author Information
------------------

This role is part of the [oxivanisher.linux_base](https://galaxy.ansible.com/ui/repo/published/oxivanisher/linux_base/) collection, and the source for that is located on [github](https://github.com/oxivanisher/collection-linux_base).
