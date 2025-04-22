<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <header>
        <h1 id="main-title">Welcome to My Interactive Page</h1>
    </header>
    
    <section>
        <p id="description">Click the button to change this text and style!</p>
        <button id="change-button">Change Text & Style</button>
    </section>
    
    <div>
        <h2>Dynamic List</h2>
        <ul id="item-list">
          <li>Sample Item</li>
        </ul>
        <button id="add-item-button">Add Item</button>
        <button id="remove-item-button">Remove Last Item</button>
    </div>
    
    <footer>
        <p>&copy; 2025 Interactive Web</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>

document.getElementById("change-button").addEventListener("click", function () {
    const description = document.getElementById("description");
    description.textContent = "The text has been updated!";
    description.style.color = "white";
    description.style.backgroundColor = "teal";
    description.style.padding = "10px";
    description.style.borderRadius = "5px";
});
  
document.getElementById("add-item-button").addEventListener("click", function () {
    const ul = document.getElementById("item-list");
    const newItem = document.createElement("li");
    newItem.textContent = "New List Item";
    ul.appendChild(newItem);
});
  
document.getElementById("remove-item-button").addEventListener("click", function () {
    const ul = document.getElementById("item-list");
    if (ul.lastElementChild) {
      ul.removeChild(ul.lastElementChild);
    }
});
  
