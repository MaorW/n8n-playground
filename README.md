# N8n Server with Nginx Reverse Proxy

Docker-based setup with nginx as reverse proxy for n8n.

## Services

- **nginx**: Reverse proxy (ports 80/443)
- **n8n**: Workflow automation platform (internal port 5678)
- **postgres**: Database for n8n

## Quick Start

```bash
# Start services
docker-compose up -d

# View logs
docker-compose logs -f

# Stop services
docker-compose down
```

## Access

- n8n UI: http://localhost
- Webhooks: http://localhost/webhook

## SSL Setup

1. Create ssl directory: `mkdir -p nginx/ssl`
2. Add `cert.pem` and `key.pem`
3. Uncomment HTTPS server block in nginx.conf
4. Restart: `docker-compose up -d`