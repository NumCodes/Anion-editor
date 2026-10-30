# An!on Editor

A lightweight, browser-based code playground for HTML, CSS, and JavaScript.

## Overview

An!on Editor gives front-end developers and learners a place to write, preview, and manage small web projects without leaving the browser. It keeps code, version history, tasks, and visual themes in one clean workspace so teams and solo builders can stay focused. Everything runs locally in the browser and persists between sessions, so users never have to set up a server or lose their work after closing a tab.

## System Architecture

```mermaid
flowchart LR
  User["Web Browser"]
  App["An!on Editor"]
  DB[("IndexedDB")]
  Cache["Cache Storage"]
  Plugins["Plugin Registry"]

  User --> App
  App --> DB
  App --> Cache
  App --> Plugins

  style User fill:#1e1b4b,stroke:#6366f1,stroke-width:2px,color:#fff
  style App fill:#2e1065,stroke:#8b5cf6,stroke-width:2px,color:#fff
  style DB fill:#0f172a,stroke:#3b82f6,stroke-width:2px,color:#fff
  style Cache fill:#4c0519,stroke:#ef4444,stroke-width:2px,color:#fff
  style Plugins fill:#022c22,stroke:#10b981,stroke-width:2px,color:#fff
```

## Features

- **Live code editor** with dedicated tabs for HTML, CSS, and JavaScript.
- **Real-time preview** rendered inside a sandboxed iframe.
- **Mirrored browser console** so `console.log`, `error`, `warn`, and `info` appear right in the editor.
- **Lightweight version control** that snapshots files and shows line-by-line diffs for each commit.
- **Integrated todo list** with color tags and human-readable timestamps.
- **Theme and plugin system** that downloads CSS themes and JS plugins on demand.
- **Library manager** for injecting external CSS and JavaScript dependencies into the preview.
- **Export options** for downloading a project as a single HTML file or backing up all local data.
- **Persistent local storage** so work, history, todos, plugins, and settings survive page reloads.

### Live Preview Flow

```mermaid
sequenceDiagram
  actor User
  participant Editor
  participant Store
  participant Preview

  User->>Editor: Types HTML, CSS, or JS
  Editor->>Store: Saves code
  Store->>Preview: Builds preview page
  Preview->>Store: Sends console messages
  Store->>Editor: Shows console output
```

### Version Control Flow

```mermaid
sequenceDiagram
  actor User
  participant Editor
  participant DB as Database
  participant History

  User->>Editor: Writes a commit note
  Editor->>DB: Fetches last saved files
  DB->>Editor: Returns previous snapshot
  Editor->>History: Stores diff and comment
  History->>DB: Saves new snapshot
```

### Plugin and Theme Flow

```mermaid
sequenceDiagram
  actor User
  participant Editor
  participant Registry
  participant Cache
  participant DB as Database
  participant Page

  User->>Editor: Chooses a theme or plugin
  Editor->>Registry: Fetches plugin file
  Registry->>Cache: Downloads file
  Cache->>DB: Stores plugin info
  DB->>Editor: Marks plugin active
  Editor->>Page: Applies theme or runs script
```

## Technologies Used

| Technology | Purpose | Link |
|---|---|---|
| TypeScript | Type-safe application logic | [typescriptlang.org](https://www.typescriptlang.org/) |
| Svelte | Reactive UI framework | [svelte.dev](https://svelte.dev/) |
| Vite | Fast build tooling and dev server | [vitejs.dev](https://vitejs.dev/) |
| CodeMirror | Language-aware code editing | [codemirror.net](https://codemirror.net/) |
| Dexie | Friendly wrapper for IndexedDB storage | [dexie.org](https://dexie.org/) |
| Beer CSS | Material Design component utilities | [beercss.com](https://www.beercss.com/) |

## Installation

- Clone the repository:

```bash
git clone <repository-url>
```

- Move into the project folder:

```bash
cd code-editor
```

- Install dependencies:

```bash
npm install
```

- Start the development server:

```bash
npm run dev
```

- Open the URL shown in your terminal, usually `http://localhost:5173`.

To create a production build:

```bash
npm run build
```

To preview the production build locally:

```bash
npm run preview
```

## Usage

When you open An!on Editor, you land in the code view with three tabs: HTML, CSS, and JavaScript. Type into any tab and the preview updates automatically.

```html
<h1>Hello, An!on</h1>
<button id="btn">Click me</button>
```

```css
body {
  font-family: sans-serif;
  text-align: center;
}
```

```js
document.getElementById('btn').addEventListener('click', () => {
  console.log('Button clicked');
});
```

The preview pane renders the result, and the console pane shows the message from `console.log`.

Use the bottom navigation to switch between:

- **Code** for editing.
- **Changes** to commit snapshots and review diffs.
- **Libraries** to add external CSS or JS files.
- **Todo** to track tasks.
- **Plugins** to install themes and extensions.
- **Settings** to toggle labels, manage metadata, and export or delete data.

To save a finished project, open Settings and choose **Export Data**, or use the export button to download a single self-contained `index.html` file.

## Contributing

Pull requests and issues are welcome. If you want to add a feature or fix a bug, open an issue first so we can discuss the change. Keep commits focused and include a short description of what changed.

## Author

Built by Ugochukwu Nweze.

- LinkedIn: [https://linkedin.com/in/ugochukwu-nweze-08812a2b8](https://linkedin.com/in/ugochukwu-nweze-08812a2b8)
- X: [https://x.com/CodesNum80638](https://x.com/CodesNum80638)

## Badges

[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Svelte](https://img.shields.io/badge/Svelte-FF3E00?style=for-the-badge&logo=svelte&logoColor=white)](https://svelte.dev/)
[![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev/)
[![CodeMirror](https://img.shields.io/badge/CodeMirror-000000?style=for-the-badge&logo=codemirror&logoColor=white)](https://codemirror.net/)
[![Dexie](https://img.shields.io/badge/Dexie-4B5563?style=for-the-badge&logo=javascript&logoColor=white)](https://dexie.org/)
