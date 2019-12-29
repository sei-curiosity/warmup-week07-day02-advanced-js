# warmup-week07-day02-advanced-js

## Exports & Imports(Modules)
<p>Javascript Import statement is used to import bindings that are exported by another module. If you have a very complex app and have to scroll through hundreds or thousands of lines of code, then a job of debugging or just understanding the app becomes much harder. Fortunately, Javascript helps us by having the ‘imports’ and ‘exports.’</p>

### How to use Exports & Imports
- Inside warmup-w7-d2 create a new file called data.js
- Inside data.js you have created add the following code
```js
    const course = {
        name: "SEI9",
        numOfStudents: 24
    } 
    export default course // export course object
```
- Inside warmup-w7-d2/app.js add the following code 
```js
import myCourse from './data.js' // import course object and then assign to myCourse 
console.log(myCourse)
```


## Spread & Rest Operators
```js
...
```
### Spread
<p>Used to split up array elements OR Object properties</p>

```js
// array
const oldArray = [1, 2, 3, 4]
const newArray = [...oldArray, 5, 6]
// object
const oldObject = {
    name: "SEI5" 
}
const newObject = {
    ...oldObject,
    numOfStudents: 24
}
```

### Rest
<p>Used to merge a list of function arguments into an array</p>

```js
function sortNumbers (...numbers){
    return numbers.sort()
}
console.log(sortNumbers(9, 2, 4, 8, 1))
```

## Destructuring
<p>Extract array elements or object properties and store them in variables</p>

### Array Destructuring
```js
const courses = ["SEI5", "SEI9"]
const [ , myCourse] = courses
```

### Object Destructuring
```js
const car = {
    type:"Fiat",
    model:"500",
    color:"white"
}
const { model } = car
```