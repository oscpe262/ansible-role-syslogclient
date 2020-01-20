# Ansible role 'ansible-role-syslogclient'

An Ansible role for setting up Rsyslog clients to send logs to a rsyslog server.

## Requirements
The variables `syslogserver*` collides with my role oscpe262.rsyslogserver. This should usually not be an issue
if they are changed on a global level. They shouldn't need adjustment very often though, and then usually just the port, and the port you'll probably want to change on both server and clients anyway.

## Role Variables
| Variable		| Default		| Comments (type) |
| :---			| :---			| :---		  |
| `syslogclientServer` | `localhost`| server to send logs to |
| `syslogserverListenPort` | `514` | port the server listens on |
| `syslogserverPackages` | `["rsyslog"]` | list of packages to install |
| `syslogserverService` | `rsyslog` | service name |

## Dependencies

## Example Playbook
```Yaml
- hosts: foo
  roles:
    - role: ansible-role-syslogclient
```

## Testing


## License

MIT

## Contributors

Issues, feature requests, ideas, suggestions, etc. are appreciated and can be posted in the Issues section. Pull requests are also very welcome. Please create a topic branch for your proposed changes, it's the easiest way to merge back into the project.

- [Oscar Petersson](https://github.com/oscpe262/) (Maintainer)
