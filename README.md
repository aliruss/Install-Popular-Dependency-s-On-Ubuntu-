# Installing Node.js and npm on Ubuntu 22.04

This guide explains how to install **Node.js** and **npm** on Ubuntu 22.04 using the official NodeSource repository.

## Steps

### 1. Update your package list
```bash
sudo apt update && sudo apt upgrade -y
```

### 2. Install required tools
```bash
sudo apt install -y curl
```

### 3. Add the NodeSource repository
Replace `20.x` with your desired Node.js version if you want a different version.
```bash
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
```

### 4. Install Node.js and npm
```bash
sudo apt install -y nodejs
```

### 5. Verify the installation
```bash
node -v
npm -v
```

## Notes
- If you need a different version of Node.js, change `20.x` to the desired version (e.g., `18.x`).
- For more flexibility in switching Node.js versions, consider installing **nvm** (Node Version Manager).
