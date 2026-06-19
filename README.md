# AYINDEBUILD - Multi-Platform Coding Platform

**A Vibe Coding Platform that works just fine and lets you bring in your own LLM to help as Copilot if you ever exhaust your Copilot credit**

## Overview

AYINDEBUILD is a decentralized coding platform available as:
- 🌐 **Web Version** (GitHub - Open to everyone, no security OAuth)
- 📱 **Android APK** (Standalone - Ready for APK builder compilation)
- 🖥️ **Desktop Software** (Standalone executable)

All versions support user-provided LLM/AI models to act as intelligent coding assistants, similar to GitHub Copilot.

---

## Key Features (50+ Skills & Tools)

### Core Coding Features
1. **Syntax Highlighting** - Multi-language support (JavaScript, Python, Java, C++, Go, Rust, etc.)
2. **Real-time Code Completion** - AI-powered suggestions from user's LLM
3. **Integrated Terminal** - Command execution environment
4. **File Browser** - Project structure navigation
5. **Git Integration** - Clone, commit, push, pull directly from the platform
6. **Code Formatter** - Auto-format code (Prettier, Black, etc.)
7. **Linting & Error Detection** - Real-time syntax checking
8. **Debugging Tools** - Breakpoints, watches, step-through execution
9. **Version Control Viewer** - Commit history and diff viewer
10. **Quick Search** - Find files and text across project

### AI/LLM Integration Features
11. **Custom LLM Integration** - Connect any user's LLM API (OpenAI, Anthropic, local models)
12. **Code Generation** - Generate code from natural language prompts
13. **Code Explanation** - AI explains selected code snippets
14. **Bug Detection & Fixing** - AI identifies and suggests fixes
15. **Performance Optimization Suggestions** - AI analyzes code performance
16. **Documentation Generator** - Auto-generate comments and docstrings
17. **Refactoring Assistant** - AI suggests code improvements
18. **Code Review Helper** - AI reviews code quality
19. **Security Analysis** - Detect vulnerabilities and security issues
20. **Architecture Advisor** - AI suggests system design patterns

### Collaboration Features
21. **Real-time Collaboration** - Multiple users editing same file
22. **Comment Threads** - Discuss code sections
23. **Code Review Board** - Structured peer review process
24. **Chat Integration** - Team communication within IDE
25. **Activity Timeline** - Track who changed what and when
26. **User Presence Indicators** - See who's online
27. **Pair Programming Mode** - Follow cursor movements
28. **Permission Management** - Control access levels

### Repository Management
29. **GitHub Clone Integration** - Clone any GitHub repo directly
30. **Auto-sync to GitHub** - Push changes back to GitHub automatically
31. **Multi-repo Workspace** - Work on multiple projects simultaneously
32. **Repository Templates** - Quick-start project templates
33. **Dependency Management** - Auto-detect and manage project dependencies
34. **Package Manager Integration** - npm, pip, cargo, maven support
35. **License Management** - Auto-add licenses to projects

### Development Tools
36. **Live Preview** - Real-time web development preview
37. **Emulator Support** - Android/iOS emulator integration
38. **Database Client** - Connect to databases (PostgreSQL, MongoDB, etc.)
39. **API Testing Tool** - Built-in REST/GraphQL client
40. **Environment Variable Manager** - .env file management
41. **Build System Integration** - Webpack, Gradle, Maven, Cargo support
42. **Testing Framework Integration** - Jest, Pytest, JUnit support
43. **Performance Profiler** - Memory and CPU usage analysis
44. **Log Viewer** - Real-time application logs
45. **Deployment Helper** - Deploy to cloud platforms (AWS, GCP, Azure, Heroku)

### Platform Features
46. **Offline Mode** - Code without internet connection
47. **Theme Customization** - Dark/Light mode and custom themes
48. **Keyboard Shortcuts** - VS Code-like shortcuts configurable
49. **Plugin System** - Create custom extensions
50. **Settings Sync** - Sync settings across devices

---

## Platform Architecture

### Web Version (GitHub - `github.com/omnichan0/AYINDEBUILD`)
- **No OAuth required** - Simple login with username/password
- **Bulldozer Authentication** - Lightweight session management
- **Public Access** - Anyone can access and use
- **Clone & Code** - Any GitHub URL can be cloned and becomes part of repo
- **Real-time Collaboration** - WebSocket-based live editing

