# 🧠 Learn about Events In JavaScript
A JavaScript event is something that happens in the browser — like clicking a button, typing in a textbox, loading a page, or moving your mouse.

## What is a JavaScript Event?
A JavaScript event is something that happens in the browser — like clicking a button, typing in a textbox, loading a page, or moving your mouse.

JavaScript allows you to respond to these events using event listeners.

## 🎯 Examples of Events:

| Event       | Description                      |
| ----------- | -------------------------------- |
| `click`     | When a user clicks an element    |
| `mouseover` | When the mouse hovers over       |
| `mouseout`  | When the mouse leaves an element |
| `keydown`   | When a key is pressed            |
| `input`     | When input value changes         |
| `submit`    | When a form is submitted         |
| `load`      | When the page is fully loaded    |
| `scroll`    | When the page is scrolled        |

## 🔧 How to Handle Events in JavaScript

✅ 1. Using onclick or other attributes (HTML way):

```html 

<button onclick="sayHello()">Click Me</button>

<script>
  function sayHello() {
    alert("Hello Sajid!");
  }
</script>

```
