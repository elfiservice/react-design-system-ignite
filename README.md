# Initial configuration
## Tailwindcss
- run `npm install -D tailwindcss postcss autoprefixer`
  - **postcss** is like a task manager to css (bundler css)
  - **autoprefixer** to be able to use prefixs like `webkit`, `moz` and so on in css rules
- after run `npx tailwindcss init -p`
  - to create the config files to tailwindcss and postcss
- in `tailwind.config.cjs``
  - provide the follow config
  - 
  ```
  module.exports = {
    content: [
      './src/**/*.tsx'
    ],
  ...
  }
  ```
  
- in `src/styles/global.css`
```
@tailwind base;
@tailwind utilities;
@tailwind components;

```

- and in `src/App.tsx`
```
import './styles/global.css';
...

```

## Storybook
- run `npx sb init --builder @storybook/builder-vite --use-npm`
  - using `--builder @storybook/builder-vite` to set the storybook using the vite comipler instead of babel 
  - and `use-npm` because i'm using the `npm`
  