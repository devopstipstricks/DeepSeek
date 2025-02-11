# 🚀 Deploying DeepSeek on Kubernetes  

This repository contains all the necessary **YAML files** and commands to install and run **DeepSeek AI** on **Kubernetes** using **Ollama**.  

📺 **Watch the Full Tutorial on YouTube:**  
[![DeepSeek on Kubernetes](https://img.youtube.com/vi/2N12lL-9mS0/0.jpg)](https://youtu.be/2N12lL-9mS0?si=Xda8jNn7Yehpq7NV)  

---

## 📌 Overview  

In this setup, we:  
✅ Deploy **DeepSeek AI** with Kubernetes & Ollama  
✅ Use **Persistent Volume Claims (PVCs)** for model storage  
✅ Expose DeepSeek via **Ingress** (`deepseek.devopstips.local`)  
✅ Run the Web UI using `ghcr.io/ollama-webui/ollama-webui:latest`  

---

## 📂 Files & Setup  

| File | Description |
|------|------------|
| `deepseek-pvcs.yaml` | Creates Persistent Volume Claims for DeepSeek & Web UI |
| `deepseek-deployment.yaml` | Deploys DeepSeek AI on Kubernetes |
| `deepseek-service.yaml` | Exposes DeepSeek via a Kubernetes Service |
| `deepseek-ui-deployment.yaml` | Deploys the DeepSeek Web UI |
| `deepseek-ingress.yaml` | Configures Ingress for external access |

---

## 🚀 Installation Guide  

### 1️⃣ **Clone the Repository**  
```bash
git clone https://github.com/devopstipstricks/DeepSeek.git
cd DeepSeek
2️⃣ Create the Namespace
bash
Copy
Edit
kubectl create namespace deepseek
3️⃣ Apply the PVCs
bash
Copy
Edit
kubectl apply -f deepseek-pvcs.yaml
4️⃣ Deploy DeepSeek AI
bash
Copy
Edit
kubectl apply -f deepseek-deployment.yaml
5️⃣ Expose DeepSeek with a Service
bash
Copy
Edit
kubectl apply -f deepseek-service.yaml
6️⃣ Deploy the Web UI
bash
Copy
Edit
kubectl apply -f deepseek-ui-deployment.yaml
7️⃣ Set Up Ingress for Access
bash
Copy
Edit
kubectl apply -f deepseek-ingress.yaml
8️⃣ Verify the Deployment
bash
Copy
Edit
kubectl get pods -n deepseek
kubectl get svc -n deepseek
🎯 How to Access
DeepSeek API: http://deepseek.devopstips.local
DeepSeek Web UI: http://deepseek.devopstips.local/ui
💡 Make sure your DNS or /etc/hosts file is configured to resolve deepseek.devopstips.local.

🤝 Contributing
Feel free to fork this repository, open issues, or submit pull requests! 🚀
