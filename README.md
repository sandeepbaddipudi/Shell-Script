# 🐚 DevOps Shell Scripting Repository

This repository contains useful Shell Scripting automation examples used in DevOps, Cloud, Linux Administration, Kubernetes Operations, CI/CD automation, and Infrastructure Management.

The goal of this repository is to simplify repetitive operational tasks, automate deployments, monitor infrastructure, and improve production reliability.

---

# 🚀 Key Features

✅ Linux Automation Scripts  
✅ Kubernetes Utility Scripts  
✅ Docker Automation  
✅ AWS CLI Automation  
✅ Log Monitoring & Cleanup  
✅ Server Health Monitoring  
✅ Deployment Automation  
✅ Backup & Restore Scripts  
✅ Cron Job Automation  
✅ CI/CD Utility Scripts  
✅ Process Monitoring  
✅ Infrastructure Maintenance Scripts  

---

# 📂 Repository Structure

```bash
.
├── backup-scripts/
├── deployment-scripts/
├── kubernetes-scripts/
├── monitoring-scripts/
├── docker-scripts/
├── aws-scripts/
├── linux-admin/
└── utility-scripts/

⚡ Basic Shell Scripts
🖥️ 1. Disk Usage Monitoring Script

#!/bin/bash

THRESHOLD=80

usage=$(df -h / | awk 'NR==2 {print $5}' | sed 's/%//')

if [ $usage -gt $THRESHOLD ]
then
    echo "Warning: Disk usage is above ${THRESHOLD}%"
else
    echo "Disk usage is under control"
fi

🚀 2. Docker Container Status Script

#!/bin/bash

echo "Checking Failed Pods"

kubectl get pods --all-namespaces | grep -i error

kubectl get pods --all-namespaces | grep -i crashloopbackoff

☸️ 3. Kubernetes Pod Health Check Script

#!/bin/bash

echo "Checking Failed Pods"

kubectl get pods --all-namespaces | grep -i error

kubectl get pods --all-namespaces | grep -i crashloopbackoff

📦 4. Automated Backup Script

#!/bin/bash

SOURCE="/var/www/html"
DEST="/backup"

DATE=$(date +%Y-%m-%d)

tar -czvf $DEST/backup-$DATE.tar.gz $SOURCE

echo "Backup Completed Successfully"

🔄 5. Git Auto Pull Script
#!/bin/bash

cd /opt/application

git pull origin main

echo "Latest code pulled successfully"

☁️ AWS Automation Scripts

#!/bin/bash

aws ec2 describe-instances \
--query 'Reservations[*].Instances[*].[InstanceId,State.Name]' \
--output table

☸️ Kubernetes Useful Commands
kubectl get pods -A
kubectl get nodes
kubectl top pods
kubectl describe pod <pod-name>
kubectl logs <pod-name>

🐳 Docker Useful Commands

docker ps
docker images
docker logs <container-id>
docker exec -it <container-id> /bin/bash
