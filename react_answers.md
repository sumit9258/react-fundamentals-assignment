## Question 1: What is React, and why is it used for building user interfaces?

React is a JavaScript library developed by Facebook for building interactive user interfaces, especially for single-page applications. It enables developers to build reusable UI components that automatically update when data changes. React uses a virtual DOM, which helps improve performance by minimizing direct manipulation of the real DOM. This makes UI updates faster and more efficient. It also supports a component-based architecture, allowing code to be modular, easier to debug, and more maintainable. React follows a unidirectional data flow, which helps manage data logic cleanly. React can also be combined with other libraries like Redux or React Router to build complex front-end applications. For example, a `Button` component can be reused throughout an app with different props.

---

## Question 2: What is a React component, and what is the difference between a functional component and a class component?

A React component is a reusable piece of UI that returns JSX to describe how the interface should look. Components can be of two types: functional and class-based.

Functional components are JavaScript functions that return JSX. With the introduction of React Hooks like `useState` and `useEffect`, functional components can now manage state and side effects easily.

Class components are ES6 classes that extend `React.Component`. They use lifecycle methods like `componentDidMount` and manage state using `this.state` and `this.setState()`.

While both can achieve the same outcomes, functional components are now preferred due to simpler syntax, better performance, and more concise code. They also encourage the use of hooks, which makes state management more intuitive and powerful.

---

## Question 3: What is JSX, and how does it differ from regular HTML?

JSX (JavaScript XML) is a syntax extension for JavaScript used in React to describe UI components. It allows developers to write HTML-like code within JavaScript, making the code more readable and easier to visualize. JSX looks similar to HTML, but it has important differences. For example, instead of `class`, JSX uses `className` because `class` is a reserved keyword in JavaScript. Also, attributes are written in camelCase like `onClick` or `tabIndex`.

Unlike HTML, JSX can include JavaScript expressions inside curly braces `{}`, making it dynamic and powerful. These expressions allow data binding and conditional rendering directly within the UI code.

Example:

```jsx
<h1 className="title">Hello, {userName}!</h1>

---


## Question 4: What are props in React, and how do you pass data from a parent component to a child component?

Props, short for “properties,” are a way of passing data from a parent component to a child component in React. They help make components dynamic and reusable by allowing different values to be sent into the same component structure. Props are read-only, which means a child component cannot modify them. They are passed as attributes in JSX. This approach helps maintain unidirectional data flow in React, making it easier to manage and debug data handling in an application.

Example:

```jsx
function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}

function App() {
  return <Greeting name="Alice" />;
}


---



## Question 5: What is the useState Hook, and how do you use it to manage state in a functional component?

The `useState` Hook is a built-in Hook in React that allows functional components to have their own state. Earlier, state management was only possible in class components, but with Hooks, functional components became more powerful and easier to use. `useState` takes the initial state value as an argument and returns an array with two elements: the current state and a function to update it.

Here’s a basic example:

```jsx
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click me</button>
    </div>
  );
}
