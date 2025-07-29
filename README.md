Here’s the **complete README.md** file you can copy and paste directly into your project:

---

````markdown
# React + Vite + Tailwind CSS v4 Setup

This template provides a minimal setup to get React working in Vite with HMR, ESLint rules, and Tailwind CSS v4 integration using the latest PostCSS setup.

Currently, two official Vite React plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) — uses [Babel](https://babeljs.io/) for Fast Refresh.
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) — uses [SWC](https://swc.rs/) for Fast Refresh.

---

## 1️⃣ Create Vite Project

```bash
npm create vite@latest
cd my-project
````

---

## 2️⃣ Remove any old Tailwind installation

```bash
npm uninstall -g tailwindcss
npm uninstall tailwindcss
```

---

## 3️⃣ Install Tailwind v4 + CLI + PostCSS + Autoprefixer

```bash
npm install -D tailwindcss@latest @tailwindcss/cli postcss autoprefixer
```

---

## 4️⃣ Initialize Tailwind Config

```bash
npx tailwindcss init -p
```

**`tailwind.config.js`**

```js
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

---

## 5️⃣ Install Tailwind Vite Plugin

```bash
npm install tailwindcss @tailwindcss/vite
```

---

## 6️⃣ Configure Vite (`vite.config.ts` or `vite.config.js`)

```ts
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'
import tailwindcss from '@tailwindcss/vite'

export default defineConfig({
  plugins: [
    react(),
    tailwindcss(),
  ],
})
```

---

## 7️⃣ Import Tailwind in CSS (`src/index.css` or `src/App.css`)

```css
@import "tailwindcss";
```

---

## 8️⃣ Install Tailwind PostCSS Plugin

```bash
npm install @tailwindcss/postcss
```

---

## 9️⃣ Configure PostCSS (`postcss.config.js`)

```js
export default {
  plugins: {
    '@tailwindcss/postcss': {}, // NEW way in Tailwind v4
  },
};
```

---

## 🔟 Run Dev Server

```bash
npm run dev
```

Now Tailwind will automatically work with Vite HMR — no manual build commands needed.

```

---

Do you want me to also give you a **ready-made zip** with this README and config files so you can just drop it into your project?  
That would save you setup time.
```
