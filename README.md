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
- [Interpolation](#interpolation)
- [Unescaped Interpolation](#unescaped-interpolation)
- [Tag Interpolation](#tag-interpolation)
- [Mixins](#mixins)
</p>
</details>

## Getting Started
Getting Started with Pug JS - Step by Step Guide
### Installation
- Ensure that you have Node.js installed on your system.
  You can download and install Node.js from the official website [nodejs](https://nodejs.org).
- Open your terminal or command prompt and verify that Node.js is installed by running the command: <strong>'node -v'</strong>
- Once Node.js is successfully installed, you can install Pug globally by running the command: <strong>'npm install -g pug'</strong>

### Create a Project Directory
- Create a new directory for your Pug project. 
  You can choose any suitable name for your project.
- Open your terminal or command prompt and navigate to the project directory using the <strong>'cd'</strong> command.

### Initialize a Node.js Project
- In the project directory, initialize a new Node.js project by running the command: <strong>'npm init'</strong>
- Follow the prompts to provide the necessary information for your project, or you can use the default values by pressing Enter for each prompt.

### Install Pug as a Project Dependency
- With your Node.js project initialized, you can install Pug as a project dependency by running the command: <strong>'npm install pug'</strong>

### Create a Pug Template
- Inside your project directory, create a new file with a .pug extension. 
  This file will serve as your Pug template.
- Open the Pug template file in a text editor and start writing Pug code.

### Write Pug Code
- Pug uses indentation-based syntax instead of HTML tags.
- Write Pug code to define the structure, content, and logic of your HTML template.

### Compile Pug to HTML
- In your terminal or command prompt, navigate to the project directory.
- Run the command to compile your Pug template to HTML: <strong>'pug &lt;template-file&gt; -o &lt;output-directory&gt;'</strong>
- Replace <strong>'&lt;template-file&gt;'</strong> with the path of your Pug template file.
- Replace <strong>'&lt;output-directory&gt;'</strong> with the path to the directory where you want the compiled HTML file to be generated.


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

To enable watching of Pug.js files, you can use the <strong>'-w'</strong> or <strong>'--watch-'</strong> flag when running the Pug compiler command. Here's an example:
```
pug -w <template-file>.pug -o <output-directory>
```
Also you can use the <strong>'-p'</strong> or <strong>'--pretty'</strong> to get a clean code.
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
You can add a single attribute, such as id or class, by using <strong>'#'</strong>or <strong>'.'</strong> respectively after the element name.
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
You can achieve this by using parentheses <strong>'( )'</strong> and separating the attributes with commas or spaces.
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

However, in Pug.js, you can use the <strong>'include'</strong> keyword to include the content from a separate file.
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
The compiled code for <strong>'index.pug'</strong> would be:
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
UnBuffered code starts with a hyphen <strong>'-'</strong>. 
It does not directly add anything to the output.
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
Buffered code starts with an equal sign <strong>'='</strong>
. It evaluates the JavaScript expression and outputs the result into the template.
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
Unescaped buffered code starts with an exclamation mark and equal sign <strong>'!='</strong>.
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

## Interpolation
In Pug.js, interpolation is a way to dynamically insert JavaScript expressions and variables into the HTML output.
It is denoted by the <strong>'#{...}'</strong> syntax and allows for the generation of dynamic content based on variable values or expressions.
Example:
```
- var author = "LEVI"
p Written with love by #{author}
```
The compiled code would be:
```
<p>Written with love by LEVI</p>
```
You can also leverage the power of JavaScript within interpolation.
Example:
```
- var msg = 'hello world!'
p The message is #{msg.toUpperCase()}
```
The compiled code would be:
```
<p>The message is HELLO WORLD!</p>
```
Note:
If you want to include the #{} itself, you can include it inside the interpolation or escape it.
Example:
```
p Escaping works with \#{interpolation}
p This works too #{'#{interpolation}'}
```
The compiled code would be:
```
<p>Escaping works with #{interpolation}</p>
<p>This works too '#{interpolation}</p>
```
However, if you add markup inside the interpolation, it will be escaped.
Example:
```
- var msg = '<strong>Hello World!</strong>'
h2 The message is #{msg}
```
The compiled code would be:
```
<h2>The message is &lt;strong&gt;Hello World!&lt;/strong&gt;</h2>
```
To include markup as intended and have elements nested inside elements, refer to the next section.

## Unescaped Interpolation
Unescaped interpolation, denoted by <strong>'!{...}'</strong>, allows HTML characters to be interpreted as markup in the resulting string.
Example:
```
- var msg = '<strong>Hello World!</strong>'
h2 The message is !{msg}
```
The compiled code would be:
```
<h2>The message is <strong>Hello World!</strong></h2>
```
Unescaped interpolation is useful when you want to include HTML markup within the interpolated expression without it being escaped.
It allows the markup to be rendered as intended in the final output.

## Tag Interpolation
Tag interpolation is a technique used in PugJS to dynamically insert values into a predefined template using placeholders. It provides a convenient way to generate dynamic content or apply conditional styling to elements. In PugJS, tag interpolation is achieved using the #[tag=value] syntax.
Example:
```
- var name = "Levi"
p #[span.name] Hello, #{name}!
```
The compiled code would be:
```
<p><span class="name">Hello, Levi!</span></p>
```

In the above example, we define a variable name with the value "Levi".
By using tag interpolation <strong>'#[span.name]'</strong>, we can dynamically insert the value of name into the class attribute of the &lt;span&gt; tag. As a result, the generated HTML will have the class attribute set as <strong>'name'</strong>, and the text content of the &lt;span&gt; tag will be "Hello, Levi!".

Tag interpolation allows you to create flexible templates by injecting values into specific tags or attributes based on variables or expressions. This can greatly enhance the dynamic nature of your templates and simplify the process of generating dynamic content.

## Mixins
Mixins are a powerful feature in PugJS that allow you to create reusable blocks of code, 
which can be called and included in other templates. 
They provide a convenient way to avoid code duplication and promote code reuse.

To define a mixin in PugJS, you can use the <strong>'mixins'</strong> keyword, followed by the mixin name and any arguments it may accept. 
Here's an example:
```
mixin greeting(name)
  p Hello, #{name}!
```

In the above example, we define a mixin called <strong>'greeting'</strong>'greeting' that accepts one argument <strong>'name'</strong>.
Inside the mixin block, we can use the <strong>'name'</strong> variable to dynamically insert the name value into the output.
This allows us to create a reusable greeting message that can be customized based on the provided name.

To use the defined mixin, you can call it by its name followed by parentheses, passing in the required arguments.
Here's an example of using the greeting mixin:
```
+greeting('Ahmed')
+greeting('LEVI')
```
The compiled code would be:
```
<p>Hello, Ahmed!</p>
<p>Hello, LEVI!</p>
```
