# Vite React JavaScript with Sass Setup

Step-by-step template for setting up a React JavaScript project with Vite and Sass

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

## Getting Started

1. Open the terminal and navigate to the directory where you want to create the project.
2. Initializing a new React project using the latest version of Vite: `npm create vite@latest my-project --template react`
3. Navigate into the project directory `cd my-project`
4. Run `npm install` to install the dependencies.
5. Install Sass: `npm add -D sass` (add Sass to the project as a devDependency)
6. To start the project, run `npm run dev`.
7. Open the project in Visual Studio Code: `code .`

#### In Visual Studio Code:

8. Remove any unused content/files (e.g states, logos and CSS files).
9. Inside the 'assets' folder, create a 'styles' subfolder and add two files: 'main.scss' and 'variables.scss'.
   The 'variables.scss' file will be used to store all Sass variables.
10. Import "variables.scss" to "main.scss" file: `@use './variables.scss' as *;`

#### Testing

You can now start using Sass in your project. As a test, create an empty div with an h1 tag saying "Hello World" in the `App.jsx` file.

 ```
 function App() {
   return (
     <div>
       <h1>Hello World</h1>
     </div>
   );
 }

 export default App;
 ```
Example of the variables.scss file:

```
// Declare SCSS variables
$primary-color: #333;
$secondary-color: #ccc;
$accent: #ffa500;
$font-stack: Helvetica, sans-serif;

// Add more variables as needed
```
Import "variables.scss" to "main.scss"
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
To use this style, import it into `App.jsx` by adding `import './assets/styles/main.scss'`.

 ```
 import './assets/styles/main.scss';

 function App() {
   return (
     <div>
       <h1>Hello World</h1>
     </div>
   );
 }

 export default App;
 ```
