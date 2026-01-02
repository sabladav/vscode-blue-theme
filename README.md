# Adlib Blue - VS Code Theme

A beautiful dark blue color theme for Visual Studio Code. The theme is designed to provide a pleasant color environment for long programming sessions.

## Features

- 🎨 **Dark blue color scheme** - A combination of dark blues and light cyan colors
- 👁️ **Eye-friendly** - Specially designed to reduce eye strain
- 💻 **All languages supported** - Compatible with all programming languages
- 🎯 **Clean design** - Minimalist and professional appearance

## Installation

### From Visual Studio Code Marketplace
1. Open VS Code
2. Go to the Extensions tab (Ctrl+Shift+X)
3. Search for "Adlib Blue"
4. Click "Install"
5. Activate the theme: Ctrl+K Ctrl+T and select "Adlib Blue"

### Manual Installation
1. Download the VSIX file
2. In the terminal, run: `code --install-extension adlib-blue-0.0.1.vsix`
3. Restart VS Code

## Activating the Theme

After installation, you can activate the theme:

1. **Via command palette**: Press `Ctrl+Shift+P` and type "Preferences: Color Theme"
2. Select **"Adlib Blue"** from the list

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
     "name": "adlib-blue",
     "displayName": "Adlib Blue",
     "description": "A beautiful dark blue color theme for VS Code",
     "publisher": "your-publisher-name",
     "version": "0.0.1",
     "engines": {
       "vscode": "^1.0.0"
     },
     "categories": ["Themes"],
     "contributes": {
       "themes": [
         {
           "label": "Adlib Blue",
           "uiTheme": "vs-dark",
           "path": "./themes/adlib-blue-color-theme.json"
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
       └── adlib-blue-color-theme.json
   ```

### Creating the VSIX

In the project directory, run:

```bash
vsce package
```

This command will create a file named `adlib-blue-0.0.1.vsix` (version number varies based on your package).

### Verifying the VSIX

```bash
# Using vsce
vsce ls

# Installing the created VSIX
code --install-extension adlib-blue-0.0.1.vsix
```

## Publishing to VS Code Marketplace

If you want to publish the theme to the official marketplace:

1. Create an account on [Visual Studio Marketplace](https://marketplace.visualstudio.com/)
2. Create a Publisher token at https://dev.azure.com/
3. Log in via vsce:
   ```bash
   vsce login <publisher-name>
   ```
4. Publish the extension:
   ```bash
   vsce publish
   ```

Or publish a specific version:
```bash
vsce publish patch  # increases patch version (0.0.1 → 0.0.2)
vsce publish minor  # increases minor version (0.0.1 → 0.1.0)
vsce publish major  # increases major version (0.0.1 → 1.0.0)
```

## Dependencies and Requirements

- Visual Studio Code v1.0.0 or newer
- No other dependencies

## Troubleshooting

**Theme is not displaying:**
- Make sure you have activated the correct theme (Ctrl+Shift+P → Color Theme)
- Restart VS Code
- Try uninstalling and reinstalling

**VSIX cannot be created:**
- Check that `vsce` is properly installed: `vsce --version`
- Verify the contents of `package.json` - it must have a correct structure
- Make sure you have the correct permissions for the directory

## Contributing

If you have suggestions or want to contribute, create an issue or pull request.

## License

MIT - See LICENSE file for more information

---

**Author**: David Sablatura  
**Version**: 0.0.1  
**VS Code Marketplace**: [Adlib Blue](https://marketplace.visualstudio.com/)