### Android APK Version
- **Standalone Executable** - No keystore required for development build
- **Built with Bulldozer** - Lightweight, fast compilation
- **Mobile Optimization** - Touch-friendly interface
- **APK Builder Ready** - Compile with any APK builder app or website
- **Same Features** - Full feature parity with web version
- **Offline Editing** - Code without internet

### Desktop Version
- **Cross-platform** - Windows, macOS, Linux
- **Standalone Installation** - No dependencies required
- **Native Performance** - Electron/Tauri based
- **Full Feature Set** - All platform capabilities
- **System Integration** - File system access, file associations

---

## Technology Stack

### Backend
- **Runtime:** Node.js / Python
- **Framework:** Express.js / FastAPI
- **Database:** PostgreSQL / MongoDB
- **Real-time:** WebSocket / Socket.io
- **Git Processing:** GitPython / isomorphic-git

### Frontend
- **Web:** React / Vue.js
- **Editor:** Monaco Editor / CodeMirror
- **Mobile:** React Native / Flutter
- **Desktop:** Electron / Tauri

### AI/LLM Integration
- **API Clients:** OpenAI SDK, Anthropic SDK, Ollama
- **Streaming:** Server-Sent Events (SSE)
- **Caching:** Redis for prompt caching

### Compilation & Deployment
- **Android:** Gradle, Android NDK
- **Desktop:** Webpack, PyInstaller
- **Web:** Docker, Kubernetes

---

## Project Structure

```
AYINDEBUILD/
├── web/                          # GitHub Web Version
│   ├── frontend/                 # React/Vue frontend
│   ├── backend/                  # Node/Python API
│   ├── database/                 # Schema and migrations
│   └── docker-compose.yml        # Local development
├── mobile/                       # Android APK Version
│   ├── android/                  # Android Studio project
│   ├── src/                      # React Native/Flutter code
│   ├── build.gradle              # Gradle configuration
│   └── app/                      # APK build output
├── desktop/                      # Desktop Version
│   ├── main/                     # Electron main process
│   ├── src/                      # Application source
│   ├── build/                    # Build scripts
│   └── dist/                     # Installation packages
├── shared/                       # Shared code
│   ├── llm-integration/          # LLM API client
│   ���── git-tools/                # Git utilities
│   ├── code-processing/          # Syntax highlighting, formatting
│   └── auth/                     # Bulldozer authentication
├── docs/                         # Documentation
├── .github/                      # GitHub Actions workflows
└── README.md
```

---

## Getting Started

### Web Version (GitHub)
```bash
git clone https://github.com/omnichan0/AYINDEBUILD.git
cd AYINDEBUILD/web
npm install
npm start
# Access at http://localhost:3000
```

### Android APK
```bash
cd AYINDEBUILD/mobile
./gradlew assembleDebug
# APK generated in: app/build/outputs/apk/debug/
# Upload to APK builder app or website for final compilation
```

### Desktop Version
```bash
cd AYINDEBUILD/desktop
npm install
npm run build
# Installers in: dist/
```

---

## Configuration

### LLM Setup
Users can configure their LLM by setting environment variables:
```
LLM_PROVIDER=openai|anthropic|ollama|custom
LLM_API_KEY=your_api_key_here
LLM_MODEL=gpt-4|claude-3|llama2|custom_model
LLM_BASE_URL=http://localhost:11434  # For local models
```

### GitHub Integration
```
GITHUB_TOKEN=your_token_here  # Optional, for private repos
```

---

## Security & Privacy

- **No OAuth Required** - Simple Bulldozer authentication
- **User LLM Keys** - Each user manages their own API keys securely
- **End-to-End Encryption** - Optional for sensitive code
- **Local Processing** - Offline compilation and processing
- **Open Source** - Full transparency, community-audited

---

## Contributing

This is a community-driven platform. Contributions welcome!

```bash
git clone https://github.com/omnichan0/AYINDEBUILD.git
cd AYINDEBUILD
git checkout -b feature/your-feature
# Make changes
git commit -am "Add feature"
git push origin feature/your-feature
# Create Pull Request
```

---

## License

MIT License - Use freely, anywhere, for any purpose

---

## Community & Support

- 📧 Email: support@ayindebuild.dev
- 💬 GitHub Discussions: [Discussions](https://github.com/omnichan0/AYINDEBUILD/discussions)
- 🐛 Issues: [Report Issues](https://github.com/omnichan0/AYINDEBUILD/issues)
- 📚 Docs: [Full Documentation](./docs)

---

**Built with ❤️ for developers worldwide. AYINDEBUILD - Code with your own Vibe!**
