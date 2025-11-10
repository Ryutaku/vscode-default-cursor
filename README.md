# vscode-pointer-arrow

Restore VS Code's mouse cursor to the system default arrow pointer.

Tired of the “hand” cursor showing up everywhere in VS Code?  
This single CSS file turns **all unnecessary hand / grab cursors back to the default arrow**, while keeping the editor’s I-beam and Ctrl+click “go-to-definition” hand intact.  
It feels like a native desktop app again.

---

## 🚀 Quick Start

1. Install the extension [Custom CSS and JS Loader](https://marketplace.visualstudio.com/items?itemName=be5invis.vscode-custom-css)
2. Save this repo’s file `vscode-default-cursor.css` anywhere you like (e.g. `C:\\Users\\Administrator\\Documents\\vscode-default-cursor.css`)
3. Open VS Code **settings.json** → search `vscode_custom_css.imports` → paste the **absolute path** of the file as below:  
   ```
    "vscode_custom_css.imports": [
        "file:///C:\\Users\\Administrator\\Documents\\vscode-default-cursor.css"
    ],
   ```
4. Restart VS Code when prompted
5. Enjoy a **hand-free** workspace!

---

## ✅ What Becomes an Arrow

| Area | Cursor After |
|---|---|
| Tabs (close, split, preview icons) | default |
| Activity Bar (leftmost icons) | default |
| Explorer / Extensions view | default |
| Menus & context menus | default |
| Command Palette | default |
| Settings tree, drop-downs, checkboxes | default |
| Tool-bars, status-bar, notifications | default |
| **Editor surface** | I-beam kept |
| **Ctrl + hover “go-to-definition”** | hand kept |

---

