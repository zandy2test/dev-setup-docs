# 🐧 WSL Command Quick Reference - PowerShell to Bash

**Your handy cheat sheet for transitioning from PowerShell to bash commands in WSL**

---

## 📁 **Directory & File Operations**

| Task | PowerShell (Old) | Bash (New) | Example |
|------|------------------|------------|---------|
| **List files** | `dir` or `ls` | `ls` or `ls -la` | `ls -la` (detailed list) |
| **Change directory** | `cd foldername` | `cd foldername` | `cd hello-cline-demo` |
| **Current directory** | `pwd` | `pwd` | `pwd` |
| **Go to home** | `cd ~` | `cd ~` | `cd ~` |
| **Go up one level** | `cd ..` | `cd ..` | `cd ..` |
| **Create directory** | `mkdir foldername` | `mkdir foldername` | `mkdir new-project` |
| **Create file** | `New-Item file.txt` | `touch file.txt` | `touch README.md` |
| **View file** | `Get-Content file.txt` | `cat file.txt` | `cat package.json` |
| **Copy file** | `Copy-Item src dest` | `cp src dest` | `cp index.html backup.html` |
| **Move/rename** | `Move-Item old new` | `mv old new` | `mv old-name.js new-name.js` |
| **Delete file** | `Remove-Item file.txt` | `rm file.txt` | `rm temp.log` |
| **Delete directory** | `Remove-Item -Recurse folder` | `rm -rf folder` | `rm -rf node_modules` |

---

## 🔍 **Search & Find**

| Task | PowerShell (Old) | Bash (New) | Example |
|------|------------------|------------|---------|
| **Find files** | `Get-ChildItem -Recurse -Name "*.js"` | `find . -name "*.js"` | `find . -name "*.md"` |
| **Search in files** | `Select-String "text" *.js` | `grep "text" *.js` | `grep "TODO" *.js` |
| **Search recursively** | `Select-String -Recurse "text"` | `grep -r "text" .` | `grep -r "function" src/` |

---

## 📄 **Text & File Content**

| Task | PowerShell (Old) | Bash (New) | Example |
|------|------------------|------------|---------|
| **Display text** | `Write-Host "Hello"` | `echo "Hello"` | `echo "Build complete"` |
| **First few lines** | `Get-Content file.txt -Head 10` | `head -10 file.txt` | `head -5 error.log` |
| **Last few lines** | `Get-Content file.txt -Tail 10` | `tail -10 file.txt` | `tail -20 server.log` |
| **Count lines** | `(Get-Content file.txt).Count` | `wc -l file.txt` | `wc -l README.md` |

---

## 🌐 **Network & Downloads**

| Task | PowerShell (Old) | Bash (New) | Example |
|------|------------------|------------|---------|
| **Download file** | `Invoke-WebRequest -Uri url -OutFile file` | `curl -o file url` | `curl -o setup.sh https://get.node.js` |
| **Test connection** | `Test-NetConnection google.com` | `ping google.com` | `ping github.com` |

---

## 🔧 **Development Commands**

| Task | PowerShell/Bash | Notes |
|------|-----------------|-------|
| **Git commands** | `git status`, `git add .`, `git commit -m "message"` | **Same in both!** |
| **Node.js** | `node app.js` | **Same in both!** |
| **NPM** | `npm install`, `npm start`, `npm run build` | **Same in both!** |
| **VS Code** | `code .`, `code filename.js` | **Same in both!** |

---

## 🎯 **Essential Bash-Specific Tips**

### **File Permissions:**
```bash
# Make file executable
chmod +x script.sh

# Check file permissions
ls -la filename
```

### **Environment Variables:**
```bash
# View environment variable
echo $HOME
echo $PATH

# Set temporary variable
export MY_VAR="value"
```

### **Process Management:**
```bash
# See running processes
ps aux

# Kill process by name
pkill process-name

# Background a process
command &
```

---

## 🚀 **Your Most Common Commands**

**Daily Development Workflow:**
```bash
# Navigate to project
cd /mnt/c/Users/zakko/Desktop/cline-projects/my-project

# Check Git status
git status

# List files
ls -la

# View package.json
cat package.json

# Install dependencies
npm install

# Start development server
npm start

# Check what's running
ps aux | grep node
```

**File Management:**
```bash
# Create new project structure
mkdir my-new-project && cd my-new-project
touch README.md index.html style.css script.js

# Quick file peek
head -10 README.md

# Find specific files
find . -name "*.json"

# Search for TODO comments
grep -r "TODO" .
```

---

## 🎨 **Bash Shortcuts You'll Love**

| Shortcut | Action | Example |
|----------|--------|---------|
| **Tab** | Auto-complete | Type `cd hel` + Tab → `cd hello-cline-demo` |
| **Ctrl+C** | Cancel current command | Stop a running process |
| **Ctrl+L** | Clear screen | Clean terminal view |
| **Up Arrow** | Previous command | Repeat last command |
| **Ctrl+R** | Search command history | Find previously used commands |
| **!!** | Repeat last command | `sudo !!` (run last command with sudo) |

---

## 🔄 **Path Translation Helper**

**Windows Path → WSL Path:**
```
C:\Users\zakko\Desktop\cline-projects
↓
/mnt/c/Users/zakko/Desktop/cline-projects
```

**Quick Navigation:**
```bash
# Your main project folder
cd /mnt/c/Users/zakko/Desktop/cline-projects

# Alternative: if you're already in terminal
cd cline-projects  # (if you're in Desktop)
```

---

## ⚠️ **Important Differences**

### **Case Sensitivity:**
- **Windows/PowerShell:** `README.md` = `readme.md` = `ReadMe.Md`
- **Linux/Bash:** `README.md` ≠ `readme.md` ≠ `ReadMe.Md`

### **File Paths:**
- **Windows:** Uses backslashes `\` 
- **Linux:** Uses forward slashes `/`

### **File Extensions:**
- **Windows:** `.exe` files for programs
- **Linux:** No extension needed, uses file permissions

---

## 🆘 **When You Get Stuck**

**Command Help:**
```bash
# Get help for any command
man command-name        # Detailed manual
command-name --help     # Quick help
```

**Common Fixes:**
```bash
# If command not found
which command-name      # Check if installed
echo $PATH             # Check your PATH

# If permission denied
chmod +x filename      # Make executable
sudo command           # Run as administrator
```

---

## 🎊 **Pro Tips**

1. **Use Tab completion** - It's your best friend for long file names
2. **Arrow keys** - Up/Down to cycle through command history
3. **Ctrl+R** - Search your command history quickly
4. **Copy/Paste** - Right-click in terminal for context menu
5. **Multiple commands** - Use `&&` to chain: `npm install && npm start`

---

**Remember:** Most of your development workflow stays exactly the same - Git, npm, VS Code all work identically. You're just using different commands for basic file operations!

**🚀 You've got this! The bash commands will become second nature in just a few days.**
