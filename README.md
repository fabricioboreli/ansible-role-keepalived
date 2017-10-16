Keepalived
==========
Ansible Role para instalar e configurar Keepalived.  

Este role instala os pacotes necessários e transfere o arquivo de configuração _keepalived.conf_.

Requisitos
----------
Debian 9  

Variáveis do Role
-----------------
Arquivo de configuração:
```yaml
keepalived_config_file: "env_data/router_01/keepalived.conf.j2"
```

Dependências
------------

Nenhuma.

Playbook de exemplo
-------------------
```yaml
---
- name: Instala e configura keepalived
  hosts: router-01
  become: true
  gather_facts: true

  roles:
    - role: ansible-role-keepalived
      keepalived_config_file: "env_data/router_01/keepalived.conf.j2"
```

Licença
-------

MIT

Informações do Autor
--------------------

Fabricio Boreli  
fabricioboreli at openmailbox dot org
