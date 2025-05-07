# Deploy Website with Ansible Role

This repository contains an Ansible project to automate the deployment of a static website using a reusable Ansible role.

## 📦 Project Structure

```bash
.
├── ansible.cfg
├── playbook.yml
├── inventory
├── roles/
│   └── website/
│       ├── tasks/
│       │   └── main.yml
└── README.md
```

## 🚀 Features

* Uses a custom Ansible role (`website`) to handle deployment tasks.
* Copies a static HTML file (`index.html`) to the target web server.
* Ensures the Apache web server is installed and running.
* Clean, modular role structure for reuse in other projects.

## 📋 Prerequisites

* Ansible installed on the control machine.
* A target host (remote VM or server) with:

  * SSH access configured.
  * A Debian-based OS (e.g., Ubuntu).
* Python installed on the target host (required by Ansible).

## ⚙️ Inventory (`hosts` file)

Update the `hosts` file with the IP address or hostname of your target machine:

```ini
[webservers]
your_server_ip_or_hostname ansible_user=your_user ansible_ssh_private_key_file=~/.ssh/your_key
```

## 🛠️ Running the Playbook

1. Clone the repository:

```bash
git clone https://github.com/emanzaki/Deploy-website-with-ansible-role.git
cd Deploy-website-with-ansible-role
```

2. Run the Ansible playbook:

```bash
ansible-navigator run deploy.yml
```

## 📄 Role: `website`

This role performs the following tasks:

* Installs Apache2.
* Starts and enables the Apache2 service.
* Write the hostname to `/var/www/html/index.html`.

## 📝 License

This project is open-source and available under the [MIT License](LICENSE) (add if applicable).

## 👩‍💻 Author

**Eman Zaki**
[GitHub Profile](https://github.com/emanzaki)
