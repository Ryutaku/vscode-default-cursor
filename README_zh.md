# VS Code 自定义光标样式

将 VS Code 的鼠标样式恢复为系统默认箭头指针。

在 VS Code 里，很多本应是「箭头」的地方（标签页、工具栏、资源管理器、设置页……）默认会显示「手形」光标。  
这份 CSS 把所有**非编辑区**的 `cursor:pointer / grab` 统一改回默认指针，**保留编辑器内文本 I-beam 与 Ctrl+跳转小手**，让界面回归传统桌面软件直觉。

---

## 🚀 一键食用

1. 安装插件 [Custom CSS and JS Loader](https://marketplace.visualstudio.com/items?itemName=be5invis.vscode-custom-css)  
2. 把本仓库 `vscode-default-cursor.css` 保存到本地任意路径（例如： `C:\\Users\\Administrator\\Documents\\vscode-default-cursor.css`）  
3. 打开 VS Code 的**用户设置 settings.json** → 填入刚才的文件绝对路径  
   ```
    "vscode_custom_css.imports": [
        "file:///C:\\Users\\Administrator\\Documents\\vscode-default-cursor.css" // <-- 替换为你自己的 CSS 文件路径
    ],
   ``` 
4. **重启 VS Code** → 右下角弹窗点 **「Restart」**  
5. 享受「全屏都是箭头」的清爽体验！

---

## 🎯 覆盖范围

| 区域 | 改造后光标 |
|---|---|
| 标签页（含关闭、拆分图标） | ➡️ 默认指针 |
| 活动栏（左侧一排图标） | ➡️ 默认指针 |
| 资源管理器 / 扩展市场 | ➡️ 默认指针 |
| 菜单栏 & 下拉菜单 | ➡️ 默认指针 |
| 命令面板 | ➡️ 默认指针 |
| 设置页左侧树、下拉框、复选框 | ➡️ 默认指针 |
| 工具栏、状态栏、通知按钮 | ➡️ 默认指针 |
| **代码编辑区** | 文本 I-beam 保留；Ctrl+跳转小手保留 |

---

## 📄 CSS 内容（直接复制也可）

```css
/* ===== 0. 编辑区保持原样 ===== */
.monaco-editor .view-lines            { cursor: text  !important; }
.monaco-editor .margin                { cursor: default !important; }
.monaco-editor .goto-definition-link  { cursor: pointer !important; }

/* ===== 1. 标签页 + 图标 ===== */
.monaco-workbench .tabs-container,
.monaco-workbench .tabs-container * {
    cursor: default !important;
}

/* ===== 2. 菜单栏 & 下拉 ===== */
.monaco-workbench .part.menubar,
.monaco-workbench .part.menubar *,
.monaco-menu .monaco-action-bar .action-item,
.monaco-menu .monaco-action-bar .action-item * {
    cursor: default !important;
}

/* ===== 3. 命令面板 ===== */
.monaco-quick-open-widget,
.monaco-quick-open-widget * {
    cursor: default !important;
}

/* ===== 4. 活动栏 / 侧边栏 / 面板 / 标题栏 ===== */
.monaco-workbench .part.activitybar,
.monaco-workbench .part.sidebar,
.monaco-workbench .part.panel,
.monaco-workbench .part.titlebar {
    cursor: default !important;
}

/* ===== 5. 资源管理器 ===== */
.monaco-workbench .explorer-viewlet,
.monaco-workbench .explorer-viewlet * {
    cursor: default !important;
}

/* ===== 6. 扩展市场 ===== */
.monaco-workbench .extensions-viewlet,
.monaco-workbench .extensions-viewlet * {
    cursor: default !important;
}

/* ===== 7. 工具栏 ===== */
.monaco-toolbar * {
    cursor: default !important;
}

/* ===== 8. 状态栏 ===== */
.statusbar-item * {
    cursor: default !important;
}

/* ===== 9. 左侧通用 action-bar ===== */
.monaco-action-bar .action-item * {
    cursor: default !important;
}

/* ===== 10. 设置页左侧树 ===== */
.monaco-tl-row * {
    cursor: default !important;
}

/* ===== 11. 设置页控件 ===== */
select * {
    cursor: default !important;
}

/* ===== 12. 通知 & 按钮 ===== */
.notification-list-item *,
.button-container * {
    cursor: default !important;
}
