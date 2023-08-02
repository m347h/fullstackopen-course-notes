# fullstackopen-course-notes

Firstly, we start with some notes from previous lesson's homework: in Part 1 a) introduction to react (homework exercise), in another github's sample solution, a method called "reduce" was used in React, which was applied when they were summing up the total number of exercises with the use of an accumulator. In the solution, we had to define a "const Total" handler, in which we had to apply this "reduce" and use accumulator. 

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
Now, remember that it was in App handler (const App), that we defined the array and the parts. To revise the code, see below.  

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

 # continue onto part 1 b) javascript 

javasript is a reminiscent, in terms of 1) name (obv!) and 2) syntax of JAVA, but core mechanisms, so different! 

let's talk about variable:

in JS, there are few ways to define variables.
```
const x = 1 
let y = 5

console.log(x,y)
y += 10  // y = y+ 10 = 5+ 10 = 15 
console.log(x,y)
// "1, 15" are printed 
y = 'sometext'
console.log(x,y)
// "1, sometext" are printed 
x = 4 //causes an error, as const was defined 
 
```

It was shown that datatypes can be changed. 

let defines a normal variable, while const defines a constant. 

var can B used too. 

**Arrays**
An array and a couple of examples of its use:
```
const t = [1, -1, 3]
t.push(5)
```

```
console.log(t.length) // 4 is printed
console.log(t[1]) 
```
 // printing length and the element 
 
```
t.forEach(value => {
console.log(value)
})
```
outputes the numbers in the array: 1, -1, 3, 5, each to its **own line**

Okay, how to add an element to an existign array and create such a new array? 

```
const t = [1,2,4]
const t2 = t.concat(5) //creates new array 
console.log(t) //prints [1,2,4]
console.log(t2) //prints [1,2,4,5]

```

Many useful methods for arrays, one of them being **map** 


```
const t = [1,2,3]

const m1 = t.map(value => value*2)

console.log(m1) // this is where an arrayx2 [2,4,6] is printed

```

**Objects**
There are a few different ways of defining objects in JavaScript. One very common method is using object literals, which happens by listing its properties within braces:

you can have: 
```
const object1 = {
  name: 'Arto Hellas',
  age: 35,
  education: 'PhD',
}
```
or you have have ones within one, being like:
```
const object3 = {
  name: {
    first: 'Dan',
    last: 'Abramov',
  },
  grades: [2, 3, 5, 3],
  department: 'Stanford University',
}
```
you can the obv print: 

console.log(object1.name)

you get:  Arto Hellas

const fieldName = 'age' 

console.log(object1[fieldName]) //35 is printed. 

// you can then define such a const variable and then output it. 
```
Moreover, you can do a lot more things, you could add e.g. an address property. 

```
object1.address = 'Helsinki'
```

the latter addition has to be done using brackets bc when using dot notation, secret number isnt a valid peroprty name. 

```
object1['secret number'] = 12341
```


**Functions**

functiosn and arrow dunctions,

this is how u define it: 

```
const sum = (p1, p2) => {
console.log(p1)
console.log(p2)
return p1+p2
}
```


```
const result = sum(1, 5)
console.log(result)

```



```
const square = p => {
  console.log(p)
  return p * p
}
```

Moreover, one of the more ancient ways of referencing a function was simply giving a function declaraiton.

```
function product(a, b) {
  return a * b
}

const result = product(2, 6)
// result is now 12

```


Another way of defining or referencing functions would be usin ga dunciton expression :

const average = function(a,b) {
return (a+b)/2
}


const result = average(2,5)

//result is 3.5 

  
