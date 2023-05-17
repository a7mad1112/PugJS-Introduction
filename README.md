<h1 align="center">
  <img src="./Pug-Life-PNG-Picture.png" width="128">
  <br>
  PugJs Introduction
</h1>

<p>
  Pug.js is a high-performance template engine for Node.js and browsers, used to generate HTML markup efficiently. It offers a concise and expressive syntax, enabling developers to write clean and maintainable templates with features like conditionals, loops, and mixins. Pug.js promotes code reusability and simplifies the process of rendering dynamic content in web applications.
</p>

<details>
<summary>📖 Table of Contents</summary>
<p>

- [Getting Started](#getting-started)
  - [Installation](#installation)
  - [Create a Project Directory](#create-a-project-directory)
  - [Initialize a Node.js Project](#initialize-a-nodejs-project)
  - [Install Pug as a Project Dependency](#install-pug-as-a-project-dependency)
  - [Create a Pug Template](#create-a-pug-template)
  - [Write Pug Code](#write-pug-code)
  - [Compile Pug to HTML](#compile-pug-to-html)
  - [View the Compiled HTML](#view-the-compiled-html)
  - [Make Changes and Repeat](#make-changes-and-repeat)
- [Watching PugJS Files](#watching-pugjs-files)
- [Understanding the Syntax of Pug.js](#understanding-the-syntax-of-pugjs)
</p>
</details>


## Getting Started
Getting Started with Pug JS - Step by Step Guide
### Installation
- Ensure that you have Node.js installed on your system.
  You can download and install Node.js from the official website [nodejs](https://nodejs.org).
- Open your terminal or command prompt and verify that Node.js is installed by running the command: 'node -v'
- Once Node.js is successfully installed, you can install Pug globally by running the command: 'npm install -g pug'

### Create a Project Directory
- Create a new directory for your Pug project. 
  You can choose any suitable name for your project.
- Open your terminal or command prompt and navigate to the project directory using the 'cd' command.

### Initialize a Node.js Project
- In the project directory, initialize a new Node.js project by running the command: 'npm init'
- Follow the prompts to provide the necessary information for your project, or you can use the default values by pressing Enter for each prompt.

### Install Pug as a Project Dependency
- With your Node.js project initialized, you can install Pug as a project dependency by running the command: 'npm install pug'

### Create a Pug Template
- Inside your project directory, create a new file with a .pug extension. 
  This file will serve as your Pug template.
- Open the Pug template file in a text editor and start writing Pug code.

### Write Pug Code
- Pug uses indentation-based syntax instead of HTML tags.
- Write Pug code to define the structure, content, and logic of your HTML template.

### Compile Pug to HTML
- In your terminal or command prompt, navigate to the project directory.
- Run the command to compile your Pug template to HTML: 'pug &lt;template-file&gt; -o &lt;output-directory&gt;'
- Replace '&lt;template-file&gt;' with the path of your Pug template file.
- Replace '&lt;output-directory&gt;' with the path to the directory where you want the compiled HTML file to be generated.
- 

### View the Compiled HTML
- Open the compiled HTML file in a web browser to see the result of your Pug template.
### Make Changes and Repeat
- Edit your Pug template file to make any changes to the HTML structure or content.
- Run the Pug compiler again to generate the updated HTML output.
- Refresh the web browser to view the changes.

Great job on getting started with Pug JS! &hearts;

## Watching PugJS Files
Watching Pug.js files refers to a process where the Pug.js compiler automatically monitors for changes in your Pug files and recompiles them into HTML whenever a modification is detected.
This allows you to see the updated output in real-time without manually running the compilation command each time.

To enable watching of Pug.js files, you can use the '-w' or '--watch' flag when running the Pug compiler command. Here's an example:
```
pug -w <template-file>.pug -o <output-directory>
```
Also you can use the '-p' or '--pretty' to get a clean code.
For Instance:
```
pug -w <template-file>.pug -o <output-directory>./ --pretty
```

## Understanding the Syntax of Pug.js
Pug.js utilizes indentation to define the structure of the markup.
Instead of using opening and closing tags, elements are nested under each other based on indentation levels. 
This approach reduces clutter and improves code readability. For example:
```
html
  head
    title My Pug Page
  body
    h1 Welcome to Pug.js
    p Pug.js is a fantastic template engine.
```
The compiled code:
```
<html>
  <head>
    <title>My Pug Page</title>
  </head>
  <body>
    <h1>Welcome to Pug.js</h1>
    <p>Pug.js is a fantastic template engine.</p>
  </body>
</html>
```