# Building a Counter UI by Composing Callbacks

**[📹 Video](https://egghead.io/lessons/egghead-building-a-timer-ui-by-composing-callbacks)**

## Remember:

- `listener` is a function that is called when an event or something happens
- `broadcaster` is a function that returns a `listener`
- `operator` is a function that accepts one or more `broadcasters`
- You can also have a configuration function that resurns an `operator` (the `app` case)

## Functions

### addListener

- is a `broadcaster`
- is the one setting up the document eventListener
- the value that the `listener` will be callse with, will be the click event (since we are using [PointFree style](https://egghead.io/lessons/egghead-pointfree-programming-in-javascript) to pass the listener function to the `addEventListener` (the second parameter)
- by having functions that return other functions that return other functions, we are taking advantage of closures because the function that accepts a listener (last function) **can remember** all the previous values set by the parent scopes. this is very important and useful to advance or delay function executions.

```js
let addListener = (selector, eventType) => (listener) => {
  let element = document.querySelector(selector)
  element.addEventListener(eventType, listener)
  //                                     ☝️
  // See that the `listener` function (input function) is being passed as a callback to the `addEventListener` DOM event
}
```

### merge

- is an `operator` that receives TWO `broadcasters`
- this is how it setup both `plusClick` and `minusClick`, that way it can pass the same listener to both broadcasters
- `merge` is used to create our counter

```js
let merge = (b1, b2) => (listener) => {
  b1(listener)
  b2(listener)
  // same listener to both broadcasters
}
```

### plusClick & minusClick

- both are `broadcasters` (because they return a function that accepts a `listener`)
- here is where you wire up the DOM buttons and the type of event you will be listening to

```js
let plusClick = addListener("#plus", "click")
let minusClick = addListener("#minus", "click")

// example of how to call them:
plusClick("#plus", "click")((value) => console.log(value))
// This function will setup the "#plus" button to listen to the click event, and will call the last function passed. this will result in loggin in the console the MouseEvent from all the clicks to the button with id "#plus"
```

### hardCode

- this function is used to "hardCode" the value passed to the listener
- in this example, by default the value passed to the listener will always be the click event because that's what we setup in the `addListener` broadcaster
- in this function, we are creating a new anonymous `listener`function, that accepts `value` (which will be the Mouse Event) and _ignores it_ in favor of the `newValue` passed in the config function. You can say that _the new listener is calling the original listener_.
- `hardCode` will always pass to the listener the same value (the one hardcoded)

```js
let hardCode = (newValue) => (broadcaster) => (listener) => {
  broadcaster((value) => {
    // `value is ignored, we can even implement this function without setting any parameters to this function
    listener(newValue) // newValue is being passed always to the listener function
  })
}
```

### add

- is a `configuration function` (accepts a value that returns a function that accepts a broadcaster that also returns a function that accepts a listener)
- this one does use the same technique to ignore the original value passed to the listener and override the value with another one (`initial += value` instead of just the `value`)
- you see how `initial` is being _closed_ (capture or remembered however you prefer to call it) so its accessible within the listener function passed to the broadcaster? (✨ MAGIC ✨)

```js
let add = (initial) => (broadcaster) => (listener) => {
  broadcaster((value) => {
    listener((initial += value))
  })
}
```

### plusOne & minusOne

- both are `broadcasters` (functions that accepts a `listener`)
- `1` and `-1` are the hardcoded values (`newValue` variable in `hardCode` function)
- this syntax is quite common to see when you have a function that returns another function (two sets of parenthesis after the function name)
- this functions are needed to set the value steps each button will take (1 & -1)

```js
let plusOne = hardCode(1)(plusClick)
let minusOne = hardCode(-1)(minusClick)
```

### counter

- FINALLY! we got into our counter!
- counter is calling a config function (add) with both the initial value (0) and the result of `merge` being passed to a the second function of add (the one that accepts a broadcaster)
- you can also see how we are passing the final listener function to `counter` (logging the value passed)

```js
let counter = add(0)(merge(plusOne, minusOne))

counter((value) => {
  console.log(value)
})
```

## References

- [Pointfree Programming in JavaScript by Kyle Shevlin](https://egghead.io/lessons/egghead-pointfree-programming-in-javascript)
- [Just Enough Functional Programming in JavaScript by Kyle Shevlin](https://egghead.io/courses/just-enough-functional-programming-in-javascript)

---

📹 [Go to Previous Lesson](https://egghead.io/lessons/egghead-use-buffers-to-store-values-until-a-condition-is-met)
📹 [Go to Next Lesson](https://egghead.io/lessons/egghead-building-a-timer-ui-by-composing-callbacks)
