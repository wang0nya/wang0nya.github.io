---
title: Better console.logs
updated: 2018-10-18
---
If you work with javascript a lot, you probably often need to use `console.log()` to output some info as you go along.

It's usually just the plain old way though:
```javascript
(() => {
    // do stuff
    console.log('Success!')
})()
```
![plain](https://thepracticaldev.s3.amazonaws.com/i/7c9pbcb63avm83drprur.png)

Here are a few ways you could make your logs a bit more visually informative, and interesting 🙂

### Use `console.error()` for error logs
```javascript
(() => {
    // do stuff
    console.error('Oops, something went wrong!')
})()
```
![errorlog](https://thepracticaldev.s3.amazonaws.com/i/d2sjc7fbnab0ihih2718.png)

### Use `console.warn()` for warning logs
```javascript
(() => {
    // do stuff
    console.warn('Warning! Something doesnt seem right.')
})()
```
![warninglog](https://thepracticaldev.s3.amazonaws.com/i/5d5je9x3d5kex8y7kosz.png)

### Use `console.table()` for iterable objects
```javascript
function Person(firstName, lastName) {
  this.firstName = firstName
  this.lastName = lastName
}

const me = new Person('John', 'Smith')

console.table(me)
```
![tablelog](https://thepracticaldev.s3.amazonaws.com/i/smtigum4notzzl2gjrnq.png)


### Add your custom styles
```javascript
(() => {
    // do stuff
    console.log('%c%s',
            'color: green; background: yellow; font-size: 24px;','Success!')
})()
```
![custom_success](https://thepracticaldev.s3.amazonaws.com/i/2ey09anydalwx4jo89nk.png)

You can have a custom function in your code that lets you use "your own" log with colors directly

```javascript
function customLog(message, color='black') {
     switch (color) {
         case 'success':  
              color = 'Green'
              break
         case 'info':     
                 color = 'Blue'  
              break;
         case 'error':   
              color = 'Red'   
              break;
         case 'warning':  
              color = 'Orange' 
              break;
         default: 
              color = color
     }

     console.log(`%c${message}`, `color:${color}`)
}

customLog('Hello World!')
customLog('Success!', 'success')
customLog('Error!', 'error')
customLog('Warning!', 'warning')
customLog('Info...', 'info')
```
![custom_function](https://thepracticaldev.s3.amazonaws.com/i/utfaa6x2ryx37z9540nn.png)

Here's the [pen](https://codepen.io/wang0nya/pen/PyRJmO). 

Hope you found this useful and happy debugging! 😊