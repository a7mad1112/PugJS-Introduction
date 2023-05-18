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
- [Pug.js Attributes](#pugjs-attributes)
- [Include in Pug.js](#include-in-pugjs)
- [Code in Pug.js](#code-in-pugjs)
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

## Pug.js Attributes
In Pug.js, you have the flexibility to add attributes to HTML elements easily.
You can add a single attribute, such as id or class, by using '#' or '.' respectively after the element name.
For example:
```
p.desc This is a paragraph with the class name "desc".
p#id-1 This is a paragraph with the id "id-1".
```
When compiled, the code will generate the following output:
```
<p class="desc">This is a paragraph with the class name "desc".</p>
<p id="id-1">This is a paragraph with the id "id-1".</p>
```
In certain cases, you may want to add multiple attributes to an element.
You can achieve this by using parentheses '( )' and separating the attributes with commas or spaces.
For example:
```
a(class='link' id='id-1' href='https://www.example.com/') Link
// You can also separate attributes by commas
a(class='link', id='id-2', href='https://www.example.com/') Link
```
The compiled code will result in the following output:
```
<a class="link" id="id-1" href="https://www.example.com/">Link</a>
<!-- You can also separate attributes by commas-->
<a class="link" id="id-2" href="https://www.example.com/">Link</a>
```

## Include in Pug.js
In certain cases, you may encounter situations where you need to reuse a block of code from one file in another file.
For instance, consider a website with multiple pages like index, about, and contact, where the header content remains the same across all pages.
Writing the header code in each file would be redundant and require modifications in multiple places if changes are made.

However, in Pug.js, you can use the 'include' keyword to include the content from a separate file.
This allows you to write the header code in one file and include it in other files.
Any modifications made to the included file will automatically reflect in all the files that include it.

Here's an example of how to use the include keyword:
header.pug file:
```
header
  h1 My Website
  nav
    // Navigation links...
```
index.pug file:
```
doctype html
html
  body
    include header.pug
    h1 Welcome to the Index Page
    // Rest of your code...
```
The compiled code for 'index.pug' would be:
```
<!DOCTYPE html>
<html>
  <body>
    <header>
      <h1>My Website</h1>
      <nav>
        <!-- Navigation links...-->
      </nav>
    </header>
    <h1>Welcome to the Index Page</h1>
    <!-- Rest of your code...-->
  </body>
</html>
```

## Code in Pug.js
Pug.js allows you to write inline JavaScript code within your templates.
There are three types of code you can use: UnBuffered Code, Buffered Code, and Unescaped Buffered Code.

- UnBuffered Code:
UnBuffered code starts with a hyphen '-'. It does not directly add anything to the output.
UnBuffered code is typically used for tasks like loops or declaring variables using keywords such as var, let, or const.
The result of unBuffered code does not directly affect the generated output.
Example:
```
- var stop = 3
ul
  - for (var i = 0; i < stop; i++)
    li Item
```
The compiled code would be:
```
<ul>
  <li>Item</li>
  <li>Item</li>
  <li>Item</li>
</ul>
```

- Buffered Code:
Buffered code starts with an equal sign '='. It evaluates the JavaScript expression and outputs the result into the template.
Example:
```
- const name = "Ahmed Alawneh"
p= '<span>' + name + '</span>'
```
The compiled code would be:
```
<p>&lt;span&gt;Ahmed Alawneh&lt;/span&gt;</p>
```

- Unescaped Buffered Code:
Unescaped buffered code starts with an exclamation mark and equal sign '!='.
It evaluates the JavaScript expression and outputs the result without performing any HTML escaping.
This is useful when you want to include specific elements or raw HTML content.
Example:
```
- const name = "Ahmed Alawneh"
p!= '<span>' + name + '</span>'
```
The compiled code would be:
```
<p><span>Ahmed Alawneh</span></p>
```
By using these different types of code in Pug.js, you can leverage the power of JavaScript within your templates and generate dynamic content.