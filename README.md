# Frontend Interview Hotlist

## Summary
These questions and answers provide a quick screening of various topics related to software development on Frontend, covering areas such as Git, JSON, Javascript, React, Vite, Unit testing and more.

### Junior Software Developer (1-3 years)

#### **Git:**
   - What is Git and what are its key features?
> **Answer:** Git is a distributed version control system that allows developers to track changes to source code over time. Its key features include branching, merging, and remote collaboration.

   - What is a branch in Git, and how do you create one?
> **Answer:** A branch is a separate line of development in a repository. You can create a branch using `git branch <branch-name>`

   - How do you use `pull requests`?
> **Answer:** Platforms like Github/Gitlab/Bitbucket provides tools for code review, such as `pull requests`, which allow other developers to review and comment on your code.

#### **JSON:**
   - What is JSON and how is it used in web development?
> **Answer:** JSON (JavaScript Object Notation) is a lightweight data interchange format that is easy for humans to read and write and easy for machines to parse and generate. It is commonly used in web development to send data from a server to a client or vice versa.

   - What is the difference between the structures of a JSON object and an array?
> **Answer:** A JSON object is a collection of key-value pairs, while a JSON array is a collection/list of values. (3years)

   - In JSON, what are two common ways you can reference a property in a nested object?

> **Answer:** Dot Notation `jsonObj.address.street`, or Bracket Notation `jsonObj["address"]["street"]`

#### **JavaScript Basics:**

   - List 3-4 of the common Javascript Data Types
> **Answer:** Boolean, Null, Undefined, Number, String, Symbol, Array, Object

   - What is a closure in JavaScript?
> **Answer:** A closure is a combination of functions enclosed together. The inner functions have access of the other functions variables.

   - What is var, let, and const? What are their differences?
> **Answer:** `var`, `let`, and `const` are three different keywords used to declare variables. The main differences between them are:

Scope :

   - `var`: Function scope, meaning the variable is accessible throughout the function it's declared in.
   - `let` and `const`: Block scope, meaning the variable is only accessible within the block it's declared in (e.g., inside an if statement or a loop).

and Reassignment : 

   - `var` and `let`: Variables can be reassigned.
   - `const`: Variables cannot be reassigned.


   - What are some common ways in JavaScript for selecting elements?
> **Answer:**

```JS
getElementsbyClassName()
getElementByName()
getElementsByTagName()
querySelector()"
```

   - Explain the difference between synchronous and asynchronous JavaScript.
> **Answer:** `Synchronous` code is executed sequentially, meaning that each line must complete before the next line is executed. `Asynchronous` code, on the other hand, allows certain tasks to run in the background without blocking the main execution thread.

#### **React:**

   - What’s the virtual DOM?
> **Answer:** The virtual DOM is a copy of the website's UI stored in memory. When changes are made, it compares the changes and only updates the parts that are necessary, making it very efficient.

   - What is the difference between state and props in React?
> **Answer:** state and props are two types of data that can be used to store and manage information in a component. State is used for data that changes within a component, while props is used for data that is passed from a parent component to a child component.

   - What are React Hooks? 
> **Answer:** Hooks are functions that let us hook into React state and lifecycle features from a functional component. React Hooks cannot be used in class components. They let us write components without class.

   - What is the purpose of the key prop in React?
> **Answer:** The key prop helps React identify which components have changed, so it can efficiently update the DOM.

---

### Mid-Level Software Developer (3-5 years)

#### **Git:**
   - Can you explain the concept of rebasing and when you would use it instead of merging??
> **Answer:** `Rebasing` rewrites commit history to make it look like changes were made on top of another branch. While `Merging` combines changes from two branches into a new commit.


#### **HTML & CSS:**
   - What are the different ways to center an element in CSS?
> **Answer:** You can center an element using various methods such as `margin: auto`, `text-align: center`, `flexbox`, or `grid`.

   - Explain the concept of CSS flexbox and grid.
> **Answer:** Flexbox is a one-dimensional layout model that allows you to align and distribute space between items in a container, even when their size is unknown or dynamic. Grid is a two-dimensional layout model that allows you to create complex layouts by defining rows and columns.

