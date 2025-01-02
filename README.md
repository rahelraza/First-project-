# First-project-


<form id="registration-form">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name"><br><br>
  <label for="email">Email:</label>
  <input type="email" id="email" name="email"><br><br>
  <label for="phone">Phone:</label>
  <input type="tel" id="phone" name="phone"><br><br>
  <label for="event">Event:</label>
  <select id="event" name="event">
    <option value="select">Select an event</option>
    <option value="event1">Event 1</option>
    <option value="event2">Event 2</option>
    <option value="event3">Event 3</option>
  </select><br><br>
  <input type="submit" value="Register">
</form>

<div id="registration-status"></div>




const form = document.getElementById('registration-form');
const statusDiv = document.getElementById('registration-status');

form.addEventListener('submit', (e) => {
  e.preventDefault();
  const name = document.getElementById('name').value;
  const email = document.getElementById('email').value;
  const phone = document.getElementById('phone').value;
  const event = document.getElementById('event').value;

  if (name && email && phone && event !== 'select') {
    // Assuming you have a server-side script to handle the registration
    // You can send the data to the server using fetch or XMLHttpRequest
    statusDiv.innerHTML = 'Registration successful!';
  } else {
    statusDiv.innerHTML = 'Please fill out all fields correctly.';
  }
});
