<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Functional Website</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

  <!-- Navigation -->
  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <!-- Main Content -->
  <div class="container">
    <h1>Welcome to Our Website!</h1>
    <p>This is a functional website example.</p>

    <!-- Form -->
    <form id="contact-form">
      <label for="name">Name:</label>
      <input type="text" id="name" name="name" required>

      <label for="email">Email:</label>
      <input type="email" id="email" name="email" required>

      <button type="submit">Submit</button>
    </form>

    <!-- Button -->
    <button id="alert-button">Click Me</button>
  </div>

  <script src="script.js"></script>
</body>
</html>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

nav {
  background-color: #333;
  color: #fff;
  padding: 10px;
}

nav ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

nav ul li {
  display: inline;
  margin-right: 20px;
}

.container {
  max-width: 800px;
  margin: 20px auto;
  text-align: center;
}

form {
  margin-bottom: 20px;
}

form label {
  display: block;
  margin-bottom: 5px;
}

form input {
  width: 100%;
  padding: 8px;
  margin-bottom: 10px;
  border: 1px solid #ccc;
}

form button {
  padding: 10px 20px;
  background-color: #333;
  color: #fff;
  border: none;
  cursor: pointer;
}

button {
  padding: 10px 20px;
  background-color: #333;
  color: #fff;
  border: none;
  cursor: pointer;
}

button:hover {
  background-color: #555;
}
// Form submission event listener
document.getElementById('contact-form').addEventListener('submit', function(event) {
  event.preventDefault(); // Prevent default form submission

  // Retrieve form values
  var name = document.getElementById('name').value;
  var email = document.getElementById('email').value;

  // Validate form fields
  if (name.trim() === '' || email.trim() === '') {
    alert('Please fill in all fields.');
    return;
  }

  // Simulate form submission (you can replace this with an actual form submission)
  alert('Form submitted successfully:\nName: ' + name + '\nEmail: ' + email);
});

// Button click event listener
document.getElementById('alert-button').addEventListener('click', function() {
  alert('Button clicked!');
});
