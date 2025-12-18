<h1 align="center">DEGENI – Claude + Gemini AI Terminal</h1>

<p align="center">
  <img src="https://img.shields.io/github/v/release/bicknicktick/DEGENI-CLAUDE-ANTIGRAVITY-GEMINI?style=for-the-badge&amp;color=06b6d4" alt="Release Version">
  <img src="https://img.shields.io/github/license/bicknicktick/DEGENI-CLAUDE-ANTIGRAVITY-GEMINI?style=for-the-badge&amp;color=10b981" alt="License">
  <img src="https://img.shields.io/github/actions/workflow/status/bicknicktick/DEGENI-CLAUDE-ANTIGRAVITY-GEMINI/ci.yml?branch=main&amp;style=for-the-badge&amp;color=8b5cf6" alt="Build Status">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/DEGENI-v1.0.0-06b6d4?style=for-the-badge" alt="DEGENI">
  <img src="https://img.shields.io/badge/by-BITZY.ID-10b981?style=for-the-badge" alt="BITZY.ID">
  <img src="https://img.shields.io/badge/Claude-Sonnet%204.5-8b5cf6?style=for-the-badge" alt="Claude">
  <img src="https://img.shields.io/badge/Gemini-3%20Pro-f59e0b?style=for-the-badge" alt="Gemini">
</p>

```
  ██████╗ ███████╗ ██████╗ ███████╗███╗   ██╗██╗
  ██╔══██╗██╔════╝██╔════╝ ██╔════╝████╗  ██║██║
  ██║  ██║█████╗  ██║  ███╗█████╗  ██╔██╗ ██║██║
  ██║  ██║██╔══╝  ██║   ██║██╔══╝  ██║╚██╗██║██║
  ██████╔╝███████╗╚██████╔╝███████╗██║ ╚████║██║
  ╚═════╝ ╚══════╝ ╚═════╝ ╚══════╝╚═╝  ╚═══╝╚═╝
         
       Claude + Gemini AI Terminal
            by BITZY.ID
```

<p align="center">
  <strong>🚀 Access Claude Sonnet 4.5 &amp; Gemini 3 Pro FREE in your terminal!</strong>
</p>

---

## 📝 Description

**DEGENI** is a terminal-based AI tool that provides free access to powerful Claude and Gemini models directly from your shell, with zero subscription costs. It wraps Google AI Pro and Antigravity-based Claude wrappers into a single CLI experience, complete with persistent sessions and a live web dashboard. Designed for developers and power users, DEGENI makes it easy to code, analyze, and experiment with state-of-the-art models from your own machine.

---

## ✨ Key Features

- 🆓 **100% Free access** to Google AI Pro and Claude wrappers (no monthly subscription)
- 🤖 **Multi-model support**: Claude Sonnet/Opus 4.5 Thinking + Gemini 3 Pro / 2.5 Pro / 2.5 Flash
- 💬 **Interactive chat mode** with session history and timestamps
- ⚡ **Quick one-off questions** directly from the CLI
- 💾 **Session management**: save, load, list, and clear conversations
- 📊 **Live dashboard** with real-time server status, logs, account list, and model switching
- 🔄 **Auto-balance across multiple accounts** to reduce rate limiting
- 🎛️ **1-click actions** from the dashboard (restart proxy, toggle accounts, switch models)
- 📦 **Portable install**: simple shell scripts, no heavy dependencies beyond Node.js and CLI tools
- 🔐 **Local-only traffic** with credentials stored on your machine

---

## 🖼️ Screenshots

> Example layout of the DEGENI dashboard and terminal usage.

| ![Screenshot 1](screenshots/screen1.png) | ![Screenshot 2](screenshots/screen2.png) | ![Screenshot 3](screenshots/screen3.png) |
|:---:|:---:|:---:|
| *Terminal chat with Claude + Gemini* | *Live dashboard with real-time stats* | *Session management and logs view* |

---

## 🚀 Installation

### 1. Clone the repository (recommended)

```bash
git clone https://github.com/bicknicktick/DEGENI-CLAUDE-ANTIGRAVITY-GEMINI.git
cd DEGENI-CLAUDE-ANTIGRAVITY-GEMINI
```

