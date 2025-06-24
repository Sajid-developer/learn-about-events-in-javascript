# 🧠 Learn about Events In JavaScript

## What is a JavaScript Event?
A JavaScript `event` is something that happens in the browser — like clicking a button, typing in a textbox, loading a page, or moving your mouse.

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

---

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
