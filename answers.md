# React Review 3

### 1. Import a Component

App.jsx

```jsx

import Gallery from './components/Gallery.jsx'

```

### 2. Object Destructuring

```jsx
const props = {
  name: 'English Breakfast',
  temperature: 99,
  type: 'Black Tea',
  origin: 'India',
  steepTime: 3, // in minutes
  caffeineContent: 40, // in mg per serving
  flavorNotes: ['Malty', 'Robust'],
  isOrganic: false,
  packaging: 'Tea Bags',
  price: 5.99, // in USD
  stockQuantity: 100,
  rating: 4.5, // out of 5
};

// Write your code here

const {name, packaging, temperature} = props;


```

### 3. State in React

State is a React object and contains data about a component. If useState is being used, React will update the browser if the component's state changes. 

### 4. Using state in React

```js

import { useState } from 'react'

function Tea (props) {
  const[isBrewing, setIsBrewing] = useState(true);
}
```

### 5. Connect the handler

There is an unconnected handler called `checkTime` in the `Tea` component. Connect it to an
appropriate element inside the component.

```jsx
import { useState } from "react";

function Tea(props) {
  const checkTime = () => { props.steepTime > props.startTime ? alert("TEA IS DONE!"); }

  return <>
    <h1>Tea Time</h1>
    <button onClick={checkTime}>Check if tea is ready</button>
  </>
}
```
