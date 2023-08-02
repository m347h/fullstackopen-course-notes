# fullstackopen-course-notes

notes from previous lesson: in Part 1 a) introduction to react (homework exercise), in sample solution, "reduce" was used in React, when they were summing up the total number of exercises, with an accumulator. in the const Total, we had to apply this "reduce" and use accumulator. 

```
const Total = ({parts}) => {
const totalExercises = parts.reduce((accumulator, currentObj) => accumulator + currentObj.exercises, 0);
return <p>total is {totalExercises}</p>
};
```

in this line below, App sends parts as a prop to Total. in Total, reduced method was called on parts. in our code, parts as the array contained multiple values,
such as name and exercises, which one do we want to accumulate? OBVS, its exercises!! so we specify by stating: currentObj.exercises. Now, about the 0, so u bascially start from 0. if u specify another num like 100, then the {totalExercises} will be +100 more than what we should've had.  

```
const totalExercises = parts.reduce((accumulator, currentObj) => accumulator + currentObj.exercises, 0);

```
remeber that it was in App, that we defined teh array and the parts. 

```
const Total = ({ parts }) => {
  const totalExercises = parts.reduce((accumulator, currentObj) => accumulator + currentObj.exercises, 0);

  return <p>Number of exercises {totalExercises}</p>;
};


const App = () => {
  const course = {
    name: 'Half Stack application development',
    parts: [
      {
        name: 'Fundamentals of React',
        exercises: 10
    },
      {
        name: 'Using props to pass data',
        exercises: 7
      },
      {
        name: 'State of a component',
        exercises: 14
      }
    ]

  };

  
```

Expand the following application by adding a button that can be clicked to display a random anecdote from the field of software engineering:

import { useState } from 'react';



```
function test() {
  console.log("notice the blank line before this function?");
}


const App = () => {
    const anecdotes = [
        'If it hurts, do it more often.',
        'Adding manpower to a late software project makes it later!',
       

```
