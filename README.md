# k3s GitOps Lab 🚀

This repository is used to manage Kubernetes workloads using GitOps with:

- k3s
- Argo CD
- GitHub

---

## 🧠 Architecture

GitHub → Argo CD → k3s Cluster

Argo CD continuously watches this repository and reconciles the cluster state to match what is defined here.

---

## 📁 Repository Structure
k3s-gitops-lab/
├── apps/
│ └── hello-nginx/
│ ├── deployment.yaml
│ └── service.yaml


- `apps/` – Application manifests
- Each app lives in its own folder
- Designed for future expansion (multi-env, app-of-apps, platform services)

---

## 🚀 How It Works

1. Changes are committed to GitHub
2. Argo CD detects changes
3. Application becomes `OutOfSync`
4. Sync applies changes to the cluster
5. Cluster state matches Git

---

## 🔥 Goals

- Learn GitOps principles
- Understand Argo CD reconciliation
- Experiment with scaling, rollouts, and drift detection
- Model future platform architecture

---

## 🛠 Next Steps

- Add Auto-Sync
- Enable Self-Heal
- Implement App-of-Apps pattern
- Introduce environments (dev/stage/prod)
- Explore Helm support

---

## ⚠️ Notes

This repository is intended for lab and experimentation purposes.
Not production hardened (yet 😉).