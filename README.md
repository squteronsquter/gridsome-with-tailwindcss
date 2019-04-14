# Gridsome with Tailwind

### 1. Install Gridsome CLI tool if you have not done so yet

```
npm install --global @gridsome/cli
```

### 2. Create a Gridsome project

1. `gridsome create my-shining-website` to install default starter
2. `cd my-shining-website` to open the folder
3. `npm install -D gridsome-plugin-tailwindcss` install gridsome plugin
4. `touch gridsome.config.js` tell gridsome where tailwind configuration file is:

```
plugins: [
  {
    use: 'gridsome-plugin-tailwindcss',
    options: {
      config: './tailwind.js'
    }
  }
]
```

5. Tell Gridsome where the styles.css file with Tailwind classes imports is:

```
import './assets/styles.css'
```

Create your styles.css file inside /src/assests folder

```
touch /src/assets/styles.css
```

Inside thnsi file you will need these three lines (documented at TaiwindCSS website)

```
@tailwind preflight;
@tailwind components;
@tailwind utilities;
```

Add Tailwind CSS by creating Tailwind configuration file

```
npx tailwind init tailwind.js
```

Then run the development server to check if everuthing works fine:

```
gridsome develop
```

to start a local dev server go to `http://localhost:8080`

**_Happy coding_**
