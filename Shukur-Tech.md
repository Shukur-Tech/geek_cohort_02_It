<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Learning Progress</title>
    <link rel="icon" href="favicon.ico">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <style>
        :root {
    --primary-bg: #f9f9f9;
    --primary-text: #1a1a1a;
    --accent: #0070f3;
    --header-bg: #fff;
    --footer-bg: #f1f1f1;
    --card-bg: #fff;
    --border-radius: 12px;
    --transition: 0.3s;
}

body {
    margin: 0;
    font-family: 'Segoe UI', 'Roboto', Arial, sans-serif;
    background: var(--primary-bg);
    color: var(--primary-text);
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    transition: background var(--transition), color var(--transition);
}

header {
    background: var(--header-bg);
    box-shadow: 0 2px 8px rgba(0,0,0,0.02);
    padding: 2rem 1rem 1rem 1rem;
    text-align: center;
    border-bottom: 1px solid #eaeaea;
}

h1 {
    margin: 0;
    font-size: 2.3rem;
    letter-spacing: 1px;
    color: var(--accent);
}

main {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: flex-start;
    padding: 2rem 1rem;
    background: var(--primary-bg);
}

section {
    background: var(--card-bg);
    border-radius: var(--border-radius);
    box-shadow: 0 2px 16px rgba(0,0,0,0.04);
    max-width: 600px;
    width: 100%;
    padding: 2rem;
    margin: 0 auto;
}

h2 {
    margin-top: 0;
    color: var(--accent);
    font-size: 1.4rem;
    margin-bottom: 1.5rem;
}

ol {
    padding-left: 1.2rem;
}

li {
    margin-bottom: 1.5rem;
}

li strong {
    font-size: 1.1em;
    color: #222;
}

a {
    color: var(--accent);
    text-decoration: underline;
    transition: color var(--transition);
}

a:hover, a:focus {
    color: #0050b3;
}

footer {
    background: var(--footer-bg);
    text-align: center;
    padding: 1rem 0;
    font-size: 1rem;
    color: #888;
    border-top: 1px solid #eaeaea;
}

#toggle-theme {
    position: fixed;
    bottom: 1.2rem;
    right: 1.2rem;
    border: none;
    background: var(--accent);
    color: #fff;
    border-radius: 50%;
    width: 48px;
    height: 48px;
    font-size: 1.5rem;
    box-shadow: 0 2px 8px rgba(0,0,0,0.10);
    cursor: pointer;
    transition: background var(--transition), color var(--transition);
    z-index: 100;
}

#toggle-theme:hover, #toggle-theme:focus {
    background: #0050b3;
}

/* Dark mode styles */
body.dark {
    --primary-bg: #191b22;
    --primary-text: #e5e9f0;
    --header-bg: #232531;
    --footer-bg: #191b22;
    --card-bg: #232531;
    --accent: #61dafb;
}

body.dark #toggle-theme {
    background: #232531;
    color: #61dafb;
}

@media (max-width: 700px) {
    section {
        padding: 1rem;
        font-size: 1rem;
    }
    h1 {
        font-size: 1.5rem;
    }
    h2 {
        font-size: 1.1rem;
    }
}
    </style>
    <header>
        <h1>My Learning Progress In IT</h1>
    </header>
    <main>
        <section>
            <h2>What I Have Learned So Far</h2>
            <ol>
                <li>
                    <strong>What is GitHub?</strong>
                    <p>
                        GitHub is a web-based platform for version control and collaboration that allows developers to store, manage, and track changes in their projects using Git.
                    </p>
                </li>
                <li>
                    <strong>What is Git?</strong>
                    <p>
                        Git is a distributed version control system that helps developers track changes in their code, collaborate with others, and manage project history.
                    </p>
                </li>
                <li>
                    <strong>What is GitHub Desktop?</strong>
                    <p>
                        GitHub Desktop is a graphical user interface application that makes it easy to interact with Git and GitHub without using the command line.
                    </p>
                </li>
                <li>
                    <strong>How to Create a GitHub Account</strong>
                    <p>
                        To create a GitHub account easily, go to <a href="https://github.com" target="_blank" rel="noopener">github.com</a>, click on "Sign up", and follow the instructions to register.
                    </p>
                </li>
                <li>
                    <strong>What is a Repository?</strong>
                    <p>
                        A repository (or "repo") is a storage space where your project files and revision history are kept.
                    </p>
                </li>
                <li>
                    <strong>What is a Commit?</strong>
                    <p>
                        A commit is a snapshot of your repository at a specific point in time. It saves changes you've made to your files.
                    </p>
                </li>
                <li>
                    <strong>How to Host on GitHub</strong>
                    <p>
                        You can host your code or website on GitHub by pushing your project to a repository. For web projects, GitHub Pages can be used to publish your site live.
                    </p>
                </li>
            </ol>
        </section>
    </main>
    <footer>
        <p>Keep learning and building!</p>
    </footer>
    <button id="toggle-theme" aria-label="Toggle dark/light mode">🌙</button>
    <script src="main.js">
          // Toggle light/dark mode
const btn = document.getElementById('toggle-theme');
const prefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;

function setTheme(dark) {
    document.body.classList.toggle('dark', dark);
    btn.textContent = dark ? '☀️' : '🌙';
    localStorage.setItem('theme', dark ? 'dark' : 'light');
}

// Load saved or system theme on start
const savedTheme = localStorage.getItem('theme');
if (savedTheme === 'dark' || (prefersDark && !savedTheme)) {
    setTheme(true);
} else {
    setTheme(false);
}

btn.addEventListener('click', () => {
    setTheme(!document.body.classList.contains('dark'));
});
    </script>
</body>
</html>
