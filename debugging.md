


Debugging

For each of the following questions, start by understanding and explaining why the given piece of code doesn’t work. Then propose a couple of fixes, and rewrite the code to implement one of the fixes you proposed so the program works correctly:

### I want this code to log out "hey amy", but it logs out "hey arnold" - why?
```
function greet(person) {
  if (person == { name: 'amy' }) {
    return 'hey amy'
  } else {
    return 'hey arnold'
  }
}
greet({ name: 'amy' })
```

<br/><br/><br/><br/><br/>

### I want this code to log out the numbers 0, 1, 2, 3 in that order, but it doesn’t do what I expect (this is a bug you run into once in a while, and some people love to ask about it in interviews).
```
for (var i = 0; i < 4; i++) {
  setTimeout(() => console.log(i), 0)
}
```

<br/><br/><br/><br/><br/>

### I want this code to log out "doggo", but it logs out undefined!

```
let dog = {
  name: 'doggo',
  sayName() {
    console.log(this.name)
  }
}
let sayName = dog.sayName
sayName()
```

<br/><br/><br/><br/><br/>


### I want my dog to bark(), but instead I get an error. Why?

```
function Dog(name) {
  this.name = name
}
Dog.bark = function() {
  console.log(this.name + ' says woof')
}
let fido = new Dog('fido')
fido.bark()
```

<br/><br/><br/><br/><br/>


### Why does this code return the results that it does?

```
function isBig(thing) {
  if (thing == 0 || thing == 1 || thing == 2) {
    return false
  }
  return true
}
isBig(1)    // false
isBig([2])  // false
isBig([3])  // true
```
