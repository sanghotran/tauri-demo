# Tauri + Vanilla

This template should help get you started developing with Tauri in vanilla HTML, CSS and Javascript.

## Recommended IDE Setup

- [VS Code](https://code.visualstudio.com/) + [Tauri](https://marketplace.visualstudio.com/items?itemName=tauri-apps.tauri-vscode) + [rust-analyzer](https://marketplace.visualstudio.com/items?itemName=rust-lang.rust-analyzer)


# SUMARY

1. Dùng Tauri build exe
    - cài nodejs local
    - build trên github
2. lệnh tạo project:
```bash
    npm create tauri-app@latest
```
3. Cấu trúc thư mục
    src: html, js, css
    src-tauri: icon, app name, config window
    .github/workflows: yml
4. Giao diện
    - dùng data-number đánh dấu phần tử trong html, giúp js tìm dễ hơn
    - Glassmorphism: 
        background: rbga(...);
        backdrop-filter: blur(...);
    - Flexbox: căn giữa
        display: flex;
        justify-content: center;
        align-items: center;
    - Bỏ cuộn:
        overflow: hidden
5. Logic
    - Click chuột:
        addEventListener('clicl', ...)
    - Bàn phím:
        document.addEventListener('keydown', ...)
6. Config tauri
    - width-window = width-css + 20
    - height-window = height-css + 20
    - resizable: false
    - maximizable: false
    - center: true
7. Test local
```bash
    npx vite src
```
8. Build
```bash
    git push
```
9. Note
    config:
        withGlobalTauri: true
        decorations: false
        transparent: true
    frontend:
        html: không dùng type=module
        js: không dùng import
        const invoke = window.__TAURI__ ? window.__TAURI__.core.invoke : null;
        thêm data-tauri-drag-region vào title bar
    backend:
        viết hàm trong lib.rs



