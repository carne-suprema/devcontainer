# Claude DevContainer

A reusable development container configuration for running Claude code in YOLO mode. (--dangerously-skip-permissions) This devcontainer provides a pre-configured environment optimized for AI-assisted development with Claude.

## 🎯 Purpose

This devcontainer is designed to provide a consistent, isolated development environment for projects that leverage Claude's AI capabilities. It comes pre-configured with essential tools and dependencies needed for modern AI-assisted development workflows.

## ✨ Features

- **Pre-configured AI development environment** - Ready-to-use setup for Claude-powered development
- **Isolated development space** - Consistent environment across different machines
- **YOLO mode optimized** - Configured for rapid prototyping and experimentation
- **Modern tooling** - Latest versions of essential development tools
- **Cross-platform compatibility** - Works on Windows, macOS, and Linux

## ⚡ Quick Start (One Liner)

```bash
curl -s https://raw.githubusercontent.com/carne-suprema/devcontainer/main/.devcontainer/devcontainer.json | mkdir -p .devcontainer && curl -s https://raw.githubusercontent.com/carne-suprema/devcontainer/main/.devcontainer/devcontainer.json -o .devcontainer/devcontainer.json && curl -s https://raw.githubusercontent.com/carne-suprema/devcontainer/main/.devcontainer/Dockerfile -o .devcontainer/Dockerfile && code .
```

This command downloads the `.devcontainer` folder and opens VS Code in one go!

## 🚀 Quick Start

### Prerequisites

- [Docker](https://www.docker.com/get-started) installed and running
- [VS Code](https://code.visualstudio.com/) with the [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
- [Git](https://git-scm.com/) for cloning the repository

### Installation

1. **Clone this repository:**

   ```bash
   git clone https://github.com/carne-suprema/devcontainer.git
   cd devcontainer
   ```

2. **Open in VS Code:**

   ```bash
   code .
   ```

3. **Start the devcontainer:**
   - When prompted, click "Reopen in Container"
   - Or use the command palette: `Ctrl/Cmd + Shift + P` → "Dev Containers: Reopen in Container"

### Alternative: Use as a Template

You can also use this devcontainer as a template for your own projects:

1. Copy the `.devcontainer` folder to your project
2. Customize the configuration as needed
3. Open your project in VS Code and start the devcontainer

## 📁 Repository Structure

```
devcontainer/
├── .devcontainer/
│   ├── devcontainer.json      # Main devcontainer configuration
│   └── Dockerfile             # Container image definition
└── README.md                  # This file
```

## 🔧 Configuration

The devcontainer is configured with:

- **Base Image**: Ubuntu-based with essential development tools
- **Extensions**: Pre-installed VS Code extensions for AI development
- **Settings**: Optimized VS Code settings for Claude workflows
- **Ports**: Common development ports pre-configured
- **Features**: Additional container features for enhanced development experience

## 🛠️ Customization

### Adding Extensions

Edit `.devcontainer/devcontainer.json` and add extensions to the `customizations.vscode.extensions` array:

```json
{
  "customizations": {
    "vscode": {
      "extensions": [
        "ms-vscode-remote.remote-containers",
        "your-extension-id"
      ]
    }
  }
}
```

### Modifying Dependencies

Update the `Dockerfile` to install additional packages or tools:

```dockerfile
# Add your custom installations here
RUN apt-get update && apt-get install -y \
    your-package \
    another-package
```

## 🚀 Usage

Once the devcontainer is running:

1. **Open a terminal** in VS Code (`Ctrl/Cmd + `` `)
2. **Start coding** - The environment is ready for Claude-assisted development
3. **Install project dependencies** as needed
4. **Run your applications** within the containerized environment
