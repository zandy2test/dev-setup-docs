# 🔧 VS Code Settings & Configuration Backup

**Complete backup of your VS Code development environment for easy restoration**

---

## 📋 **Installed Extensions (WSL)**

**Essential Extensions Currently Installed:**

| Extension | Version | Purpose |
|-----------|---------|---------|
| **Cline (claude-dev)** | 3.18.14 | AI development assistant |
| **Prettier** | 11.0.0 | Code auto-formatting |
| **Live Server** | 5.7.9 | Local development server |
| **GitLens** | 17.3.0 | Git history and blame information |
| **REST Client** | 0.25.1 | API testing within VS Code |

---

## 🚀 **Quick Extension Installation Command**

To restore all extensions on a new machine (WSL):
```bash
code --install-extension eamodio.gitlens@17.3.0
code --install-extension esbenp.prettier-vscode@11.0.0
code --install-extension humao.rest-client@0.25.1
code --install-extension ritwickdey.liveserver@5.7.9
code --install-extension saoudrizwan.claude-dev@3.18.14
```

**Alternative - One Line Installation:**
```bash
code --install-extension eamodio.gitlens@17.3.0 && code --install-extension esbenp.prettier-vscode@11.0.0 && code --install-extension humao.rest-client@0.25.1 && code --install-extension ritwickdey.liveserver@5.7.9 && code --install-extension saoudrizwan.claude-dev@3.18.14
```

---

## ⚙️ **VS Code Settings**

**Note:** Your VS Code settings may be managed through Settings Sync (synced to Microsoft account) or stored locally.

### **Key Settings Applied (Based on Setup Documentation):**

```json
{
  "files.autoSave": "afterDelay",
  "files.autoSaveDelay": 1000,
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "terminal.integrated.defaultProfile.linux": "bash",
  "terminal.integrated.shellIntegration.enabled": true,
  "git.enableSmartCommit": true,
  "git.autofetch": true,
  "editor.bracketPairColorization.enabled": true,
  "editor.minimap.enabled": true,
  "liveServer.settings.donotShowInfoMsg": true,
  "todo-tree.highlights.enabled": true,
  "projectManager.baseFolder": "/mnt/c/Users/zakko/Desktop/cline-projects"
}
```

### **To Backup Current Settings:**

1. **Via VS Code UI:**
   - `Ctrl+Shift+P` → "Preferences: Open Settings (JSON)"
   - Copy the entire content to backup

2. **Via File System:**
   ```bash
   # Check if settings exist in WSL
   ls -la ~/.vscode-server/data/User/settings.json
   
   # If exists, backup with:
   cp ~/.vscode-server/data/User/settings.json ~/vscode-settings-backup.json
   ```

3. **Enable Settings Sync (Recommended):**
   - `Ctrl+Shift+P` → "Settings Sync: Turn On"
   - Sign in with Microsoft account
   - All settings automatically sync across devices

---

## 🎯 **Workspace Configuration**

**Current Project Structure:**
```
/mnt/c/Users/zakko/Desktop/cline-projects/
├── dev-setup-docs/          # This documentation project
├── hello-cline-demo/         # Demo project
├── workflow-test/            # Test project
└── [future projects]
```

**Project Manager Configuration:**
- Base folder: `/mnt/c/Users/zakko/Desktop/cline-projects`
- Auto-scans for new projects
- Quick switching with `Ctrl+Alt+P`

---

## 🔄 **Restoration Process**

### **On New Machine (WSL Setup):**

1. **Install WSL2 and Ubuntu**
2. **Install VS Code with WSL extension**
3. **Open VS Code in WSL mode**
4. **Install extensions** (use commands above)
5. **Apply settings** (either via Settings Sync or manual JSON)
6. **Configure Project Manager** base folder
7. **Clone your projects** from GitHub

### **Quick Setup Script:**
```bash
# Navigate to projects folder
cd /mnt/c/Users/zakko/Desktop/cline-projects

# Clone this documentation
git clone https://github.com/zandy2test/dev-setup-docs.git

# Install all extensions
code --install-extension eamodio.gitlens@17.3.0 && code --install-extension esbenp.prettier-vscode@11.0.0 && code --install-extension humao.rest-client@0.25.1 && code --install-extension ritwickdey.liveserver@5.7.9 && code --install-extension saoudrizwan.claude-dev@3.18.14

# Open VS Code
code .
```

---

## 📝 **Additional Extensions (Optional)**

**Extensions mentioned in documentation but not currently installed:**
- `gruntfuggly.todo-tree` - Visual TODO/FIXME tracking
- `alefragnani.project-manager` - Enhanced project management

**To install if needed:**
```bash
code --install-extension gruntfuggly.todo-tree
code --install-extension alefragnani.project-manager
```

---

## 💡 **Pro Tips**

1. **Settings Sync** - Enable this for automatic backup across all devices
2. **Extension Sync** - Settings Sync also handles extensions automatically
3. **Regular Updates** - Extensions auto-update, but you can disable this per-extension
4. **Profile Management** - VS Code supports multiple profiles for different workflows

---

## 🔄 **Keeping This Backup Current**

**Update this file when you:**
- Install new extensions
- Change important settings
- Add new projects or workspaces
- Modify VS Code configuration

**Quick check command:**
```bash
code --list-extensions --show-versions
```

---

**Last Updated:** January 13, 2025  
**Environment:** WSL2 Ubuntu with VS Code Remote Development
