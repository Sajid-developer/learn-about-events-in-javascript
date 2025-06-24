# 🧠 Learn about Events In JavaScript

## What is a JavaScript Event?
A JavaScript `event` is something that happens in the browser — like clicking a button, typing in a textbox, loading a page, or moving your mouse.

JavaScript allows you to respond to these events using event listeners.

## 🎯 Examples of Events:

| Event Name     | Trigger Condition                        | Common Use Case                          | Example Listener                            |
|----------------|------------------------------------------|------------------------------------------|---------------------------------------------|
| `click`        | When an element is clicked               | Buttons, links, interactive elements     | `element.addEventListener('click', ...)`    |
| `dblclick`     | When an element is double-clicked        | Zooming, custom action triggers          | `element.addEventListener('dblclick', ...)` |
| `mouseover`    | When mouse enters an element             | Hover effects, tooltips                  | `element.addEventListener('mouseover', ...)`|
| `mouseout`     | When mouse leaves an element             | Revert hover changes                     | `element.addEventListener('mouseout', ...)` |
| `mousedown`    | When mouse button is pressed down        | Drag, hold actions                       | `element.addEventListener('mousedown', ...)`|
| `mouseup`      | When mouse button is released            | End of drag                              | `element.addEventListener('mouseup', ...)`  |
| `keydown`      | When a key is pressed                    | Shortcuts, typing detection              | `document.addEventListener('keydown', ...)` |
| `keyup`        | When a key is released                   | Confirm input after key release          | `document.addEventListener('keyup', ...)`   |
| `input`        | When value of input/textarea changes     | Live validation, live search             | `input.addEventListener('input', ...)`      |
| `change`       | When input value changes and loses focus | Dropdowns, checkboxes                    | `input.addEventListener('change', ...)`     |
| `submit`       | When a form is submitted                 | Form handling, validation                | `form.addEventListener('submit', ...)`      |
| `load`         | When page or image is fully loaded       | Init scripts after everything loads      | `window.addEventListener('load', ...)`      |
| `scroll`       | When user scrolls the page               | Infinite scroll, animations              | `window.addEventListener('scroll', ...)`    |
| `focus`        | When an element gets focus               | Input field styling, form interactions   | `input.addEventListener('focus', ...)`      |
| `blur`         | When an element loses focus              | Hide hints, validate input               | `input.addEventListener('blur', ...)`       |


---

## 🔧 How to Handle Events in JavaScript

✅ 1. Using `onclick` or other attributes (HTML way):

```html 

<button onclick="sayHello()">Click Me</button>

<script>
  function sayHello() {
    alert("Hello Sajid!");
  }
</script>

```


✅ 2. Using `addEventListener()` (Recommended Modern Way):

```html 

<button id="btn">Click Me</button>

<script>
  const button = document.getElementById("btn");

  button.addEventListener("click", function() {
    alert("Button clicked!");
  });
</script>

```

Note : `addEventListener()` is flexible, supports multiple handlers, and separates HTML from JS.

---

## 💡 Event Listener Syntax:

```javascript 

element.addEventListener("eventType", callbackFunction);

```

---

## 🧪 Common Event Examples

### ☑️ Click Event

```javascript 

button.addEventListener("click", () => {
  console.log("Clicked!");
});

```

### ☑️ Mouseover and Mouseout

```javascript 

element.addEventListener("mouseover", () => {
  element.style.color = "red";
});

element.addEventListener("mouseout", () => {
  element.style.color = "black";
});

```

### ☑️ Keyboard Events

```javascript 

document.addEventListener("keydown", (event) => {
  console.log("Key pressed:", event.key);
});

```

### ☑️ Input Event

```html 

<input type="text" id="name" placeholder="Type your name" />

```

```javascript 

const input = document.getElementById("name");

input.addEventListener("input", () => {
  console.log("You typed:", input.value);
});

```

### ☑️ Form Submit Event

```html 

<form id="myForm">
  <input type="text" />
  <button type="submit">Submit</button>
</form>

```

```javascript 

document.getElementById("myForm").addEventListener("submit", function(e) {
  e.preventDefault(); // Prevent page reload
  alert("Form submitted!");
});

```

---

## 📥 Event Object

Every event has a built-in object that gives you details like:

- `event.target` → The actual element

- `event.key` → The key pressed

- `event.preventDefault()` → Stops default behavior

- `event.stopPropagation()` → Stops event bubbling


```javascript 

button.addEventListener("click", function(event) {
  console.log(event.target); // The clicked element
});

```

---


## 🔁 Event Bubbling & Capturing

### 🔹 Event Bubbling:

- Events bubble up from child to parent.

- Default behavior in JavaScript.

### 🔹 Example:

```html 

<div id="parent">
  <button id="child">Click Me</button>
</div>

```

```javascript 

document.getElementById("parent").addEventListener("click", () => {
  console.log("Parent clicked");
});

document.getElementById("child").addEventListener("click", () => {
  console.log("Child clicked");
});
// Output: "Child clicked", then "Parent clicked"

```

---

## Show your support

If you find it helpful in your learning journey then kindly give a star ⭐ to this repo to help others discover it.

Thanks for reading 🙏🏼.
