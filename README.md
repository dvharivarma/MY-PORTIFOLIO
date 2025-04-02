<!DOCTYPE html>
<html lang="en">
<head>
    <title>MY PORTFOLIO</title>
    <style>
        html, body {
            height: 100%;
            margin: 0;
            display: flex;
            flex-direction: column;
        }

        main {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center;
            width: 100%;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: #f9f9f9;
            text-align: center;
        }

        header {
            background-color: #222;
            color: white;
            padding: 20px;
            font-size: 20px;
        }

        h1 {
            margin: 10px 0;
        }

        button {
            background-color: #007bff;
            border: none;
            color: white;
            padding: 12px 24px;
            margin: 8px;
            cursor: pointer;
            font-size: 18px;
            border-radius: 5px;
            transition: background-color 0.3s;
        }

        button:hover {
            background-color: #0056b3;
        }

        .content {
            display: none;
            padding: 30px;
            background-color: white;
            box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
            margin: 20px auto;
            max-width: 800px;
            border-radius: 10px;
        }

        footer {
            background-color: #222;
            color: white;
            padding: 15px;
            font-size: 14px;
            text-align: center;
        }

        input {
            display: block;
            margin: 0 auto;
            text-align: center;
        }

        textarea {
            display: block;
            margin: 0 auto;
            text-align: center;
        }

        .content ul {
            list-style-type: disc;
            padding-left: 20px;
        }

        .content ul li {
            font-size: 18px;
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome To My Portfolio</h1>
        <button onclick="showSection('about')" class="button">ABOUT</button>
        <button onclick="showSection('skills')" class="button">SKILLS</button>
        <button onclick="showSection('projects')" class="button">PROJECTS</button>
        <button onclick="showSection('contact')" class="button">CONTACT</button>
        <button onclick="showSection('resume')" class="button">RESUME</button>
    </header>
    
    <main>
        <div id="about" class="content">
            <h1>ABOUT ME</h1>
            <p>I am a passionate web developer eager to contribute to innovative projects.</p>
        </div>
        <div id="skills" class="content">
            <h1 id="h1">TECHNICAL SKILLS</h1>
            <ul>
                <li>Python</li>
                <li>JavaScript</li>
                <li>HTML & CSS</li>
                <li>React.js</li>
            </ul>
        </div>
        <div id="projects" class="content">
            <h1>MY PROJECTS</h1>
            <h3>To-Do List App</h3>
            <p>Dynamic Web Application - My To-Do-List
 Built a to-do list application with task management capabilities, allowing users to manage 100+ tasks with real-time updates.
 Implemented responsive design, achieving 95% usability across mobile, tablet, and desktop devices.</h2></p>
            <h3>Random Jokes Generator</h3>
            <p>Built a web application that fetches real-time jokes from an API, optimizing response time by 15% for a seamless user experience.</p>
        </div>
        <div id="contact" class="content">
            <h1>CONTACT ME</h1>
            <form>
                <input type="text" id="name" required placeholder="Name"><br>
                <input type="email" id="email" required placeholder="Email"><br>
                <textarea id="Bio" required placeholder="Bio"></textarea><br>
                <button type="submit">Send</button>
            </form>
        </div>

        <div id="resume" class="content">
            <h1>MY RESUME</h1>
            <p>Click below 👇 to download my resume.</p>

<a id="downloadResume" href="resume.pdf" download="My_Resume.pdf">
    <button>Download My Resume</button>
</a>s        </div>
    </main>
    <footer>
        <p>&copy; 2025 My Portfolio | Designed by Hari Varma</p>
    </footer>
    <script>
        document.querySelectorAll("button").forEach(button => {
            button.addEventListener("click", function() {
                document.querySelectorAll("button").forEach(btn => {
                    btn.style.backgroundColor = "#007bff"; 
                });
                this.style.backgroundColor = "grey";
            });
        });

        function showSection(sectionId) {
            var sections = document.getElementsByClassName("content");

            for (var i = 0; i < sections.length; i++) {
                sections[i].style.display = "none";
            }

            document.getElementById(sectionId).style.display = "block";

            switch(sectionId) {
                case 'about':
                    document.querySelector("main").style.backgroundColor = "#f0f8ff";
                    break;
                case 'skills':
                    document.querySelector("main").style.backgroundColor = "#e6ffe6";
                    break;
                case 'projects':
                    document.querySelector("main").style.backgroundColor = "#fff0f0";
                    break;
                case 'contact':
                    document.querySelector("main").style.backgroundColor = "#e6ffe6";
                    break;
                default:
                    document.querySelector("main").style.backgroundColor = "#f0f8ff";
            }
            var downloadButton = document.getElementById("downloadResume");
            if (sectionId === "resume") {
                downloadButton.style.display = "block";
            } else {
                downloadButton.style.display = "none";
            }
        }
    </script>
</body>
</html>
