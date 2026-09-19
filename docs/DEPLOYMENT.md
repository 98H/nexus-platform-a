# Deployment & Operations Guide: Platform A

## 🚀 Live Access & URLs
- **Live Public Access URL:** [/preview/prod-platform-a-6934ab/](/preview/prod-platform-a-6934ab/)
- **Internal Port:** `0`
- **Runtime Engine:** `python_preview`
- **Deployment Status:** `DEPLOYED / ACTIVE`
- **Timestamp:** `2026-09-19T16:16:33.128415+00:00`

## 🛠️ Management & Service Control
### Launch Command
```bash
python3 app.py --port 0
```

### Health Check Probe
```bash
curl -I http://127.0.0.1:0/
```

### Systemd Service Template
```ini
[Unit]
Description=Platform A Service
After=network.target

[Service]
Type=simple
WorkingDirectory=/tmp/pytest-of-root/pytest-0/test_scoped_chat_persistence_a0/workspaces/prod-platform-a-6934ab
ExecStart=/usr/bin/python3 /tmp/pytest-of-root/pytest-0/test_scoped_chat_persistence_a0/workspaces/prod-platform-a-6934ab/app.py
Restart=always
RestartSec=3

[Install]
WantedBy=multi-user.target
```

## 🔒 Production Security Protocols
- HTTP-only reverse proxy via Nexus Gateway.
- Dedicated port allocation with zero port conflict.
