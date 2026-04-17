# 🚀 Ansible Patch Management Automation

## 📌 Project Overview

This project automates patch management across multiple Linux servers using Ansible.
It supports both Debian-based and RedHat-based systems and ensures systems are updated, rebooted if required, and handled safely with error control.

---

## 🎯 Features

* Automated package updates for Ubuntu (APT) and RedHat (YUM)
* Conditional reboot only when required
* Error handling using `ignore_errors`
* OS-based task execution using `ansible_os_family`
* Logging of update status
* Idempotent execution (safe to run multiple times)

---

## 🧱 Project Structure

```
ansible-patch-project/
├── ansible.cfg
├── inventory/
├── group_vars/
├── roles/
│   └── patch/
│       └── tasks/
├── playbook.yml
```

---

## ⚙️ Prerequisites

* Ansible installed
* SSH access to target servers
* Sudo privileges on target machines

---

## ▶️ How to Run

### 1. Test connectivity

```
ansible all -m ping -i inventory/hosts.ini
```

### 2. Run playbook

```
ansible-playbook -i inventory/hosts.ini playbook.yml --ask-become-pass
```

---

## 🧠 Key Concepts Used

* Roles in Ansible
* Conditional execution (`when`)
* Error handling (`ignore_errors`)
* Privilege escalation (`become`)
* Idempotency

---


## 👤 Author

DEEPAK YADAV
