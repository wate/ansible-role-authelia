authelia
=================

Setup Authelia(work in progress)

OS Platform
-----------------

### Debian

- bookworm
- bullseye

Role Variables
--------------

### [defaults/main.yml](defaults/main.yml)

設定方法の詳細については[defaults/main.yml](defaults/main.yml)のサンプルコードなどを参照してください。

#### `authelia_version`

インストールするバージョン

#### `authelia_users`

ユーザーデータベース  
※Authentication Backend が`file`の場合のみ有効

#### `authelia_cfg`

Autheliaの設定  
@see https://github.com/authelia/authelia/blob/master/internal/configuration/config.template.yml

### [vars/main.yml](vars/main.yml)

設定値については[vars/main.yml](vars/main.yml)を参照してください。

#### `authelia_dependency_packages`

#### `authelia_repo`

Example Playbook
--------------

```yaml
- hosts: servers
  roles:
    - role: authelia
```

License
--------------

Apache License 2.0