### 2. Run the installer

```bash
bash install.sh
```

### 3. Reload your shell (one time only)

```bash
# Bash / Zsh
source ~/.bashrc   # or source ~/.zshrc
```

### 4. Add a Google AI account (required)

```bash
degeni add
# → Choose [1] Antigravity (recommended for Claude models)
# → Open the URL shown in your browser
# → Login with your Google account
# → Authorize the app
# → Copy the callback URL from the browser
# → Paste it back into the terminal
```

### 5. Verify the installation

```bash
degeni "hello world"
degeni status
```

> After this one-time setup, you can call `degeni` from anywhere in your terminal.

---

## 📦 Usage

### Quick questions from the terminal

```bash
# Ask a one-off question (no interactive session)
degeni "jelaskan docker dalam 3 kalimat"

# Ask in English
degeni "Explain the difference between Claude Sonnet 4.5 and Gemini 3 Pro."
```

### Interactive chat mode

```bash
# Start an interactive session
degeni chat
```

Inside chat mode you can use:

```bash
/sessions        # List all saved sessions
/new [name]      # Start new session with an optional name
/load <number>   # Load session by number
/history         # Show current session history
/clear           # Clear all sessions
/help            # Show in-chat help
```

The same operations are available via the CLI:

```bash
degeni sessions              # List sessions
degeni session new "My Chat" # Create session
degeni session load 1        # Load session #1
degeni session delete 1      # Delete a session
degeni session clear         # Clear all sessions
```

### Account management

```bash
degeni              # Interactive menu
degeni list         # List all configured accounts
degeni add          # Add a new account
degeni disable      # Disable an account
degeni enable       # Enable an account
degeni restart      # Restart & try to unsuspend accounts
degeni test         # Test all accounts
```

### Model and dashboard commands

```bash
degeni model        # Switch AI model (Claude / Gemini variants)
degeni dash         # Open live dashboard in your browser
degeni status       # Show system status
degeni errors       # View recent error logs
```

### Troubleshooting helpers

```bash
# Diagnose common issues
degeni diagnose

# Diagnose + interactive auto-fix options
degeni fix
```

Checks include:

- Proxy server availability
- Account presence and status
- Rate limits and quota issues
- Authentication errors (expired tokens)
- Suspended accounts
- API connectivity

---

## 🌐 Live Dashboard

Dashboard dengan **real-time data** – bukan dummy!

```bash
# Start dashboard services
~/DEGENI/start-dashboard.sh

# Open in browser
# http://localhost:8080/dashboard.html
```

### Dashboard Features

| Feature | Action | Status |
|--------|--------|--------|
| **Server Status** | Auto-refresh | ✅ LIVE |
| **Account List** | Click to toggle | ✅ LIVE |
| **Switch Model** | Click to switch | ✅ LIVE |
| **Restart Proxy** | Click button | ✅ LIVE |
| **Test Connection** | Click button | ✅ LIVE |
| **System Logs** | Auto-refresh 5s | ✅ LIVE |

**Semua aksi tinggal KLIK – langsung execute!**

---

## 🤖 Available Models

### Claude Wrappers (via Antigravity)

| Model | Best For |
|-------|----------|
| `gemini-claude-sonnet-4-5-thinking` ⭐ | Coding, analysis |
| `gemini-claude-opus-4-5-thinking` | Complex reasoning |
| `gemini-claude-sonnet-4-5` | General tasks |

### Gemini Models

| Model | Best For |
|-------|----------|
| `gemini-3-pro-preview` | All-purpose, latest model |
| `gemini-2.5-pro` | Long-context tasks |
| `gemini-2.5-flash` | Quick, low-latency tasks |

---

## 📁 Project Structure

```bash
~/DEGENI/
├── install.sh           # One-shot installer
├── start-dashboard.sh   # Start live dashboard
├── bin/
│   ├── degeni           # Main CLI tool entrypoint
│   ├── ai               # AI wrapper with session support
│   ├── degeni-api       # Backend API server
│   └── degeni-session   # Session manager
├── ui/
│   ├── dashboard.html   # Live dashboard UI
│   └── favicon.svg      # Dashboard icon
├── sessions/            # Saved chat sessions (JSON)
├── config/              # Configuration and runtime data
├── logs/                # Application and proxy logs
└── README.md            # Project documentation
```

