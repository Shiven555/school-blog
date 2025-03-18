<!DOCTYPE html>
<html lang="en">
<head>
    <link rel="html.css" href="">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Advanced Web Project</title>
    <style>
        :root {
            --bg-light: linear-gradient(to right, #f4f4f4, #ecf0f1);
            --bg-dark: linear-gradient(to right, #2c3e50, #34495e);
            --nav-light: #3498db;
            --nav-dark: #2c3e50;
            --text-light: #3498db;
            --text-dark: #ecf0f1;
            --btn-bg-light: #2ecc71;
            --btn-bg-dark: #16a085;
            --btn-hover-light: #27ae60;
            --btn-hover-dark: #1abc9c;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: var(--bg-light);
            margin: 0;
            padding: 0;
            color: var(--text-light);
            transition: background-color 0.3s, color 0.3s;
        }

        nav {
            background-color: var(--nav-light);
            color: white;
            padding: 15px;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
            font-size: 18px;
            font-weight: bold;
            transition: color 0.3s;
        }

        nav a:hover {
            color: var(--btn-hover-light);
        }

        section {
            padding: 50px;
            text-align: center;
        }

        h1 {
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }

        .btn {
            background-color: var(--btn-bg-light);
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            font-size: 18px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s, background-color 0.3s;
        }

        .btn:hover {
            background-color: var(--btn-hover-light);
            transform: scale(1.1);
        }

        .dark-mode {
            --bg-light: var(--bg-dark);
            --nav-light: var(--nav-dark);
            --text-light: var(--text-dark);
            --btn-bg-light: var(--btn-bg-dark);
            --btn-hover-light: var(--btn-hover-dark);
        }

        .contact-card {
            display: inline-block;
            padding: 20px;
            margin: 10px;
            border: 1px solid #ddd;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: box-shadow 0.3s;
        }

        .contact-card:hover {
            box-shadow: 0 8px 12px rgba(0, 0, 0, 0.2);
        }

        @media (max-width: 600px) {
            nav {
                font-size: 16px;
            }

            h1 {
                font-size: 24px;
            }

            .btn {
                font-size: 16px;
                padding: 10px 20px;
            }

            .contact-card {
                width: 90%;
            }
        }
    </style>
</head>
<body>
    <nav>
        <a href="#home">Home</a>
        <a href="#contact">Contact</a>
        <button class="btn" onclick="toggleDarkMode()">Toggle Dark Mode</button>
    </nav>

    <section id="home" class="home">
        <h1>Welcome to My Advanced Project 🚀</h1>
        <p>This is your interactive home page. Explore and connect!</p>
        <button class="btn" onclick="homeButtonClick()">Discover More</button>
    </section>

    <section id="contact" class="contact">
        <h1>Contact Us</h1>
        <div class="contact-card">
            <p><strong>Email:</strong> support@example.com</p>
        </div>
        <div class="contact-card">
            <p><strong>Phone:</strong> +123-456-7890</p>
        </div>
    </section>

    <script>
        function homeButtonClick() {
            alert('Welcome to the adventure!');
        }

        function toggleDarkMode() {
            document.body.classList.toggle('dark-mode');
        }
    </script>
</body>
</html>
