<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For Tabitha</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f0f0f0;
        }
        .login-container, .info-container {
            background-color: white;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        .hidden {
            display: none;
        }
        input {
            padding: 8px;
            margin: 5px 0;
            width: 200px;
        }
        button {
            padding: 10px 20px;
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        h1 {
            color: #333;
        }
    </style>
</head>
<body>
    <!-- Login Page -->
    <div id="loginPage" class="login-container">
        <h1>Welcome Tabitha!</h1>
        <p>Please login to see your special information</p>
        <input type="text" id="username" placeholder="Username"><br>
        <input type="password" id="password" placeholder="Password"><br>
        <button onclick="checkLogin()">Login</button>
        <p id="error" style="color: red;"></p>
    </div>

    <!-- Information Page -->
    <div id="infoPage" class="info-container hidden">
        <h1>My Dearest Tabitha</h1>
        <p>Here's some special information just for you:</p>
        <ul>
            <li>You are the most amazing wife in the world</li>
            <li>I love your beautiful smile that lights up my day</li>
            <li>Your kindness and caring nature inspire me every day</li>
            <li>Our adventures together are my favorite memories</li>
            <li>I’m so grateful to have you by my side</li>
        </ul>
        <p>Love you always, <br>Your Husband</p>
        <button onclick="logout()">Logout</button>
    </div>

    <script>
        // Simple login check (username: tabitha, password: love)
        function checkLogin() {
            const username = document.getElementById('username').value.toLowerCase();
            const password = document.getElementById('password').value;
            const error = document.getElementById('error');

            if (username === 'tabitha' && password === 'love') {
                document.getElementById('loginPage').classList.add('hidden');
                document.getElementById('infoPage').classList.remove('hidden');
                error.textContent = '';
            } else {
                error.textContent = 'Incorrect username or password';
            }
        }

        function logout() {
            document.getElementById('infoPage').classList.add('hidden');
            document.getElementById('loginPage').classList.remove('hidden');
            document.getElementById('username').value = '';
            document.getElementById('password').value = '';
        }
    </script>
</body>
</html>