#### **SCSS:**
   - How do you use mixins and functions in SCSS?
> **Answer:** Mixins allow you to define reusable styles, and functions allow you to perform calculations and return values. For example:

     ```scss
     @mixin border-radius($radius) {
       -webkit-border-radius: $radius;
          -moz-border-radius: $radius;
           -ms-border-radius: $radius;
               border-radius: $radius;
     }

     @function multiply($a, $b) {
       @return $a * $b;
     }

     .box {
       @include border-radius(10px);
       width: multiply(5, 10);
     }
     ```

#### **JSON:**
   - How do you handle nested JSON data in JavaScript?
> **Answer:** You can handle nested JSON data by recursively accessing the properties. For example:

     ```javascript
     const jsonData = {
       "user": {
         "name": "John",
         "age": 30,
         "address": {
           "city": "New York",
           "zip": "10001"
         }
       }
     };

     console.log(jsonData.user.address.city); // Output: New York
     ```

   - What is the difference between JSON and XML?
> **Answer:** JSON is a lightweight data interchange format that is easy for machines to parse and generate. XML, on the other hand, is a markup language that is designed to be human-readable and extensible.


#### **JavaScript Advanced:**
   - What is the difference between call, apply, and bind?
> **Answer:** `call`, `apply`, and `bind` are methods that allow you to set the `this` context for a function. `call` takes arguments as individual parameters, `apply` takes them as an array, and `bind` returns a new function with the specified `this` context.

   - Explain how closures work in JavaScript.
> **Answer:** A closure is a function that has access to its own scope, the outer function’s scope, and the global scope. Closures allow you to maintain state between function calls.

#### **React:**
   - How do you handle side effects in React components?
> **Answer:** You can handle side effects using the `useEffect` hook in functional components. For example:
     ```jsx
     import React, { useEffect } from 'react';

     function MyComponent() {
       useEffect(() => {
         console.log('Component did mount or update');
         return () => {
           console.log('Component will unmount');
         };
       }, [dependency]);

       return <div>My Component</div>;
     }
     ```

   - What is the purpose of higher-order components (HOCs)?
> **Answer:** HOCs are functions that take a component and return a new component with additional functionality. They are used to share functionality between components without duplicating code.

#### **Decoupled Drupal:**
   - How do you handle authentication and state management in a decoupled Drupal setup?
> **Answer:** You can handle authentication by using Drupal's RESTful API or a token-based system. For state management, you can use a state management library like Redux in your React app.

   - What are the benefits of using RESTful APIs in a decoupled architecture?
> **Answer:** RESTful APIs provide a standardized way to access and manipulate data, making it easier to build decoupled architectures. They also enable better scalability and performance by allowing clients to request only the data they need.

#### **Docker:**
   - What is Docker Compose, and why is it useful?
> **Answer:** Docker Compose is a tool for defining and running multi-container Docker applications. It allows you to define the services, networks, and volumes in a YAML file and start all the services with a single command.

   - How do you manage multiple services in a Docker Compose file?
> **Answer:** You can define multiple services in a Docker Compose file, each with its own set of configurations.

For example:

     ```yaml
     version: '3'
     services:
       web:
         image: my-web-app
         ports:
           - "3000:3000"
       db:
         image: my-db-app
         volumes:
           - db-data:/var/lib/mysql

     volumes:
       db-data:
     ```

#### **Agile:**
   - How do you manage dependencies and risks in an Agile project?
> **Answer:** You can manage dependencies by creating a dependency graph and identifying critical paths. Risks can be identified through risk assessments and mitigation plans.

   - What are the key roles in an Agile team?
> **Answer:** Key roles include the Scrum Master, Product Owner, and Development Team. The Scrum Master facilitates the Agile process, the Product Owner prioritizes the product backlog, and the Development Team delivers the product increments.

#### **General Questions:**
    - What are some best practices you follow in your development process?
> **Answer:** Best practices include writing clean, maintainable code, performing code reviews, and using version control systems like Git.
    - How do you stay up-to-date with the latest trends and technologies in web development?
