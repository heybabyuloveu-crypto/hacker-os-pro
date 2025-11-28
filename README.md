# ⚡ Hacker OS PRO — Ultra Realistic Cyberpunk AI System  
![version](https://img.shields.io/badge/version-1.0.0-blue)  
![license](https://img.shields.io/badge/license-MIT-green)  
![build](https://img.shields.io/github/actions/workflow/status/heybabyloveu-crypto/hacker-os-pro/deploy.yml)
![stars](https://img.shields.io/github/stars/heybabyloveu-crypto/hacker-os-pro?style=flat)
![issues](https://img.shields.io/github/issues/heybabyloveu-crypto/hacker-os-pro)

---

## 🚀 Features (PRO Edition)

### 🟢 3D Cyber Globe + Real-time Attack Lines  
- WebGL powered rotating Earth  
- Shader-based neon arcs  
- Live attack simulation  

### 🟢 AI Voice Terminal  
- Microphone input  
- TTS (Text-to-Speech) output  
- Command simulation: `scan`, `trace`, `breach`, `locate`

### 🟢 Hologram Hacker Desktop  
- Multi-window UI  
- Floating neon panels  
- Boot animation  
- Matrix shader background

### 🟢 Full AI Agent Integration  
- Local LLM (Ollama + Llama 3.1)  
- Web search tool  
- Memory tool  
- File ops  
- Multi-agent orchestration  

---

# 🖥 Project Structure

```
/backend
  ├── index.js
  ├── ai/
  ├── routes/
  ├── package.json

/frontend
  ├── src/
  ├── public/
  ├── vite.config.js
  ├── package.json

/render.yaml
/LICENSE
/README.md
```

---

# 📦 Deploy on Render (FREE)

Click to deploy instantly:

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy)

Or manual deploy:

```
git add .
git commit -m "deploy"
git push origin main
```

Render automatically detects:
- Frontend → Static site  
- Backend → Node web service  

---

# 📄 render.yaml (Auto Deploy Config)

```
services:
  - type: web
    name: hacker-os-backend
    env: node
    rootDir: backend
    buildCommand: "npm install"
    startCommand: "node index.js"

  - type: static
    name: hacker-os-frontend
    rootDir: frontend
    buildCommand: "npm install && npm run build"
    publishPath: "dist"
```

---

# 🤖 GitHub Actions — Auto Deploy (deploy.yml)

Create this file:  
`.github/workflows/deploy.yml`

```
name: Deploy to Render

on:
  push:
    branches: [ "main" ]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repo
        uses: actions/checkout@v3

      - name: Install backend
        working-directory: backend
        run: npm install

      - name: Install frontend
        working-directory: frontend
        run: npm install && npm run build

      - name: Deploy to Render
        run: echo "Render deploy triggered"
```

---

# 🤝 Contributing

1. Fork the repo  
2. Create new branch  
3. Commit changes  
4. Open PR  

---

# 📜 License  
MIT — free for personal and commercial use.

---

# ⭐ Support  
Give the project a **Star** ⭐ to support development!
