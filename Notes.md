### Creating Elements and JSX

Create Element Syntax:
```
React.createElement( /* type */, /* props */, /* content */ );
```
- In react the in the process of rendering an element - what to render is different from actually rendering it.
Let's break down what each item can be:

 - "type" – either a string or a React Component
    This can be a string of any existing HTML element (e.g. 'p', 'span', or 'header') or you could pass a React component (we'll be creating components with JSX, in just a moment).

 - props – either null or an object
    This is an object of HTML attributes and custom data about the element.

 - content – null, a string, a React Element, or a React Component
    Anything that you pass here will be the content of the rendered element. This can include plain text, JavaScript code, other React elements, etc.

#### Nested Elements
```
import React from 'react'
import ReactDOM from 'react-dom'

const element = React.createElement('ol', null,
  React.createElement('li', null , 'Michael'),
  React.createElement('li', null , 'Anuja'),
  React.createElement('li', null , 'Anu')
)

ReactDOM.render(
  element,
  getElementByID('root')
  )
```


React lets you use JavaScript Arrays:

```
import React from 'react'
import ReactDOM from 'react-dom'

const people = [{name: Michael},
                {name: Anuja},
                {name: Anu}]

const element = React.createElement('ol', null,
  people.map((person, index) => (
    React.createElement('li', {key: index}, person.name)
  ))
)

ReactDOM.render(
  element,
  getElementByID('root')
  )
```

Creating the same list in JSX.

Any Javascript expression can be executed using {} braces.

JSX Returns One Root Element, Too
When writing JSX, keep in mind that it must only return a single element. This element may have any number of descendants, but there must be a single root element wrapping your overall JSX (typically a <div> or a <span>).

```
import React from 'react'
import ReactDOM from 'react-dom'

const people = [{name: Michael},
                {name: Anuja},
                {name: Anu}]

const element = <ol>
{people.map(person => (
  <li key={person.name}> {person.name} </li>
  ))}

ReactDOM.render(
  element,
  getElementByID('root')
  )
```

### Create React App
### Composing with Components
### Rendering UI Outro
### Introduction
### Pass Data with Props
### Functional Components
### Add State to a component
### Update State with setState
### Proptypes
### Controlled Components
### Lesson Summary
### Introduction
### componentDidMount Lifecycle Event
### Lesson Summary
### Introduction
### Dynamically Rendering pages
### The Browser Router Component
### The Link Component
### The Route component
### Finishing the Contact Form
### Lesson Summary
### Course Outro