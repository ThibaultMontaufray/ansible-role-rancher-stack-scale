RANCHER SCALE STACK
===================

This roles scale a stack in rancher

Example Playbook
----------------

Here is a use case :

```yaml
  - hosts: servers
    remote_user: mysuperadmin
    vars:
     - servive_fqdn: "web.site"
     - service_scale: 2
     - rancher_api_key: "admin"
     - rancher_api_secret: "r@nch3r!"
     - rancher_project_name: "myproject"
     - hostmaster: "{{ hostvars[groups['rancher-master'][0]]['ansible_default_ipv4']['address'] }}"
     - rancher_url: "http://{{ hostmaster }}:8080"
  - roles:
     - ansible-role-rancher-scale-stack
```

License
-------

MIT
