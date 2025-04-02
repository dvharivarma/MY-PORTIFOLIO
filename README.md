<!DOCTYPE html><html lang="en">
<head>
    <title>MY PORTFOLIO</title>
    <style>
        body {font-family: Arial, sans-serif; margin: 0; padding: 0; background-color: #f9f9f9;text-align: center;}
        header {background-color: #222;color: white;padding: 20px; font-size: 20px;}
        h1 {margin: 10px 0;}
        button {background-color: #007bff; border: none; color: white; padding: 12px 24px;margin: 8px; cursor: pointer; font-size: 18px;border-radius: 5px; transition: background-color 0.3s;}
        button:hover {background-color: #0056b3;}
        .content {display: none; padding: 30px; background-color: white; box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1); margin: 20px auto; max-width: 800px; border-radius: 10px;}
        footer {background-color: #222;color: white;padding: 15px;font-size: 14px;}
    </style>
    <script>
        function showSection(sectionId) {var sections = document.getElementsByClassName("content");for (var i = 0; i < sections.length; i++) {sections[i].style.display = "none";} document.getElementById(sectionId).style.display = "block";}
    </script>
</head>
<body>
    <header>
        <h1>Welcome To My Portfolio</h1>
        <button onclick="showSection('about')">ABOUT</button> <button onclick="showSection('skills')">SKILLS</button> <button onclick="showSection('projects')">PROJECTS</button> <button onclick="showSection('contact')">CONTACT</button>
    </header>
    <main>
        <div id="about" class="content">
            <h1>About Me</h1>
            <p>I am a passionate web developer eager to contribute to innovative projects. My expertise lies in coding, designing, and developing user-friendly applications.</p>
        </div>
        <div id="skills" class="content">
            <h1>Technical Skills</h1>
            <ul>
                <li>Python</li> <li>JavaScript</li> <li>HTML & CSS</li> <li>React.js</li>
            </ul>
        </div>
        <div id="projects" class="content">
            <h1>My Projects</h1>
            <h3>To-Do List App</h3>
            <p>Developed a fully functional task management system, enabling users to efficiently handle 100+ tasks with real-time updates.</p>
            <h3>Random Jokes Generator</h3>
            <p>Built a web application that fetches real-time jokes from an API, optimizing response time by 15% for a seamless user experience.</p>
        
        </div>
        <div id="contact" class="content">
            <h1>Contact Me</h1>
            <form>
                <label for="name">Name:</label> <input type="text" id="name" required><br>
                <label for="email">Email:</label> <input type="email" id="email" required><br>
                <label for="Bio">Bio:</label> <textarea id="Bio"  required></textarea><br>
                <button type="submit">Send</button>
            </form>
        </div>
    </main>
    <footer>
        <p>&copy; 2025 My Portfolio | Designed by Hari Varma</p>
    </footer>
</body>
</html>
