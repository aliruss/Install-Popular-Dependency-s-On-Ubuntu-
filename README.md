# Install Popular Dependencies on Ubuntu 22.04
## Installing Popular Dependencies

Run the following command to install a set of commonly used development and system administration tools on Ubuntu:

```bash
sudo apt install curl screen iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev ca-certificates -y
```

## Docker Compose (v2)

Docker Compose v2 is included when you install the `docker-compose-plugin` (as shown above).  
You use it with the `docker compose` command (note the space).

### Check your Compose version
```bash
docker compose version
```

### Quick test with a minimal Compose file
Create a `docker-compose.yml`:
```yaml
services:
  hello:
    image: hello-world
```

Run it:
```bash
docker compose up
```

Stop and clean up:
```bash
docker compose down
```

### Where is Compose installed?
With v2, Compose is shipped as a Docker CLI plugin:
- Linux path: `/usr/lib/docker/cli-plugins/docker-compose` (path can vary by distro)
- Command name: `docker compose`

> Note: Legacy `docker-compose` (v1) is deprecated. Prefer `docker compose` (v2).

## Installing Popular Dependencies

Run the following command to install a set of commonly used development and system administration tools on Ubuntu:

```bash
sudo apt install curl screen iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev ca-certificates -y
```
