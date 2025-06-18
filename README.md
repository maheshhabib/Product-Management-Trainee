# Problem 2: Kubernetes Security Scan

## Tools Used
- Minikube
- Kubescape

## Instructions

### Step 1: Install Minikube
```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
minikube start
```

### Step 2: Deploy Sample App
```bash
kubectl create deployment nginx --image=nginx
kubectl expose deployment nginx --port=80 --type=NodePort
```

### Step 3: Run Kubescape Scan
```bash
curl -s https://raw.githubusercontent.com/kubescape/kubescape/master/install.sh | /bin/bash
kubescape scan framework nsa --format json --output results.json
```

> Submit the `results.json` file.
