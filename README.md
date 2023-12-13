### React History
- developed by Facebook 
- kept Open Source 
- cross platform support 
- React in lead for 6 years 
- most popular library 
- Part of MERN stack 
- react updates on same html, using DOM 
- react using virtual DOM 
    - JS object 
    ex of how it looks:
        const VirtualDom = {
            key: value,
            key: value
        }
- updating virtual DOM is faster than updating real DOM 
- When something changes in a react component, we get a new react element, react will 
compare the parent and children of the current and previous component 
- WIll update the real DOM to keep in sync with the virtual DOM 
- Prereq: JavaScript 
 
### Components 
- small piece of a user interface 
- lets you split the UI into independent and reusable performance 
- helps you build a full fledge interactive website UI 
- Wy import React?
    - We need to import React to be able to use the entirety of this library 
- then we use a JS class to make the react component that extends the react component 
- then we use the render method to describe what should be displayed and what it should look like 
- import React from 'react'
- then arrow function 
- ex:
    - const Example = () {
        return <div>Hello World!</div>
    }
    - this called jsx
    - describes what the UI should look like 
    - produces react elements 
    

### Ex code:

import { useState, useEffect } from 'react';
import './App.css';

const App = () => {

  const [counter, setCounter] = useState(0); //hook

  useEffect(() => {
    //counter = 100; //never modify/ mutate state directly, do not do this 
    //correctway
    alert("You've changed the counter to " + counter);
  }, [counter]);

  return (
    <div className="App">
      <button onClick={() => setCounter((prevCount) => prevCount - 1)}>-</button>
      <h1>{counter}</h1>
      <button onClick={() => setCounter((prevCount) => prevCount + 1)}>+</button>
    </div>
  );
}

export default App;
