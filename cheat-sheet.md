# Arrow function

```javascript
function callMe(name) {
     console.log(name);
}
```

Which you could also write as:

```javascript
const callMe = function(name) {
    console.log(name);
}

```
becomes in Arrow Function:

```javascript
const callMe = (name) => {
    console.log(name);
}
```
<br>

# Class

```javascript
class Human {
    species = 'human';
}

class Person extends Human {
    name = 'Max';
    printMyName = () => {
        console.log(this.name);
    }
}
const person = new Person();
```
<br>

# Spread & Rest Operator

The spread operator allows you to pull elements out of an array (`=>` split the array into a list of its elements) or pull the properties out of an object. Here are two examples:
```javascript
const oldArray = [1, 2, 3];
const newArray = [...oldArray, 4, 5]; // This now is [1, 2, 3, 4, 5];
```
Here's the spread operator used on an object:
```javascript
const oldObject = {
    name: 'Max'
};
const newObject = {
    ...oldObject,
    age: 28
};
```

newObject would then be:
```javascript
{
    name: 'Max',
    age: 28
}
```
<br>

# Components

## 1. Functional components
```javascript
const cmp = () => { 
    return <div>some JSX</div> 
}
```

## 2. Class-based components

```javascript
import React, { Component } from 'react';

class Cmp extends Component { 
    render () {
        return <div>some JSX</div> 
    } 
}
```
<br>

# Props and state

## 1. Props
In All posts component:
```javascript
const posts = () => {
    return (
        <div>
            <Post title="My first Post" />
        </div>
    );
}
```
In post component:
```javascript
const post = (props) => {
    return (
        <div>
            <h1>{props.title}</h1>
        </div>
    );
}
```

## 1. State
```javascript
class NewPost extends Component { // state can only be accessed in class-based components!
    state = {
        counter: 1
    };
    render () { // Needs to be implemented in class-based components! Needs to return some JSX!
        return (
            <div>{this.state.counter}</div>
        );
    }
}
```

state example:

```javascript
 state = {
    persons: [
      { name: 'Milon', Age: 21 },
      { name: 'Nazmul', Age: 21 },
      { name: 'fakrul', Age: 23  },
    ],
    otherState: 'Some other state'
  }

  switchNameHandler = () => {
    //DON'T DO THIS this.state.persons[0].name = 'Milon Mahato';
    this.setState({
      persons: [
        { name: 'Milon Mahato', Age: 21 },
        { name: 'Nazmul Hassan', Age: 21 },
        { name: 'Fakrul Islam', Age: 23  },
      ]
    })
  }

```