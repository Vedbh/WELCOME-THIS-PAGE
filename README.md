
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stylish Navbar and Sidebar</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
            color: #333;
            overflow-x: hidden; /* Hide horizontal scrollbar */
        }

        /* Navbar styling */
        header {
            background-color: #333;
            color: #fff;
            padding: 1em;
            text-align: center;
        }

        nav {
            background-color: #444;
            overflow: hidden;
        }

        nav a {
            float: left;
            display: block;
            color: #fff;
            text-align: center;
            padding: 14px 16px;
            text-decoration: none;
            transition: background-color 0.3s ease;
        }

        nav a:hover {
            background-color: #555;
        }

        /* Sidebar styling */
        .sidebar {
            height: 100%;
            width: 250px;
            position: fixed;
            z-index: 1;
            top: 0;
            left: -250px;
            background-color: #111;
            padding-top: 20px;
            transition: 0.5s;
        }

        .sidebar a {
            padding: 16px;
            text-decoration: none;
            font-size: 18px;
            color: #818181;
            display: block;
            transition: 0.3s;
        }

        .sidebar a:hover {
            color: #f1f1f1;
        }

        .open-btn {
            font-size: 20px;
            cursor: pointer;
            background-color: #333;
            color: #fff;
            border: none;
            padding: 10px;
            position: fixed;
            top: 10px;
            left: 10px;
            border-radius: 5px;
            z-index: 2;
        }

        .open-btn:hover {
            background-color: #555;
        }

        /* Page content */
        .content {
            margin-left: 250px;
            padding: 1em;
        }
        li{
            color: black;
        }
        form {
            background-color: silver;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            padding: 20px;
            width: 300px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
        }

        input, textarea {
            width: 100%;
            padding: 8px;
            margin-bottom: 16px;
            box-sizing: border-box;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button {
            background-color: #4caf50;
            color: #fff;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        button:hover {
            background-color: #45a049;
        }
        h2{
            color: red;
        }
        footer{
            background-color: silver;
        }
        .sign-in {
    float: right;
}

.sign-in a {
    padding: 14px 16px;
}
            </style>


    <header>
        <h1>HAPPY DIWALI</h1>
    </header>

    <!-- Sidebar toggle button -->
    <button class="open-btn" onclick="openNav()">☰ Open </button>

    <!-- Sidebar -->
    <div class="sidebar" id="mySidebar">
        <a href="javascript:void(0)" class="close-btn" onclick="closeNav()">×</a>
        <a href="https://vedbh.github.io/WELCOME-TO-HOME-PAGE/">Home</a>
        <a href="https://vedbh.github.io/WELCOME-TO-ABOUT-PAGE/">About</a>
        <a href="https://vedbhogayta.github.io/SERVICES/">Services</a>
        <a href="https://vedbh.github.io/CONTACT-US/">Contact Us</a>
        <a href="https://vedbh.github.io/SIGN-IN-PAGE/">Sign In</a>
    </div>

    <!-- Main content area -->
    <div class="content">
        <h2>Welcome to our website!</h2>
        <li>Online Buisness Ideas To Earn Money....<a href="#"> More</a></li><br>
        <li>How to download GTA 5 and GTA YCT In PC, download link and process...<a href="#">More</a></li><br>

    </div>
    

    <center><form>
        <!-- Add contact form fields here -->
        <label for="name">Name:</label>
        <input type="text" id="name" name="name" required>

        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>

        <label for="message">Message:</label>
        <textarea id="message" name="message" required></textarea>

        <button type="submit">Submit</button>
    </form>

    <footer>
        <p>&copy; 2023 Ved Website. All rights reserved.</p>
    </footer>

    
      
    <script>
        function openNav() {
            document.getElementById("mySidebar").style.left = "0";
        }

        function closeNav() {
            document.getElementById("mySidebar").style.left = "-250px";
        }
       

    </script>

