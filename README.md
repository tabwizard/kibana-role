Kibana Role
=========

Устанавливает и настраивает Kibana

Requirements
------------

Поддерживаются только ОС семейств debian и EL.

Role Variables
--------------

|   Variable name   |   Default   |   Description                                                      |
|-------------------|-------------|--------------------------------------------------------------------|
| kibana_version    | "7.14.0"    | Параметр, который определяет какой версии kibana будет установлена |
| server_host       | 0.0.0.0     | Адрес по которому будет доступен сервер Kibana                     |
| elastic-instance  | "{{ hostvars['el-instance']['ansible_facts']['default_ipv4']['address'] | default('0.0.0.0') }}" | Адрес хоста с Elasticsearch                                        |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- name: Install Kibana
    hosts: servers
    roles:
    - role: kibana-role
        vars:
        elastic-instance: 1.2.3.4

```

License
-------

MIT

Author Information
------------------

Andrey Pirozhkov tabwizard@gmail.com.
