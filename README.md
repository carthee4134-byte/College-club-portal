# College-Club-Portal
student's College club portal

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>College Club Portal</title>

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: Arial, sans-serif;
            background: #f4f7fb;
            color: #243047;
            line-height: 1.6;
        }

        header {
            background: #14213d;
            color: white;
            padding: 18px 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 12px;
        }

        header h1 {
            font-size: 25px;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin-left: 16px;
        }

        nav a:hover {
            color: #fca311;
        }

        .hero {
            background: linear-gradient(120deg, #14213d, #315a9b);
            color: white;
            text-align: center;
            padding: 65px 20px;
        }

        .hero h2 {
            font-size: 36px;
            margin-bottom: 12px;
        }

        .hero p {
            margin-bottom: 22px;
        }

        .btn {
            display: inline-block;
            background: #fca311;
            color: #14213d;
            padding: 11px 20px;
            border: none;
            border-radius: 6px;
            font-weight: bold;
            text-decoration: none;
            cursor: pointer;
        }

        section {
            padding: 42px 8%;
            scroll-margin-top: 20px;
        }

        section h2 {
            text-align: center;
            margin-bottom: 25px;
        }

        .cards {
            display: grid;
            grid-template-columns: repeat(
                auto-fit, minmax(210px, 1fr)
            );
            gap: 20px;
        }

        .card {
            background: white;
            padding: 22px;
            border-radius: 10px;
            box-shadow: 0 3px 12px #00000012;
        }

        .card h3 {
            color: #315a9b;
            margin-bottom: 10px;
        }

        .card p {
            margin-bottom: 12px;
        }

        #register {
            background: #e8eef8;
        }

        form {
            max-width: 500px;
            margin: auto;
            background: white;
            padding: 25px;
            border-radius: 10px;
        }

        label {
            display: block;
            margin: 12px 0 5px;
            font-weight: bold;
        }

        input, select {
            width: 100%;
            padding: 11px;
            border: 1px solid #b8c3d5;
            border-radius: 5px;
            font-size: 15px;
        }

        form .btn {
            margin-top: 18px;
            width: 100%;
        }

        #message {
            margin-top: 15px;
            font-weight: bold;
            overflow-wrap: anywhere;
        }

        footer {
            background: #14213d;
            color: white;
            text-align: center;
            padding: 20px;
        }

        @media (max-width: 600px) {
            header {
                flex-direction: column;
            }

            nav a {
                margin: 0 6px;
            }

            .hero h2 {
                font-size: 28px;
            }
        }
    </style>
</head>

<body>
    <header>
        <h1>Campus Clubs</h1>

        <nav aria-label="Main navigation">
            <a href="#home">Home</a>
            <a href="#clubs">Clubs</a>
            <a href="#events">Events</a>
            <a href="#register">Register</a>
        </nav>
    </header>

    <main>
        <section class="hero" id="home">
            <h2>Discover Your Campus Community</h2>
            <p>Explore your interests, learn new skills, and
               participate in college activities.</p>
            <a class="btn" href="#clubs">Explore Clubs</a>
        </section>

        <section id="clubs">
            <h2>Our Clubs</h2>

            <div class="cards">
                <article class="card">
                    <h3>💻 Coding Club</h3>
                    <p>Learn programming, web development,
                       and problem-solving.</p>
                    <button class="btn choose-club"
                            data-club="Coding Club">
                        Join Interest List
                    </button>
                </article>

                <article class="card">
                    <h3>📸 Photography Club</h3>
                    <p>Explore photography, creativity,
                       and visual storytelling.</p>
                    <button class="btn choose-club"
                            data-club="Photography Club">
                        Join Interest List
                    </button>
                </article>

                <article class="card">
                    <h3>🎭 Cultural Club</h3>
                    <p>Participate in cultural programs,
                       music, and performances.</p>
                    <button class="btn choose-club"
                            data-club="Cultural Club">
                        Join Interest List
                    </button>
                </article>
            </div>
        </section>

        <section id="events">
            <h2>Upcoming Events</h2>

            <div class="cards">
                <article class="card">
                    <h3>Web Development Workshop</h3>
                    <p>Learn the basics of HTML, CSS,
                       and JavaScript.</p>
                    <p><strong>Date:</strong> To be announced</p>
                </article>

                <article class="card">
                    <h3>Photography Exhibition</h3>
                    <p>Showcase creative photographs
                       and visual projects.</p>
                    <p><strong>Date:</strong> To be announced</p>
                </article>

                <article class="card">
                    <h3>Cultural Fest</h3>
                    <p>Celebrate student talent through
                       performances and activities.</p>
                    <p><strong>Date:</strong> To be announced</p>
                </article>
            </div>
        </section>

        <section id="register">
            <h2>Club Interest Registration</h2>

            <form id="registrationForm">
                <label for="studentName">Student Name</label>
                <input id="studentName" name="studentName"
                       type="text" required
                       placeholder="Enter your name">

                <label for="email">Email Address</label>
                <input id="email" name="email"
                       type="email" required
                       placeholder="Enter your email">

                <label for="club">Select a Club</label>
                <select id="club" name="club" required>
                    <option value="">Choose a club</option>
                    <option value="Coding Club">Coding Club</option>
                    <option value="Photography Club">
                        Photography Club
                    </option>
                    <option value="Cultural Club">Cultural Club</option>
                </select>

                <button class="btn" type="submit">
                    Submit Registration
                </button>

                <p id="message" role="status"
                   aria-live="polite"></p>
            </form>
        </section>
    </main>

    <footer>
        <p>© 2026 College Club Portal |
           Student Club Activities</p>
    </footer>

    <script>
        const form = document.getElementById(
            "registrationForm"
        );

        const message = document.getElementById("message");
        const clubSelect = document.getElementById("club");

        document.querySelectorAll(".choose-club")
            .forEach(function(button) {
                button.addEventListener("click", function() {
                    clubSelect.value = button.dataset.club;

                    document.getElementById("register")
                        .scrollIntoView({ behavior: "smooth" });

                    document.getElementById("studentName").focus();
                });
            });

        form.addEventListener("submit", function(event) {
            event.preventDefault();

            if (!form.checkValidity()) {
                form.reportValidity();
                return;
            }

            const name = document.getElementById(
                "studentName"
            ).value.trim();

            const club = clubSelect.value;

            if (!name) {
                message.textContent =
                    "Please enter a valid student name.";
                return;
            }

            message.textContent =
                "Thank you, " + name +
                "! Your interest in " + club +
                " has been recorded for this session.";

            form.reset();
        });
    </script>
</body>
</html>
