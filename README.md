# Frontend Interview Hotlist

## Summary
These questions and answers provide a comprehensive overview of various topics related to software development, covering areas such as JavaScript, React, HTML/CSS, SCSS, JSON, decoupled Drupal, Docker, Git, Agile methodologies, and more.

### Junior Software Developer (1-3 years)

#### **Git:**
   - What is Git and what are its key features?
> **Answer:** Git is a distributed version control system that allows developers to track changes to source code over time. Its key features include branching, merging, and remote collaboration.

   - How do you perform a merge and resolve conflicts?
> **Answer:** You can merge branches in Git using the `git merge` command. If there are conflicts, Git will prompt you to resolve them manually.

For example:

     ```bash
     git merge feature-branch
     ```

#### **HTML & CSS:**
   - What is the difference between inline, internal, and external CSS?
> **Answer:** Inline CSS is applied directly to an HTML element using the `style` attribute. Internal CSS is defined within a `<style>` tag in the `<head>` section of an HTML document. External CSS is defined in a separate `.css` file and linked to an HTML document using the `<link>` tag.

   - Explain the concept of CSS box model.
> **Answer:** The CSS box model consists of content, padding, border, and margin. The content area is where the text and images are placed. Padding is the space between the content and the border. Border is the line that surrounds the padding and content. Margin is the space outside the border.

#### **SCSS:**
   - What is SCSS and how does it differ from CSS?
> **Answer:** SCSS (Sassy CSS) is a preprocessor scripting language that is interpreted or compiled into Cascading Style Sheets (CSS). It adds features like variables, nesting, mixins, and functions, which make CSS more maintainable and scalable.

   - How do you use variables in SCSS?
> **Answer:** You can define variables using the `$` symbol in SCSS.

For example:

     ```scss
     $primary-color: #3498db;
     $font-size: 16px;

     body {
       color: $primary-color;
       font-size: $font-size;
     }
     ```

#### **JSON:**
   - What is JSON and how is it used in web development?
> **Answer:** JSON (JavaScript Object Notation) is a lightweight data interchange format that is easy for humans to read and write and easy for machines to parse and generate. It is commonly used in web development to send data from a server to a client or vice versa.

   - How do you parse JSON data in JavaScript?
> **Answer:** You can parse JSON data using the `JSON.parse()` method in JavaScript.
For example:

     ```javascript
     const jsonString = '{"name": "John", "age": 30}';
     const obj = JSON.parse(jsonString);
     console.log(obj.name); // Output: John
     ```

#### **JavaScript Basics:**
   - What is an event loop in JavaScript?
> **Answer:** An event loop is a mechanism in JavaScript that handles asynchronous operations. It allows JavaScript to perform non-blocking I/O operations, such as reading from a file or making a network request, without blocking the execution of the main thread.

   - Explain the difference between synchronous and asynchronous JavaScript.
> **Answer:** Synchronous code is executed sequentially, meaning that each line must complete before the next line is executed. Asynchronous code, on the other hand, allows certain tasks to run in the background without blocking the main execution thread.

#### **React:**
   - What is the purpose of React and why is it popular?
> **Answer:** React is a JavaScript library for building user interfaces, particularly single-page applications. It is popular because it allows developers to build complex UIs in a declarative and efficient way.

   - How do you handle state in a functional component using hooks?
> **Answer:** You can use the `useState` hook to manage state in functional components.

For example:

     ```jsx
     import React, { useState } from 'react';

     function Counter() {
       const [count, setCount] = useState(0);

       return (
         <div>
           <p>You clicked {count} times</p>
           <button onClick={() => setCount(count + 1)}>
             Click me
           </button>
         </div>
       );
     }
     ```

#### **Decoupled Drupal:**
   - What is decoupled Drupal, and why would you use it?
> **Answer:** Decoupled Drupal allows you to build a frontend application using a different technology stack (e.g., React, Angular) than the backend. This enables you to use the best tools and technologies for each part of the application, leading to improved performance and flexibility.

   - How do you integrate a React app with Drupal?
   - **Answer:** You can integrate a React app with Drupal by using RESTful APIs provided by Drupal. For example, you can create endpoints to fetch content from Drupal and use them in your React app.

#### **Docker:**
   - What is Docker and why is it useful in development?
> **Answer:** Docker is a platform that allows developers to create, deploy, and run applications in lightweight, portable containers. It simplifies the development and deployment process by ensuring that applications run consistently across different environments.

   - How do you create a Docker image for a Node.js application?
> **Answer:** You can create a Docker image for a Node.js application by defining a `Dockerfile`.

For example:

     ```Dockerfile
     FROM node:14
     WORKDIR /app
     COPY package.json .
     RUN npm install
     COPY . .
     EXPOSE 3000
     CMD ["node", "server.js"]
     ```
#### **Agile:**
   - What is Agile, and what are its key principles?
> **Answer:** Agile is a project management methodology that emphasizes iterative development, collaboration, and customer satisfaction. Key principles include working software, customer collaboration, and responding to change.

   - How do you manage a sprint in an Agile project?
> **Answer:** In an Agile project, a sprint is a time-boxed period (usually 2-4 weeks) during which a set of features is developed. You can manage a sprint by planning tasks, daily stand-ups, and sprint reviews.
---

### Mid-Level Software Developer (3-5 years)

#### **Git:**
   - What are the best practices for branching and merging in Git?
> **Answer:** Best practices include using a branching strategy like Git Flow or Feature Branching. Merge conflicts should be resolved by discussing changes and finding a common solution.

   - How do you use Git for code review and collaboration?
> **Answer:** Git provides tools for code review, such as pull requests, which allow other developers to review and comment on your code. Collaboration is facilitated by using Git's branching and merging capabilities.

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
