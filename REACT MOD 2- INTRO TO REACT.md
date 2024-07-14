<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Module 4</title>
    <style>
        body {
            background-color: black;
            color: white;
        }
        h1, h2, h3, h4, h5, h6 {
            color: white;
        }
    </style>
</head>
<body>
## Module 2: Introduction to ReactJS

### What is React JS?
React JS is a JavaScript library for building user interfaces. It is maintained by Facebook and a community of individual developers and companies. React can be used as a base in the development of single-page applications (SPAs) or mobile applications.

#### Example
```javascript
import React from 'react';
import ReactDOM from 'react-dom';

function App() {
  return (
    <div>
      <h1>Hello, World!</h1>
    </div>
  );
}

ReactDOM.render(<App />, document.getElementById('root'));
```

### Why use React JS?
React JS is widely used because of its simplicity, flexibility, and performance. It allows developers to create large web applications that can change data, without reloading the page. Its component-based architecture promotes reusability and easy maintenance.

#### Benefits
- **Component-Based Architecture**: Promotes code reusability and separation of concerns.
- **Virtual DOM**: Enhances performance by minimizing direct manipulation of the real DOM.
- **Unidirectional Data Flow**: Ensures data flows in a single direction, making the application easier to understand and debug.
- **Large Ecosystem**: Rich ecosystem with numerous libraries and tools for various needs.

### What is a Single Page Application (SPA)?
A Single Page Application (SPA) is a web application that loads a single HTML page and dynamically updates the page as the user interacts with the app. SPAs use AJAX and HTML5 to create fluid and responsive web apps, without constant page reloads.

#### Example
```javascript
import React, { useState } from 'react';

function SPA() {
  const [page, setPage] = useState('home');

  const renderPage = () => {
    switch (page) {
      case 'home':
        return <div>Home Page</div>;
      case 'about':
        return <div>About Page</div>;
      default:
        return <div>Home Page</div>;
    }
  };

  return (
    <div>
      <nav>
        <button onClick={() => setPage('home')}>Home</button>
        <button onClick={() => setPage('about')}>About</button>
      </nav>
      {renderPage()}
    </div>
  );
}

ReactDOM.render(<SPA />, document.getElementById('root'));
```

### Why SPA?
- **Faster Load Time**: Only the necessary components are loaded initially, and other parts are loaded dynamically.
- **Improved User Experience**: Provides a more fluid and seamless user experience, similar to a desktop application.
- **Reduced Server Load**: Fewer full-page reloads reduce the load on the server.

### React JS Version
React JS has undergone several updates since its release. The current stable version is React 18, which introduces concurrent rendering, automatic batching, and new hooks like `useId`.

#### Example (Using React 18)
```javascript
import React from 'react';
import ReactDOM from 'react-dom/client';

const root = ReactDOM.createRoot(document.getElementById('root'));

root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```

### React DOM
React DOM is the package that provides DOM-specific methods. It efficiently updates and renders components to the DOM.

#### Example
```javascript
import React from 'react';
import ReactDOM from 'react-dom';

function App() {
  return (
    <div>
      <h1>Hello, World!</h1>
    </div>
  );
}

ReactDOM.render(<App />, document.getElementById('root'));
```

### React Virtual DOM
The Virtual DOM is a concept where a virtual representation of the real DOM is kept in memory and synced with the real DOM by libraries like ReactDOM. This process is called reconciliation. It enhances performance by updating only the necessary parts of the DOM.

#### Example
```javascript
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

ReactDOM.render(<Counter />, document.getElementById('root'));
```

## Interview Questions and Answers

1. **What is React JS?**
   - **Answer:** React JS is a JavaScript library for building user interfaces, maintained by Facebook and a community of developers. It is used to build single-page applications and mobile apps.

2. **Why use React JS over other frameworks?**
   - **Answer:** React JS is simple, flexible, and performant. Its component-based architecture promotes reusability, and the Virtual DOM enhances performance. Additionally, React has a large ecosystem and a strong community.

3. **What is a Single Page Application (SPA) and why use it?**
   - **Answer:** An SPA loads a single HTML page and dynamically updates the page as the user interacts with the app. It provides faster load times, improved user experience, and reduced server load compared to traditional multi-page applications.

4. **What are the key features introduced in the latest React JS version?**
   - **Answer:** React 18 introduces concurrent rendering, automatic batching, new hooks like `useId`, and improvements to server-side rendering.

5. **What is the Virtual DOM and how does it improve performance?**
   - **Answer:** The Virtual DOM is a virtual representation of the real DOM kept in memory. It enhances performance by updating only the necessary parts of the DOM, reducing the number of direct manipulations of the real DOM.

6. **Explain the role of React DOM in a React application.**
   - **Answer:** React DOM provides DOM-specific methods that efficiently update and render components to the DOM. It handles the reconciliation process between the Virtual DOM and the real DOM.

These notes, interview questions, and code examples provide a comprehensive overview of ReactJS, its features, and its advantages for building modern web applications.