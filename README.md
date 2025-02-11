DeepSeek on Kubernetes

This repository provides all the necessary YAML files and commands to deploy DeepSeek AI on Kubernetes using Ollama. Follow along with the YouTube tutorial for a step-by-step guide.

📌 YouTube Tutorial

🎥 Watch the full tutorial here: Installing & Running DeepSeek on Kubernetes

🚀 What’s Included

Namespace Creation (deepseek)

Persistent Volume Claims (PVCs) for models and web UI

DeepSeek Deployment using Ollama

Web UI Deployment (ghcr.io/ollama-webui/ollama-webui:latest)

Service & Ingress Configuration

📂 Files in This Repo

deepseek-pvc.yaml – Defines Persistent Volume Claims

deepseek-server-deployment.yaml – Deploys DeepSeek with Ollama

deepseek-server-svc.yaml – Exposes DeepSeek server within the cluster

deepseek-ui-deployment.yaml – Deploys the Web UI

deepseek-ui-svc.yaml – Exposes DeepSeek ui within the cluster

deepseek-ing.yaml – Configures Ingress for external access

🛠 Setup Instructions

Clone the repository:

git clone https://github.com/devopstipstricks/DeepSeek.git
cd DeepSeek

Create the namespace:

kubectl create namespace deepseek

Apply the configurations:

kubectl apply -f deepseek-pvcs.yaml
kubectl apply -f deepseek-deployment.yaml
kubectl apply -f deepseek-service.yaml
kubectl apply -f deepseek-ui-deployment.yaml
kubectl apply -f deepseek-ingress.yaml

Check the running pods:

kubectl get pods -n deepseek

Access the Web UI:
Open your browser and go to:

http://deepseek.devopstips.local

🤝 Contributing

Feel free to submit issues or pull requests to improve this setup!

📢 Stay Connected

🔔 Subscribe for more DevOps & Kubernetes content: DevOpsTips YouTube Channel

Happy deploying! 🚀

