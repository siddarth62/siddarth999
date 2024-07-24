<!DOCTYPE html>
<html>
<head>
    <title>My Personal Website</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
        }
        header {
            background-color: #333;
            color: white;
            padding: 10px 0;
            text-align: center;
        }
        nav {
            display: flex;
            justify-content: center;
            background-color: #444;
        }
        nav a {
            color: white;
            padding: 14px 20px;
            text-decoration: none;
            text-align: center;
        }
        nav a:hover {
            background-color: #555;
        }
        .container {
            padding: 20px;
        }
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 10px 0;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>

<header>
    <h1>Welcome to My Website</h1>
</header>

<nav>
    <a href="#home" onclick="showPage('home')">Home</a>
    <a href="#about" onclick="showPage('about')">About</a>
    <a href="#contact" onclick="showPage('contact')">Contact</a>
</nav>

<div class="container">
    <div id="home" class="page">
        <h2>Home</h2>
        <p>This is the home page of my personal website. Here you can find information about me and my interests.</p>
    </div>
    <div id="about" class="page" style="display: none;">
        <h2>About</h2>
        <p>This is the about page. Here you can find information about my background, skills, and experiences.</p>
    </div>
    <div id="contact" class="page" style="display: none;">
        <h2>Contact</h2>
        <p>This is the contact page. Feel free to reach out to me through the following form:</p>
        <form>
            <label for="name">Name:</label><br>
            <input type="text" id="name" name="name"><br><br>
            <label for="email">Email:</label><br>
            <input type="email" id="email" name="email"><br><br>
            <label for="message">Message:</label><br>
            <textarea id="message" name="message"></textarea><br><br>
            <input type="submit" value="Submit">
        </form>
    </div>
</div>

<footer>
    <p>&copy; 2024 My Personal Website</p>
</footer>

<script>
    function showPage(pageId) {
        const pages = document.querySelectorAll('.page');
        pages.forEach(page => {
            page.style.display = 'none';
        });
        document.getElementById(pageId).style.display = 'block';
    }
</script>

</body>
</html>
