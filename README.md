# Adlib Blue - VS Code Theme

A beautiful dark blue color theme for Visual Studio Code inspired by Adlib Tracker II. The theme is designed to provide a pleasant color environment for long programming sessions.

## Features

- 🎨 **Dark blue color scheme** - A combination of dark blues and light cyan colors
- 👁️ **Eye-friendly** - Specially designed to reduce eye strain
- 💻 **All languages supported** - Compatible with all programming languages
- 🎯 **Clean design** - Minimalist and professional appearance

## Installation

### Manual Installation
1. Download the VSIX file
2. In the terminal, run: `code --install-extension sabladav-blue-0.0.1.vsix`
3. Restart VS Code

## Activating the Theme

After installation, you can activate the theme:

1. **Via command palette**: Press `Ctrl+Shift+P` and type "Preferences: Color Theme"
2. Select **"Sabladav Blue"** from the list

## Creating a VSIX File

VSIX is the packaging format for VS Code extensions. Here's how to create a VSIX for this theme:

### Requirements

- Node.js and npm (https://nodejs.org/)
- vsce (VS Code Extension CLI)

### Installing Tools

```bash
npm install -g vsce
```

### Preparing the Package

1. Verify that you have the correct information in `package.json`:
   ```json
   {
     "name": "sabladav-blue",
     "displayName": "Sabladav Blue",
     "description": "A beautiful dark blue color theme for VS Code",
     "publisher": "sabladav",
     "version": "0.0.1",
       "vscode": "^1.0.0"
     },
     "categories": ["Themes"],
     "contributes": {
       "themes": [
         {
           "label": "Adlib Blue",
           "uiTheme": "vs-dark",
           "path": "./themes/sabladav-blue-color-theme.json"
         }
       ]
     }
   }
   ```

   **Important**: Replace `"publisher"` with your username from Azure DevOps

2. Make sure you have all required files:
   ```
   adlib-blue/
   ├── package.json
   ├── README.md (this file)
   ├── LICENSE (recommended)
   └── themes/
       └── sabladav-blue-color-theme.json
   ```

### Creating the VSIX

In the project directory, run:

```bash
vsce package
```

This command will create a file named `sabladav-blue-0.0.1.vsix` (version number varies based on your package).

### Verifying the VSIX

```bash
# Using vsce
vsce ls

# Installing the created VSIX
code --install-extension sabladav-blue-0.0.1.vsix
```

## License

MIT - See LICENSE file for more information
---

**Author**: David Sablatura  
**Version**: 0.0.1  
**VS Code Marketplace**: [Sabladav Blue](https://marketplace.visualstudio.com/)
