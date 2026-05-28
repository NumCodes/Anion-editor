# An!on Code Editor

## Overview

This project gives you a full-featured, in-browser editor for HTML, CSS, and JavaScript. It helps you quickly write and test your frontend code by providing everything you need in one place, including a way to track your changes, manage external libraries, keep a to-do list, and even extend its capabilities with plugins. You don't need a complicated local setup; just open it up and start building.

## Description

An!on Code Editor is your all-in-one web development playground right in the browser. It's designed for developers who want a seamless environment to craft, preview, and manage their web projects without the hassle of context switching. With integrated version control, package management, a personal to-do list, and a robust plugin system, An!on empowers you to focus on coding and see your changes instantly.

## Installation

Getting An!on Code Editor up and running locally is super straightforward. Just follow these steps:

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/NumCodes/Anion-editor.git
    cd anion-editor
    ```

2.  **Install Dependencies:**
    ```bash
    npm install
    ```

3.  **Start the Development Server:**
    ```bash
    npm run dev
    ```
    This will typically open the application in your browser at `http://localhost:5173/` (or a similar address).

4.  **Build for Production (Optional):**
    If you want to create a production-ready build, run:
    ```bash
    npm run build
    ```
    This will generate optimized static files in the `dist` directory.

## Usage

Once you've launched An!on Code Editor, you'll find a clean interface ready for your web projects.

*   **Code Editor:** The main area lets you switch between HTML, CSS, and JavaScript tabs. Just type your code, and the preview panel updates in real-time.
*   **Live Preview:** See your web page render instantly in the dedicated preview section.
*   **Console Output:** An integrated console shows messages, warnings, and errors from your JavaScript, helping you debug on the fly.
*   **Navigation Panel:** Use the left-hand navigation to access different features:
    *   **Code:** Your primary HTML, CSS, JS editing environment.
    *   **Changes:** Review and commit your code changes. The editor tracks differences between your current work and previously committed versions. You'll see lines added and removed, making version control easy.
    *   **Libraries:** Manage external CSS and JavaScript libraries to include in your project.
    *   **Todo:** Keep track of tasks and notes directly within the editor.
    *   **Plugins:** Extend the editor's functionality with various plugins, including different themes.
    *   **Settings:** Customize editor behavior, toggle UI elements, and manage your data (export/delete).

Experiment with the settings to personalize your coding experience, and don't forget to commit your changes regularly!

## Features

An!on Code Editor comes packed with features to enhance your frontend development workflow:

*   **Real-time Code Editor:** Write HTML, CSS, and JavaScript with instant visual feedback in a live preview.
*   **Integrated Version Control:** Track changes, diff files, and commit your code directly within the editor, providing a lightweight version history.
*   **Client-side Library Management:** Easily add and manage external CSS and JavaScript libraries to your projects, simplifying dependency inclusion.
*   **Built-in To-Do Application:** Organize your tasks and keep development notes handy with a simple, integrated to-do list.
*   **Extensible Plugin System:** Personalize your environment by installing and managing themes and custom scripts.
*   **Customizable Editor Settings:** Adjust navigation labels, enable a "Theme Editor Mode" for direct CSS modification, manage plugin URLs, and add custom head metadata to your preview.
*   **Data Export and Import:** Export all your project data (code, changes, plugins, todos) as a JSON file for backup or sharing, with import functionality coming soon.
*   **Interactive Console Output:** View `console.log`, `error`, `warn`, and `info` messages from your previewed code directly in the editor's terminal.
*   **Persistent Data Storage:** Your code and settings are saved locally in your browser using IndexedDB, so your work persists across sessions.

## Technologies Used

This project leverages a modern web stack to deliver a fast and interactive user experience.

| Technology          | Description                                                    | Link                                            |
| :------------------ | :------------------------------------------------------------- | :---------------------------------------------- |
| **Svelte**          | A modern JavaScript framework for building user interfaces.    | [svelte.dev](https://svelte.dev/)               |
| **TypeScript**      | A typed superset of JavaScript that compiles to plain JavaScript. | [typescriptlang.org](https://www.typescriptlang.org/) |
| **Vite**            | A fast development build tool for modern web projects.         | [vitejs.dev](https://vitejs.dev/)               |
| **CodeMirror 6**    | A versatile text editor implemented in JavaScript for the browser. | [codemirror.net](https://codemirror.net/)       |
| **Dexie.js**        | A wrapper for IndexedDB, simplifying client-side database operations. | [dexie.org](https://dexie.org/)                 |
| **Diff.js**         | A JavaScript library for computing and displaying differences between texts. | [github.com/kpdecker/jsdiff](https://github.com/kpdecker/jsdiff) |
| **BeerCSS**         | A lightweight, Material Design-inspired CSS framework.         | [beercss.com](https://www.beercss.com/)         |
| **SortableJS**      | A JavaScript library for reorderable drag-and-drop lists.      | [sortablejs.github.io/Sortable/](https://sortablejs.github.io/Sortable/) |

## Contributing

We'd love for you to contribute to An!on Code Editor! Here's how you can help:

1.  **Fork the repository.**
2.  **Create a new branch** for your feature or bug fix: `git checkout -b feature/your-feature-name`.
3.  **Make your changes.**
4.  **Commit your changes** with a clear and concise message: `git commit -m "feat: Add new awesome feature"`.
5.  **Push to your branch:** `git push origin feature/your-feature-name`.
6.  **Open a Pull Request** explaining your changes and why they're beneficial.

Please ensure your code adheres to the existing style and conventions.

## License

This project currently does not have an explicit license.

## Author Info

*   **LinkedIn:** [Ugochukwu Nweze](http://linkedin.com/in/ugochukwu-nweze-08812a2b8/)
*   **X (Twitter):** [@CodesNum80638](https://x.com/CodesNum80638)

## Badges

![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Svelte](https://img.shields.io/badge/Svelte-FF3E00?style=for-the-badge&logo=svelte&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
