# Ansible Configuration

This repository contains Ansible playbooks and roles for infrastructure automation.

## Project Structure

```
.
├── inventory.ini              # Inventory file with host definitions
├── playbooks/
│   └── deploy.yml             # Main deployment playbook
└── roles/
    └── apache_service/        # Apache service role
        ├── tasks/
        │   └── main.yml       # Role tasks
        └── templates/
            └── container.service.j2  # Systemd service template
```

## Components

### Inventory
The `inventory.ini` file contains host definitions and group configurations for your infrastructure.

### Playbooks
- **deploy.yml**: Main deployment playbook for orchestrating infrastructure changes

### Roles
- **apache_service**: Role for managing Apache web server configuration and deployment
  - Includes tasks for service management
  - Contains Jinja2 templates for container service configuration

## Usage

To run the deployment playbook:

```bash
ansible-playbook -i inventory.ini playbooks/deploy.yml
```

## Requirements

- Ansible 2.9+
- SSH access to target hosts
- Python 3.6+ on target hosts

## License

MIT
