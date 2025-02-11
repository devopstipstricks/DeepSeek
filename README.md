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
| `deepseek-pvc.yaml` | Creates Persistent Volume Claims for DeepSeek & Web UI |
| `deepseek-server-deployment.yaml` | Deploys DeepSeek AI Server on Kubernetes |
| `deepseek-server-svc.yaml` | Exposes DeepSeek via a Kubernetes Service |
| `deepseek-ui-deployment.yaml` | Deploys the DeepSeek Web UI |
| `deepseek-ui-svc.yaml` | Exposes DeepSeek UI via a Kubernetes Service |
| `deepseek-ing.yaml` | Configures Ingress for external access |
