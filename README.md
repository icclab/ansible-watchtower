*Please note that all watchtower components are under heavy development and the norm is that things will break. Please be patient with us until the first stable release.*

<div align="center">
	<img src="https://raw.githubusercontent.com/icclab/watchtower-common/master/watchtower.png" alt="Watchtower" title="Watchtower">
</div>

# Role Name

Installs Watchtower which is a Cloud Incident Management solution.

### Role Variables

The following role variables can be set:

| Name | Values | Default | Description |
|------|--------|---------|-------------|
| release | true / false | false | If set to true the role will install the latest release, otherwise it will install the latest code |
| mysql_root_password | String | reallylongpassword | Sets the MySQL root password |
| mysql_username | String | watchtower | Watchtower's MySQL username |
| mysql_password | String | anotherlongpassword | Watchtower's MySQL password |
| mysql_database | String | watchtower | Watchtower's MySQL database |

### Dependencies

`ansible-watchtower` requires several other roles which can be easily installed by running the following commands:

```
ansible-galaxy install tkuhlman.zookeeper
ansible-galaxy install tkuhlman.kafka
```

### Installation

`ansible-watchtower` can be easily installed by running:

```
ansible-galaxy install nemros.watchtower
```

### Example Playbook

The following is an example playbook to use this role:

```
---
- hosts: all
  sudo: yes
  roles:
    - { role: nemros.watchtower }
```

# License

Copyright 2015 Zurich University of Applied Sciences

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or
implied.
See the License for the specific language governing permissions and
limitations under the License.

# Author Information

For further information or assistance please contact [**Victor Ion Munteanu**](https://github.com/nemros).
