## 👋 Welcome to postiz 🚀

Social media management and scheduling platform

## 📋 Description

Social media management and scheduling platform

## 🚀 Services

- **app**: ghcr.io/gitroomhq/postiz-app:latest

### Infrastructure Components

- **db**: Postgres database
- **redis**: Redis database


## 📦 Installation

### Option 1: Quick Install
```bash
curl -q -LSsf "https://raw.githubusercontent.com/composemgr/postiz/main/docker-compose.yaml" -o compose.yml
```

### Option 2: Git Clone
```bash
git clone "https://github.com/composemgr/postiz" ~/.local/srv/docker/postiz
cd ~/.local/srv/docker/postiz
docker compose up -d
```

### Option 3: Using composemgr
```bash
composemgr install postiz
```

## 🔧 Configuration

### Environment Variables

```shell
APP_JWT_TOKEN=changeme_jwt_secret
DB_USER_NAME=postiz
```

See `docker-compose.yaml` for complete list of configurable options.

## 🌐 Access

- **Web Interface**: http://172.17.0.1:50041

## 📂 Volumes

- `./volumes/config/postiz` - Data storage
- `./volumes/data/postiz/uploads` - Data storage
- `./volumes/data/db/postgres/postiz` - Data storage
- `./volumes/data/db/redis/postiz` - Data storage

## 🔐 Security

- Change all default passwords before deploying to production
- Use strong secrets for all authentication tokens
- Configure HTTPS using a reverse proxy (nginx, traefik, caddy)
- Regularly update Docker images for security patches
- Backup your data regularly

## 🔍 Logging

```shell
docker compose logs -f app
```

## 🛠️ Management

```bash
# Start services
docker compose up -d

# Stop services
docker compose down

# Update to latest images
docker compose pull && docker compose up -d

# View logs
docker compose logs -f

# Restart services
docker compose restart
```

## 📋 Requirements

- Docker Engine 20.10+
- Docker Compose V2+

## 🤝 Author

🤖 casjay: [Github](https://github.com/casjay) 🤖  
🦄 composemgr: [Github](https://github.com/composemgr) 🦄
