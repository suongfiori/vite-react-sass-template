# Vite React JavaScript with Sass Setup Guide

This guide provides step-by-step instructions on creating a React JavaScript project using Vite and adding Sass to it.

## Project Structure

Here is an example of a project structure

```
my-project/
├── node_modules/
├── src/
│   ├── assets/
│   │   └── styles/
│   │   │   ├── main.scss
│   │   │   └── variables.scss
│   │   ├── images/
│   │   └── fonts/
│   ├── components/
│   │   ├── Header.jsx
│   │   ├── Footer.jsx
│   │   ├── Sidebar.jsx
│   │   └── MainContent.jsx
│   ├── App.jsx
│   └── main.jsx
├── index.html
├── .gitignore
├── package.json
├── README.md
└── vite.config.js
```

## Steps

1. Open your terminal and navigate to the directory where you want to create the project.

2. Run the command `npm create vite@latest <project-name> --template react`, replacing `<project-name>` with the name of your project. 
    ```bash
    npm create vite@latest my-project --template react
    ```

3. Once the project is created, navigate into the project directory using `cd <project-name>`.

    ```bash
    cd my-project
    ```

4. Run `npm install` to install the dependencies.

    ```bash
    npm install
    ```

5. Open the project in Visual Studio Code.
Navigate to your project directory and open the project in Visual Studio Code

 ```bash
cd project-path/ code .
 ```

6. To start the project, run `npm run dev`.

    ```bash
    npm run dev
    ```

7. In a new terminal, run `npm add -D sass` to add Sass to your project as a devDependency.

    ```bash
    npm add -D sass
    ```

8. You can start using Sass in your project. As a test, create an empty div with an h1 tag saying "Hello World" in your `App.jsx` file.

    ```jsx
    function App() {
      return (
        <div>
          <h1>Hello World</h1>
        </div>
      );
    }

    export default App;
    ```

9. Remove any unused state and delete the logo and CSS files (e.g. App.css).

10. Create a new folder "styles" and add a "main.scss" file.
11. Create a new file to store all variables "variables.scss"
```
// Declare SCSS variables
$primary-color: #333;
$secondary-color: #ccc;
$font-stack: Helvetica, sans-serif;

// Add more variables as needed
```
12. import "variables.scss" to "main.scss"
```
@use './variables.scss' as *;

//example
body {
    background: $secondary;
    font-size: 16px;
}

h1 {
    color: $primary;
    border: 5px solid $accent;
    padding: 0.5rem 1rem;
    font-family: $font-stack;
}

```
13. To use this style, import it in your `App.jsx` by adding `import './styles/main.scss'`.

    ```jsx
    import './styles/main.scss';

    function App() {
      return (
        <div>
          <h1>Hello World</h1>
        </div>
      );
    }

    export default App;
    ```

