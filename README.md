<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Database Website</title>
</head>
<body>
<style>
    body {
    font-family: 'Arial', sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: #fff;
    padding: 10px;
    text-align: center;
}

main {
    max-width: 600px;
    margin: 20px auto;
    padding: 20px;
    border: 1px solid #ddd;
}

form {
    display: flex;
    flex-direction: column;
}

label {
    margin-bottom: 8px;
}

input {
    margin-bottom: 16px;
    padding: 8px;
}

button {
    background-color: #333;
    color: #fff;
    padding: 10px;
    cursor: pointer;
}

button:hover {
    background-color: #555;
}

#userData {
    margin-top: 20px;
}

</style>
    <header>
        <h1>Database Website</h1>
    </header>

    <main>
        <form id="userForm">
            <label for="name">Name:</label>
            <input type="text" id="name" name="name" required>

            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required>

            <button type="button" onclick="submitForm()">Submit</button>
        </form>

        <div id="userData">
            <!-- Display user data here -->
        <a href="admin.html" class="hidden()">show data</a>
        </div>
    </main>

    <script>
function submitForm() {
    // Get user input
    const name = document.getElementById('name').value;
    const email = document.getElementById('email').value;

    // Create an object with user data
    const userData = { name, email };

    // Store user data in local storage
    saveUserData(userData);

    // Display user data
    displayUserData();
}

function saveUserData(userData) {
    // Retrieve existing user data from local storage
    const existingData = JSON.parse(localStorage.getItem('userData')) || [];

    // Add new user data to the array
    existingData.push(userData);

    // Save the updated array back to local storage
    localStorage.setItem('userData', JSON.stringify(existingData));
}

function displayUserData() {
    // Retrieve user data from local storage
    const userData = JSON.parse(localStorage.getItem('userData')) || [];

    // Display user data in the #userData div
    const userDataDiv = document.getElementById('userData');
    userDataDiv.innerHTML = '';

    userData.forEach(user => {
        const userParagraph = document.createElement('p');
        userParagraph.textContent = `Name: ${user.name}, Email: ${user.email}`;
        userDataDiv.appendChild(userParagraph);
    });
}

// Display existing user data when the page loads
displayUserData();

    </script>
</body>
</html>