---

## 🛠️ Technologies

Main technologies and services used by DEGENI:

- ![Shell](https://img.shields.io/badge/Shell-Bash-4EAA25?logo=gnu-bash&logoColor=white) – installer and CLI scripts
- ![Node.js](https://img.shields.io/badge/Node.js-Backend-339933?logo=node.js&logoColor=white) – API server and integrations
- ![HTML](https://img.shields.io/badge/HTML-Dashboard-E34F26?logo=html5&logoColor=white) – web dashboard UI
- ![Claude](https://img.shields.io/badge/Claude-Sonnet%204.5-8b5cf6) – coding and reasoning model
- ![Gemini](https://img.shields.io/badge/Gemini-3%20Pro-f59e0b) – latest Google Gemini model family
- ![Google AI](https://img.shields.io/badge/Google%20AI-Pro-4285F4?logo=google&logoColor=white) – underlying AI service

---

## 🔧 API Endpoints

Dashboard menggunakan backend API untuk real-time data:

| Endpoint | Method | Fungsi |
|----------|--------|--------|
| `/api/status` | GET | Server status + account count |
| `/api/accounts` | GET | List all accounts |
| `/api/models` | GET | Available models |
| `/api/logs` | GET | Recent logs |
| `/api/config` | GET | Current model config |
| `/api/restart` | POST | Restart proxy server |
| `/api/test` | POST | Test API connection |
| `/api/account/toggle` | POST | Enable/disable account |
| `/api/model/switch` | POST | Switch AI model |

**API Server:** `http://localhost:8321`

---

## 🧩 Troubleshooting

### Error: `auth_unavailable`

```bash
degeni restart
```

### Error: `payment_required`

```bash
# Add another account or switch model
degeni add
degeni model  # Select: gemini-3-pro-preview
```

### Dashboard not loading

```bash
# Start dashboard services
~/DEGENI/start-dashboard.sh
```

---

## 🤝 Contributing

Contributions, bug reports, and feature requests are very welcome.

1. Fork the repository
2. Create a feature branch:  
   ```bash
   git checkout -b feature/my-feature
   ```
3. Make your changes and add tests if applicable
4. Commit with a descriptive message:
   ```bash
   git commit -m "feat: add amazing feature"
   ```
5. Push your branch:
   ```bash
   git push origin feature/my-feature
   ```
6. Open a Pull Request describing your changes, motivation, and any relevant context

Please try to follow the existing coding style and keep commits focused and atomic.

---

## 📄 License

This project is licensed under the **MIT License**.  
See the `LICENSE` file in this repository for full license text.

---

## 📞 Support

- 🌐 Website: [bitzy.id](https://bitzy.id)
- 📧 Email: support@bitzy.id

---

## ☕ Donate

Jika DEGENI bermanfaat, dukung pengembangan dengan donasi:

<p align="center">
  <a href="https://paypal.me/bitzyid">
    <img src="https://img.shields.io/badge/PayPal-Donate-00457C?style=for-the-badge&logo=paypal&logoColor=white" alt="Donate via PayPal">
  </a>
</p>

<p align="center">
  <strong>paypal.me/bitzyid</strong>
</p>

---

<p align="center">
  <strong>DEGENI v1.0.0</strong><br>
  <sub>Claude + Gemini AI Terminal</sub><br>
  <sub>by <a href="https://bitzy.id">BITZY.ID</a></sub>
</p>

<p align="center">
  <sub>Made with ❤️ in Indonesia</sub>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Free-Forever-10b981?style=flat-square" alt="Free">
  <img src="https://img.shields.io/badge/Live-Dashboard-06b6d4?style=flat-square" alt="Live">
  <img src="https://img.shields.io/badge/1--Click-Actions-8b5cf6?style=flat-square" alt="1-Click">
  <img src="https://img.shields.io/badge/Made%20in-Indonesia-ef4444?style=flat-square" alt="Indonesia">
</p>
