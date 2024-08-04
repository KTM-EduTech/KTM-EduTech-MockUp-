
# Simple HTML 5 Website Template

I used HTML and CSS to create a basic structure for your website. Focusing on creating the main structure and the home page, and then I will provide guidance on how to expand it for the other pages.



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Name - Personal Website</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --main-color: #997516;
            --secondary-color: #e91a1a;
            --bg-color: #121212;
            --text-color: #ffffff;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: "Poppins", sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
        }

        .container {
            width: 80%;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            background-color: var(--bg-color);
            padding: 20px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        /* NAVBAR STARTS HERE */
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 90%;
            margin: auto;
        }

        .logo img {
            height: 50px;
        }

        .logo-small {
            display: none;
        }

        .nav-links {
            display: flex;
            justify-content: space-around;
            width: 60%;
        }

        .nav-links li {
            list-style: none;
        }

        .nav-links a {
            color: var(--text-color);
            text-decoration: none;
            font-weight: bold;
        }

        .burger {
            display: none;
            cursor: pointer;
        }

        .burger div {
            width: 25px;
            height: 3px;
            background-color: var(--text-color);
            margin: 5px;
            transition: all 0.3s ease;
        }

        h1,
        h2 {
            color: var(--main-color);
        }

        footer {
            background-color: var(--bg-color);
            color: var(--text-color);
            text-align: center;
            padding: 20px 0;
            position: sticky;
            bottom: 0;
        }

        @media screen and (max-width: 768px) {
            .nav-links {
                position: absolute;
                right: 0px;
                height: 92vh;
                top: 8vh;
                background-color: var(--bg-color);
                display: flex;
                flex-direction: column;
                align-items: center;
                width: 50%;
                transform: translateX(100%);
                transition: transform 0.5s ease-in;
            }

            .nav-links li {
                opacity: 0;
            }

            .burger {
                display: block;
            }

            .logo-large {
                display: none;
            }

            .logo-small {
                display: block;
            }
        }

        .nav-active {
            transform: translateX(0%);
        }

        @keyframes navLinkFade {
            from {
                opacity: 0;
                transform: translateX(50px);
            }
            to {
                opacity: 1;
                transform: translateX(0px);
            }
        }

        .toggle .line1 {
            transform: rotate(-45deg) translate(-5px, 6px);
        }

        .toggle .line2 {
            opacity: 0;
        }

        .toggle .line3 {
            transform: rotate(45deg) translate(-5px, -6px);
        }
        /* NAVBAR ENDS HERE */


        .welcome-message {
            text-align: center;
            padding: 50px 0;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
        }

        .skill {
            width: 48%;
            margin-bottom: 20px;
        }

        .skill-bar {
            height: 20px;
            background-color: var(--secondary-color);
            border-radius: 10px;
        }

        footer {
            background-color: var(--bg-color);
            color: var(--text-color);
            text-align: center;
            padding: 20px 0;
            position: sticky;
            bottom: 0;
        }

        @media (max-width: 768px) {
            .container {
                width: 95%;
            }

            .skill {
                width: 100%;
            }

        /* Copy the styles from the about page, then add these additional styles */
        }
        .about-section {
            margin-bottom: 40px;
        }
        .about-section h2 {
            margin-bottom: 20px;
        }
        .about-section p {
            margin-bottom: 15px;
        }

        /* Copy the styles from the home page, then add these additional styles */
        .career-item {
            margin-bottom: 30px;
            border-left: 3px solid var(--main-color);
            padding-left: 20px;
        }
        .career-item h3 {
            color: var(--secondary-color);
        }
        .career-item p {
            margin-bottom: 10px;
        }
        
        /* Copy the styles from the home page, then add these additional styles */
        .service-item {
            background-color: rgba(153, 117, 22, 0.1);
            border-radius: 10px;
            padding: 20px;
            margin-bottom: 20px;
        }
        .service-item h3 {
            color: var(--secondary-color);
        }
 
        /* Copy the styles from the home page, then add these additional styles */
        .service-item {
            background-color: rgba(153, 117, 22, 0.1);
            border-radius: 10px;
            padding: 20px;
            margin-bottom: 20px;
        }
        .service-item h3 {
            color: var(--secondary-color);
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">
                <a href="index.html">
                    <img src="https://i.ibb.co/z4QWGJZ/KTM-Edu-Tech-Logo.png" alt="KTM EduTech Logo" class="logo-large">
                    <img src="https://i.ibb.co/JvXkFbv/ktm-favicon.png" alt="KTM EduTech Logo" class="logo-small">
                </a>
            </div>
            <ul class="nav-links">
                <li><a href="index.html">Home</a></li>
                <li><a href="about.html">About</a></li>
                <li><a href="career.html">Career</a></li>
                <li><a href="services.html">Services</a></li>
                <li><a href="portfolio.html">Portfolio</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
            <div class="burger">
                <div class="line1"></div>
                <div class="line2"></div>
                <div class="line3"></div>
            </div>
        </nav>
    </header>

    <main>
        <section id="home" class="container">
            <div class="welcome-message">
                <h1>Welcome to My Personal Website</h1>
                <p>I'm an experienced computer science educator and web developer passionate about creating innovative web solutions.</p>
            </div>

            <h2>My Skills</h2>
            <div class="skills">
                <div class="skill">
                    <p>3D SketchUp</p>
                    <div class="skill-bar" style="width: 83%;"></div>
                </div>
                <div class="skill">
                    <p>Blogger</p>
                    <div class="skill-bar" style="width: 98%;"></div>
                </div>
                <div class="skill">
                    <p>Book Creator</p>
                    <div class="skill-bar" style="width: 76%;"></div>
                </div>
                <div class="skill">
                    <p>Canva</p>
                    <div class="skill-bar" style="width: 88%;"></div>
                </div>
                <div class="skill">
                    <p>Cloudflare (SSL, Sites)</p>
                    <div class="skill-bar" style="width: 78%;"></div>
                </div>
                <div class="skill">
                    <p>GitHub (Repositories, Pages)</p>
                    <div class="skill-bar" style="width: 94%;"></div>
                </div>
                <div class="skill">
                    <p>Google Apps</p>
                    <div class="skill-bar" style="width: 98%;"></div>
                </div>
                <div class="skill">
                    <p>Office 365</p>
                    <div class="skill-bar" style="width: 78%;"></div>
                </div>
                <div class="skill">
                    <p>Pixlr</p>
                    <div class="skill-bar" style="width: 100%;"></div>
                </div>
                <div class="skill">
                    <p>WordPress</p>
                    <div class="skill-bar" style="width: 99%;"></div>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <p>&copy; <span id="year"></span> | KTM EduTech</p>
    </footer>

    <script>
        document.getElementById('year').textContent = new Date().getFullYear();
    </script>
</body>
</html>

```

This HTML file creates the basic structure of your personal website with a focus on the home page. Here's a breakdown of what's included:

1. The page uses the dark mode color scheme you specified.
2. The Poppins font is imported and applied to the body.
3. A sticky header with navigation links is implemented.
4. The home page includes a welcome message and your skills section.
5. A sticky footer with the copyright information is added.
6. The layout is responsive and should work well on different screen sizes.

To complete your website, you'll need to create separate HTML files for each of the other pages (About, Career Highlights, Services, Portfolio, and Contact). You can use the same basic structure and styling, but replace the content in the `<main>` section with the relevant information for each page.

For the Portfolio page, you can embed the frames for your projects like this:

```html
<section id="portfolio" class="container">
    <h2>Portfolio</h2>
    <iframe src="https://www.ictclickdigitalmedia.net" width="100%" height="500px"></iframe>
    <iframe src="https://www.ictdir.net" width="100%" height="500px"></iframe>
</section>
```

For the Contact page, you can create a two-column layout like this:

```html
<section id="contact" class="container">
    <h2>Contact</h2>
    <div class="contact-columns">
        <div class="contact-info">
            <p>Phone: +66644295023</p>
            <p>Email: contact@kydmasong.net</p>
            <p>Address: The Parkland Bangna, Bangna Trad 37, Bangna, Bangkok, Thailand</p>
            <div class="social-links">
                <a href="https://github.com/KTM-EduTech">GitHub</a>
                <a href="https://www.linkedin.com/in/kydmasong/">LinkedIn</a>
                <a href="https://www.youtube.com/@KTMasongTV">YouTube</a>
            </div>
        </div>
        <div class="contact-form">
            <form action="mailto:contact@kydmasong.net" method="post" enctype="text/plain">
                <input type="text" name="name" placeholder="Your Name" required>
                <input type="email" name="email" placeholder="Your Email" required>
                <textarea name="message" placeholder="Your Message" required></textarea>
                <button type="submit">Send</button>
            </form>
        </div>
    </div>
</section>
```

Remember to add appropriate CSS to style these elements.

To create a full, multi-page website, you'll need to:

1. Create separate HTML files for each page (about.html, career.html, services.html, portfolio.html, contact.html).
2. Copy the basic structure (header, footer, and styles) to each file.
3. Update the content in the `<main>` section of each file with the relevant information provided in your specifications.
4. Ensure that the navigation links in the header point to the correct files.

<hr>

