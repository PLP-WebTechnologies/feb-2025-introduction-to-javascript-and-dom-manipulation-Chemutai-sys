# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>DOM Manipulation Example</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header>
    <h1 id="main-heading">Welcome to My Page</h1>
  </header>

  <main>
    <section>
      <p id="dynamic-text">Click the button to change this text and color.</p>
      <button id="change-btn">Change Text & Style</button>
    </section>

    <section>
      <button id="toggle-element-btn">Add/Remove Element</button>
      <div id="toggle-area"></div>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 MySite</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>

 script.js
javascript

// Change text and style
document.getElementById('change-btn').addEventListener('click', function () {
  const text = document.getElementById('dynamic-text');
  text.textContent = "The text has been changed!";
  text.style.color = "green";
  text.style.fontWeight = "bold";
});

// Add or remove an element
document.getElementById('toggle-element-btn').addEventListener('click', function () {
  const area = document.getElementById('toggle-area');
  const existing = document.getElementById('new-element');

  if (existing) {
    area.removeChild(existing);
  } else {
    const newDiv = document.createElement('div');
    newDiv.id = "new-element";
    newDiv.textContent = "I'm a new element!";
    area.appendChild(newDiv);
  }
});
