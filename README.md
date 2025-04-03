# Fitness Class Booking - DevOps Deployment

This project automates the deployment of a Django-based Fitness Class Booking application using Ansible and DevOps practices.

## 🚀 Features
- Automated deployment with Ansible
- PostgreSQL database integration
- Dockerization for containerized environments
- CI/CD pipeline with GitHub Actions

## 📌 Requirements
- Ubuntu 20.04+ server
- SSH access with a private key
- Ansible installed (`pip install ansible`)
- PostgreSQL database
- GitHub repository for the project

## 📂 Project Structure
```
├── ansible/
│   ├── deploy.yml        # Ansible playbook for deployment
│   ├── inventory.ini     # Server inventory file
├── docker/
│   ├── Dockerfile        # Docker setup for the application
│   ├── docker-compose.yml
├── src/
│   ├── manage.py         # Django application entry point
│   ├── requirements.txt  # Dependencies
│   ├── .env              # Environment variables (not in repo)
```

## 🛠 Deployment Steps

### 1️⃣ Setup Ansible Inventory
Update `inventory.ini` with your server details:
```ini
[web]
YOUR_SERVER_IP ansible_user=ubuntu ansible_ssh_private_key_file=~/.ssh/id_rsa
```

### 2️⃣ Run Ansible Playbook
Execute the deployment script:
```bash
ansible-playbook -i inventory.ini ansible/deploy.yml
```

### 3️⃣ Verify Deployment
Check if the app is running:
```bash
curl http://YOUR_SERVER_IP
```

## 🚧 Troubleshooting
- **SSH Issues:** Ensure your private key matches the server’s authorized keys.
- **Database Errors:** Confirm PostgreSQL credentials in `.env`.
- **Ansible Failures:** Run with `-vvv` flag for detailed logs.

## 📜 License
MIT License. Feel free to modify and use.

---

💡 **Contributions & Feedback**
For suggestions, open an issue or submit a pull request. 🚀

