# ElectroEye

ElectroEye is an open-source security analysis tool designed for Electron desktop applications. It provides automated static and dynamic analysis to detect hardcoded secrets (e.g., API keys, tokens) and vulnerabilities (e.g., insecure `nodeIntegration`, XSS-to-RCE risks) through a user-friendly local web interface. Built with Python, Node.js, and React, ElectroEye aims to simplify Electron app security testing for developers and security researchers.

## Features
- **Static Analysis**: Unpacks `.asar` files and scans for secrets and Electron-specific misconfigurations (e.g., `nodeIntegration=true`, `contextIsolation=false`).
- **Dynamic Analysis**: Monitors runtime behavior and network traffic using Frida and mitmproxy (planned).
- **Web Interface**: Drag-and-drop file uploads, interactive dashboard, and detailed vulnerability reports powered by React and Ant Design.
- **Secrets Detection**: Identifies hardcoded sensitive data using truffleHog’s regex and entropy-based scanning.
- **Extensibility**: Modular design for adding new analysis modules or integrations.
- **CI/CD Integration**: REST API for seamless integration into DevSecOps pipelines.

## Tech Stack
- **Backend**: Python (FastAPI, Pydantic, SQLAlchemy, Celery)
- **Electron-Specific**: Node.js (asar, electronegativity)
- **Frontend**: JavaScript (React, Ant Design, Axios)
- **Database**: SQLite (scalable to PostgreSQL)
- **Task Queue**: Celery with Redis
- **Analysis Tools**: truffleHog (secrets), Frida (dynamic), mitmproxy (network)

## Installation

### Prerequisites
- Python 3.8+
- Node.js 16+
- Redis
- Git

### Setup
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/ElectroEye.git
   cd ElectroEye
