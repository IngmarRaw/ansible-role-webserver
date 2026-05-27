# Ansible Role: webserver

Installeert en configureert Apache, PHP en php-mysql op Ubuntu webservers.

## Requirements

Deze role is getest op Ubuntu 24.04.

## Role Variables

| Variabele | Standaardwaarde |
|---|---|
| `webserver_apache_package` | `apache2` |
| `webserver_php_packages` | `php`, `php-mysql` |
| `webserver_service_name` | `apache2` |
| `webserver_document_root` | `/var/www/html` |
| `webserver_index_file` | `index.php` |

## Example Playbook

```yaml
- name: Configureer webserver
  hosts: webservers
  become: true

  roles:
    - webserver
