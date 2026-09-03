# 📚 Homelab Doc2Site (Documentation Viewer)

Reactive documentation static site generator and viewer for personal knowledge docs and study guides.

Part of the [homelab-core](https://github.com/kiskaadee/homelab-core) cluster ecosystem.

---

## 🏗️ Architecture & Requirements

- **Proxy**: Traefik (attached to `proxy-net`)
- **Port**: `8000` (FastAPI/Static service)
- **Domain**: `docs.arch-services.mywire.org`

---

## ⚙️ Environment Variables

| Variable | Description | Default / Example |
| :--- | :--- | :--- |
| `DOCS_DOMAIN` | Routed FQDN | `docs.arch-services.mywire.org` |
| `DOCS_PROJECT_PATH` | Path to docs source | Configured via environment |

---

## 🚀 Deployment

### Via Orchestrator (`appctl`)
```bash
appctl up homelab-doc2site
```

### Manual Deployment
```bash
docker compose up --build -d
```
