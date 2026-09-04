# 📚 Homelab Doc2Site (Documentation Viewer)

Reactive documentation static site generator and viewer for the `roadtotech.me` knowledge vault (`~/Brain`).

---

## 🏗️ Architecture & Requirements

- **Proxy Network**: Attached to external `proxy-net`
- **Domain**: `docs.roadtotech.me`
- **Target Port**: `8000` (FastAPI/Static service)
- **Docs Root Source**: `/home/kiskaadee/Brain` (mounted read-only to `/docs:ro`)

---

## ⚙️ Configuration & Metadata (`app.yaml`)

```yaml
name: "docs"
aliases:
  - "doc2site"
  - "notes"
domain: "docs.roadtotech.me"
description: "Reactive Obsidian & Markdown Documentation Viewer"
visible: true
auth: false
networks:
  - proxy-net
env:
  PROJECT_PATH: "/home/kiskaadee/Brain"
homepage:
  title: "Docs-Viewer"
  group: "Knowledge & Notes"
  icon: "files.png"
  container: "docs"
  weight: 10
```

---

## 🚀 Deployment

### Via Orchestrator (`appctl`)
```bash
appctl up docs
```

### Manual Deployment
```bash
docker compose up -d
```

---

## 📄 License
This repository is released into the public domain under the [Unlicense](LICENSE).
