# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type-aware lint rules:

```js
export default tseslint.config([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...

      // Remove tseslint.configs.recommended and replace with this
      ...tseslint.configs.recommendedTypeChecked,
      // Alternatively, use this for stricter rules
      ...tseslint.configs.strictTypeChecked,
      // Optionally, add this for stylistic rules
      ...tseslint.configs.stylisticTypeChecked,

      // Other configs...
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```

You can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default tseslint.config([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...
      // Enable lint rules for React
      reactX.configs['recommended-typescript'],
      // Enable lint rules for React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```
# Dashboard Demo

A clean, responsive **dashboard UI** built with **React** and **TypeScript**, showcasing reusable components and interactive charts.  
🔗 **Live Demo:** [dashboard-demo-blush-ten.vercel.app](https://dashboard-demo-blush-ten.vercel.app/)

---

## ✨ Features

- ⚡ Built with **React + TypeScript** for type-safe development
- 🎨 Modular UI components:
  - `Header` – top navigation bar
  - `Aside` – sidebar navigation
  - `Cards` – summary/statistic tiles
  - `Input` – reusable form input field
- 🖼️ Rich visual assets (avatars, icons, logos, chart graphics) under `public/images`
- 📱 Responsive and clean design suitable for dashboards and admin panels

---

## 🚀 Demo

👉 [**Live Preview**](https://dashboard-demo-blush-ten.vercel.app/)  
Take a look at the deployed demo hosted on Vercel.

---

## ⚙️ Installation

```bash
# Clone repository
git clone https://github.com/Ana7K/Dashboard-demo.git
cd Dashboard-demo

# Install dependencies
npm install
# or
yarn install

# Run development server
npm start
# or
yarn dev
