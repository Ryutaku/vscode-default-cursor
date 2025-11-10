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

## 📄 CSS Snippet (copy-and-paste)

```css
/* 0. leave editor untouched */
.monaco-editor .view-lines            { cursor: text  !important; }
.monaco-editor .margin                { cursor: default !important; }
.monaco-editor .goto-definition-link  { cursor: pointer !important; }

/* 1. tabs and icons */
.monaco-workbench .tabs-container,
.monaco-workbench .tabs-container * {
    cursor: default !important;
}

/* 2. menu bar & drop-downs */
.monaco-workbench .part.menubar,
.monaco-workbench .part.menubar *,
.monaco-menu .monaco-action-bar .action-item,
.monaco-menu .monaco-action-bar .action-item * {
    cursor: default !important;
}

/* 3. command palette */
.monaco-quick-open-widget,
.monaco-quick-open-widget * {
    cursor: default !important;
}

/* 4. activity / side / panel / title bars */
.monaco-workbench .part.activitybar,
.monaco-workbench .part.sidebar,
.monaco-workbench .part.panel,
.monaco-workbench .part.titlebar {
    cursor: default !important;
}

/* 5. explorer */
.monaco-workbench .explorer-viewlet,
.monaco-workbench .explorer-viewlet * {
    cursor: default !important;
}

/* 6. extensions */
.monaco-workbench .extensions-viewlet,
.monaco-workbench .extensions-viewlet * {
    cursor: default !important;
}

/* 7. tool-bar */
.monaco-toolbar * {
    cursor: default !important;
}

/* 8. status-bar */
.statusbar-item * {
    cursor: default !important;
}

/* 9. generic action bars (left, right, bottom) */
.monaco-action-bar .action-item * {
    cursor: default !important;
}

/* 10. settings tree */
.monaco-tl-row * {
    cursor: default !important;
}

/* 11. settings controls */
select * {
    cursor: default !important;
}

/* 12. notifications & buttons */
.notification-list-item *,
.button-container * {
    cursor: default !important;
}