> **Answer:** Staying up-to-date involves following industry blogs, attending conferences, and participating in online communities and forums.

---

### Senior Software Developer (5+ years)

#### **JavaScript Advanced:**
   - What are Promises and async/await?
> **Answer:** Promises are objects that represent the eventual completion or failure of an asynchronous operation. async/await is a syntax sugar built on top of Promises, making asynchronous code look more synchronous.

   - Explain how to handle errors in JavaScript.
   - **Answer:** You can handle errors using try/catch blocks or by chaining `.catch()` methods with Promises.

#### **React:**
   - What is React Router, and how does it work?
> **Answer:** React Router is a library for handling routing in React applications. It allows you to define routes and navigate between different views.

   - What is the purpose of context in React?
> **Answer:** Context provides a way to pass data through the component tree without having to pass props down manually at every level.

#### **HTML & CSS:**
   - What are the different ways to optimize CSS performance?
   - **Answer:** Optimizing CSS performance includes minifying CSS, using CSS sprites, and avoiding unnecessary selectors.

   - Explain the concept of CSS Grid and how it differs from Flexbox.
> **Answer:** CSS Grid is a two-dimensional layout system that allows you to create complex layouts by defining rows and columns. It differs from Flexbox in that it is designed to handle two-dimensional layouts.

#### **SCSS:**
   - What is the difference between CSS and SCSS?
> **Answer:** SCSS (Syntactically Awesome Style Sheets) is a preprocessor for CSS that adds features like variables, mixins, and functions, making it more powerful and easier to maintain.

   - How do you use variables in SCSS?
> **Answer:** You can define variables in SCSS to store values that can be reused throughout the stylesheet.

For example:

     ```scss
     $primary-color: #3498db;

     .button {
       background-color: $primary-color;
     }
     ```

#### **JSON:**
   - How do you validate JSON data?
> **Answer:** You can validate JSON data using tools like JSON Schema or by manually checking the structure and values.

   - What is the difference between JSON and YAML?
   - **Answer:** JSON and YAML are both data serialization formats, but JSON is a subset of JavaScript and is more lightweight, while YAML is more human-readable and flexible.

#### **Decoupled Drupal:**
   - What is the role of a headless CMS in a decoupled architecture?
> **Answer:** A headless CMS, such as Drupal, provides an API for accessing content without rendering it on the server. This allows the frontend to be built using a different technology stack.

   - What are the benefits of using a headless CMS?
> **Answer:** Benefits include improved scalability, better performance, and the ability to use any frontend technology without being limited by the CMS's frontend.

#### **Docker:**
   - What is Kubernetes, and how does it work?
> **Answer:** Kubernetes is an open-source container orchestration platform that automates the deployment, scaling, and management of containerized applications.

   - How do you manage containerized applications in Kubernetes?
> **Answer:** You can manage containerized applications in Kubernetes by defining deployment configurations, services, and other resources. Kubernetes provides tools for scaling, rolling updates, and rolling back deployments.

#### **Git:**
   - What is a Git hook, and how can you use it?
> **Answer:** A Git hook is a script that runs automatically when a specific event occurs in the Git repository. You can use hooks to enforce code quality, run tests, or trigger other automated processes.

   - How do you manage large codebases with Git?
> **Answer:** Managing large codebases with Git involves using branching strategies like Git Flow, maintaining a clean commit history, and regularly merging changes.

#### **Agile:**
   - What is the role of a product owner in an Agile team?
> **Answer:** The product owner is responsible for defining the product vision, prioritizing the product backlog, and communicating with stakeholders.

   - What are the benefits of using Agile methodologies in software development?
> **Answer:** Benefits include improved flexibility, customer satisfaction, and the ability to deliver working software more quickly.

#### **General Questions:**
   - What are some advanced techniques you use in your development process?
> **Answer:** Advanced techniques include automated testing, continuous integration, and continuous deployment.
   - How do you handle large-scale projects with multiple stakeholders?
> **Answer:** Handling large-scale projects involves effective communication, project management, and stakeholder engagement. It also requires the ability to prioritize tasks and manage resources efficiently.
