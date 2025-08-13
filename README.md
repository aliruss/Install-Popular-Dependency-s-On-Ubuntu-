# Install Popular Dependencies on Ubuntu 22.04

This guide will help you quickly install some of the most commonly used development dependencies on Ubuntu 22.04.  
Follow the instructions step-by-step to set up your environment.

---

## 1. Install Docker and Docker Compose

### Step 1: Uninstall old versions (if any)
```bash
sudo apt remove -y docker docker-engine docker.io containerd runc
```

### Step 2: Update package index
```bash
sudo apt update
```

### Step 3: Install required packages
```bash
sudo apt install -y ca-certificates curl gnupg lsb-release
```

### Step 4: Add Docker’s official GPG key
```bash
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

### Step 5: Set up the stable repository
```bash
echo   "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu   $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

### Step 6: Update package index again
```bash
sudo apt update
```

### Step 7: Install Docker Engine, CLI, containerd, and Docker Compose plugin
```bash
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

### Step 8: Verify Docker installation
```bash
sudo docker --version
docker compose version
```

### Step 9 (Optional): Run Docker without `sudo`
```bash
sudo usermod -aG docker $USER
newgrp docker
```

---

## 2. Install Node.js and npm

We will use the official NodeSource repository to install Node.js (LTS version).

### Step 1: Update system
```bash
sudo apt update && sudo apt upgrade -y
```

### Step 2: Install required tools
```bash
sudo apt install -y curl
```

### Step 3: Add the NodeSource repository (replace `20.x` with desired version)
```bash
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
```

### Step 4: Install Node.js and npm
```bash
sudo apt install -y nodejs
```

### Step 5: Verify installation
```bash
node -v
npm -v
```

> Tip: To manage multiple Node.js versions, consider installing **nvm** (Node Version Manager).

---
