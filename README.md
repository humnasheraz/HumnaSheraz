<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Humna Sheraz | CV</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #eef2f5;
            font-family: 'Segoe UI', 'Poppins', 'Roboto', sans-serif;
            padding: 40px 20px;
            display: flex;
            justify-content: center;
        }

        /* Main CV Container */
        .cv-card {
            max-width: 1100px;
            width: 100%;
            background: white;
            border-radius: 28px;
            box-shadow: 0 25px 45px -12px rgba(0, 0, 0, 0.25);
            overflow: hidden;
            transition: all 0.3s ease;
        }

        /* Header Section with Gradient */
        .header {
            background: linear-gradient(135deg, #1e3c4c 0%, #2a5f6e 100%);
            color: white;
            padding: 40px 45px 35px 45px;
            text-align: center;
        }

        .header h1 {
            font-size: 48px;
            font-weight: 600;
            letter-spacing: 2px;
            margin-bottom: 8px;
            word-break: keep-all;
        }

        .header .tagline {
            font-size: 18px;
            font-weight: 400;
            opacity: 0.9;
            margin-bottom: 20px;
            letter-spacing: 1px;
        }

        .header .contact-bar {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            font-size: 14px;
            background: rgba(255,255,255,0.12);
            padding: 12px 20px;
            border-radius: 50px;
            width: fit-content;
            margin: 0 auto;
        }

        .header .contact-bar span {
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        /* Container for inner content */
        .content {
            padding: 35px 40px 45px 40px;
        }

        /* Section styling */
        .section {
            margin-bottom: 38px;
        }

        .section-title {
            font-size: 22px;
            font-weight: 700;
            color: #1e3c4c;
            border-left: 5px solid #2a8b7c;
            padding-left: 16px;
            margin-bottom: 20px;
            letter-spacing: -0.2px;
        }

        /* Quote / About box */
        .about-box {
            background: #f4f9fc;
            padding: 20px 28px;
            border-radius: 20px;
            margin-bottom: 10px;
            border: 1px solid #e0edf2;
        }

        .about-text {
            font-size: 16px;
            line-height: 1.6;
            color: #2c3e3f;
            font-style: italic;
            margin-bottom: 15px;
        }

        .pill-container {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 12px;
        }

        .pill {
            background: white;
            border: 1px solid #c7dfe6;
            padding: 6px 16px;
            border-radius: 40px;
            font-size: 13px;
            font-weight: 500;
            color: #1e5f6b;
            box-shadow: 0 1px 2px rgba(0,0,0,0.02);
        }

        /* Education Table/Card */
        .edu-grid {
            display: flex;
            flex-direction: column;
            gap: 14px;
        }

        .edu-item {
            background: #fefefe;
            border-radius: 18px;
            padding: 16px 22px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.03);
            border: 1px solid #e9f0f3;
            transition: 0.2s;
        }

        .edu-degree {
            font-weight: 700;
            font-size: 17px;
            color: #1a4b5a;
        }

        .edu-detail {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            margin-top: 6px;
            color: #4e6b71;
            font-size: 14px;
        }

        /* Projects Grid (2 columns) */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }

        .project-card {
            background: #ffffff;
            border-radius: 20px;
            padding: 18px;
            border: 1px solid #e2edf2;
            transition: all 0.25s;
            box-shadow: 0 6px 12px -8px rgba(0,0,0,0.05);
        }

        .project-card:hover {
            transform: translateY(-3px);
            border-color: #bcdfe8;
            box-shadow: 0 12px 22px -12px rgba(0,0,0,0.12);
        }

        .project-title {
            font-weight: 800;
            font-size: 17px;
            color: #1d5a64;
            margin-bottom: 10px;
            display: flex;
            justify-content: space-between;
        }

        .progress-bar-bg {
            background: #e1f0f3;
            border-radius: 12px;
            height: 8px;
            width: 100%;
            margin: 12px 0 10px;
        }

        .progress-fill {
            background: #2f8b7c;
            width: 75%;
            height: 8px;
            border-radius: 12px;
        }

        .tech-stack {
            font-size: 12px;
            color: #52828c;
            margin: 10px 0 5px;
            font-weight: 500;
        }

        .role {
            font-size: 13px;
            color: #3f6f7a;
        }

        /* Experience flex row */
        .exp-row {
            display: flex;
            gap: 25px;
            flex-wrap: wrap;
        }

        .exp-card {
            flex: 1;
            background: #ffffff;
            border: 1px solid #e2edf2;
            border-radius: 24px;
            padding: 20px;
            box-shadow: 0 6px 14px rgba(0, 0, 0, 0.02);
        }

        .exp-title {
            font-size: 18px;
            font-weight: 800;
            color: #1e4e5a;
            margin-bottom: 12px;
            border-bottom: 2px dashed #cae1e8;
            display: inline-block;
            padding-bottom: 5px;
        }

        .exp-list {
            list-style: none;
            margin: 15px 0;
        }

        .exp-list li {
            margin-bottom: 8px;
            padding-left: 20px;
            position: relative;
            font-size: 14px;
            color: #2b595f;
        }

        .exp-list li::before {
            content: "▹";
            position: absolute;
            left: 0;
            color: #308074;
        }

        .progress-stats {
            margin-top: 15px;
            font-weight: 500;
            font-size: 13px;
            color: #1c6e68;
        }

        /* skills */
        .skill-block {
            background: #fafeff;
            border-radius: 20px;
            padding: 8px 0;
        }

        .skill-item {
            margin-bottom: 20px;
        }

        .skill-label {
            font-weight: 700;
            font-size: 15px;
            color: #1a5f68;
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
        }

        .skill-bar-bg {
            background: #e2edf0;
            border-radius: 14px;
            height: 10px;
            overflow: hidden;
        }

        .skill-bar-fill {
            background: #2f8b7c;
            height: 10px;
            border-radius: 14px;
            width: 0%;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 8px;
        }

        .skill-tag {
            background: #e4f1f5;
            padding: 4px 12px;
            border-radius: 30px;
            font-size: 12px;
            font-weight: 500;
            color: #18616b;
        }

        .two-columns {
            display: flex;
            gap: 30px;
            flex-wrap: wrap;
        }

        .col {
            flex: 1;
        }

        .vol-card {
            background: #f9fdfe;
            border-left: 4px solid #2f8b7c;
            padding: 15px 18px;
            margin-bottom: 16px;
            border-radius: 16px;
        }

        .vol-title {
            font-weight: 800;
            font-size: 16px;
        }

        hr {
            margin: 25px 0 15px;
            border: 0;
            height: 1px;
            background: linear-gradient(to right, #cbdbe0, transparent);
        }

        .footer-note {
            text-align: center;
            margin-top: 30px;
            font-size: 12px;
            color: #95b7c0;
            border-top: 1px solid #e2edf2;
            padding-top: 20px;
        }
    </style>
</head>
<body>
<div class="cv-card">
    <!-- HEADER with gradient & clean spacing -->
    <div class="header">
        <h1>HUMMA SHE RAZ</h1>
        <div class="tagline">Computer Science Undergraduate | Project Manager | Programmer | Small Business Owner</div>
        <div class="contact-bar">
            <span>📍 Islamabad, Pakistan</span>
            <span>✉️ humnasheraz36@gmail.com</span>
            <span>🎓 FJWU (2024–2028)</span>
        </div>
    </div>

    <div class="content">
        <!-- ABOUT SECTION / modern quote -->
        <div class="section">
            <div class="section-title">About Me</div>
            <div class="about-box">
                <div class="about-text">“Blending logic with leadership, and tech with heart.”</div>
                <div class="pill-container">
                    <span class="pill">4th semester BS CS</span>
                    <span class="pill">Project-based thinker</span>
                    <span class="pill">Aspiring Technical Project Manager</span>
                </div>
                <div style="margin-top: 15px; font-size: 14px; color: #2e6f79;">
                    ➤ I turn ideas into structured projects — from code to community drives to small business operations.
                </div>
            </div>
        </div>

        <!-- EDUCATION SECTION -->
        <div class="section">
            <div class="section-title">Education</div>
            <div class="edu-grid">
                <div class="edu-item">
                    <div class="edu-degree">BS Computer Science (4th Semester)</div>
                    <div class="edu-detail"><span>Fatima Jinnah Women University</span><span class="pill" style="background:#e7f2f5;">In Progress</span></div>
                </div>
                <div class="edu-item">
                    <div class="edu-degree">FSC (ICS) | APS Humayun</div>
                    <div class="edu-detail"><span>A+ in Computer Science</span><span>77% overall</span></div>
                </div>
                <div class="edu-item">
                    <div class="edu-degree">Matriculation (Science) | Sunrise School</div>
                    <div class="edu-detail"><span>A+ Grade</span><span>86% overall</span></div>
                </div>
            </div>
        </div>

        <!-- PROJECTS - Grid with interactive bars -->
        <div class="section">
            <div class="section-title">Technical Projects</div>
            <div class="projects-grid">
                <div class="project-card"><div class="project-title">Automatic Pet Feeder</div><div class="progress-bar-bg"><div class="progress-fill" style="width:80%"></div></div><div class="tech-stack">Arduino · Blynk · HTML</div><div class="role">Role: Project Lead</div></div>
                <div class="project-card"><div class="project-title">Hangman Game</div><div class="progress-bar-bg"><div class="progress-fill" style="width:95%"></div></div><div class="tech-stack">C / C++</div><div class="role">Role: Developer</div></div>
                <div class="project-card"><div class="project-title">Banking System</div><div class="progress-bar-bg"><div class="progress-fill" style="width:88%"></div></div><div class="tech-stack">C / C++</div><div class="role">Role: Solo Developer</div></div>
                <div class="project-card"><div class="project-title">Library Management</div><div class="progress-bar-bg"><div class="progress-fill" style="width:85%"></div></div><div class="tech-stack">Java + SQL</div><div class="role">Role: Designer/Tester</div></div>
                <div class="project-card"><div class="project-title">Virtual Machine System</div><div class="progress-bar-bg"><div class="progress-fill" style="width:78%"></div></div><div class="tech-stack">Computer Networks</div><div class="role">Role: Team Coordinator</div></div>
                <div class="project-card"><div class="project-title">Encryption Tool</div><div class="progress-bar-bg"><div class="progress-fill" style="width:82%"></div></div><div class="tech-stack">Assembly + GUI</div><div class="role">Role: Developer</div></div>
            </div>
        </div>

        <!-- EXPERIENCE row style -->
        <div class="section">
            <div class="section-title">Experience</div>
            <div class="exp-row">
                <div class="exp-card">
                    <div class="exp-title">Small Business Owner (Baking)</div>
                    <ul class="exp-list">
                        <li>Instagram bakery management</li>
                        <li>Customer service & order lifecycle</li>
                        <li>Marketing, pricing & delivery timelines</li>
                    </ul>
                    <div class="progress-stats">📊 Efficiency: ▰▰▰▰▰▰▰▰▰▰ 85%</div>
                </div>
                <div class="exp-card">
                    <div class="exp-title">Home Tutor</div>
                    <ul class="exp-list">
                        <li>Personalized academic coaching</li>
                        <li>Lesson planning & progress tracking</li>
                        <li>Exam preparation & adaptive scope</li>
                    </ul>
                    <div class="progress-stats">📊 Student success: ▰▰▰▰▰▰▰▰▰▰ 92%</div>
                </div>
            </div>
        </div>

        <!-- VOLUNTEER & LEADERSHIP -->
        <div class="section">
            <div class="section-title">Volunteer Projects</div>
            <div class="vol-card">
                <div class="vol-title">Ayub National Park Cleanliness Drive — Co-Lead</div>
                <div style="font-size:13px; margin-top: 8px;">✔ Coordinated 15+ volunteers, managed supplies & schedule, created community impact.</div>
            </div>
            <div class="vol-card">
                <div class="vol-title">Community Awareness Programs — Organizer</div>
                <div style="font-size:13px; margin-top: 8px;">✔ Scheduled sessions, speaker coordination, feedback collection and outreach.</div>
            </div>
        </div>

        <!-- SKILLS with visual bars & tags -->
        <div class="section">
            <div class="section-title">Skills</div>
            <div class="skill-block">
                <div class="skill-item"><div class="skill-label">Project Management <span>85%</span></div><div class="skill-bar-bg"><div class="skill-bar-fill" style="width:85%"></div></div><div class="skill-tags"><span class="skill-tag">Planning</span><span class="skill-tag">Task Breakdown</span><span class="skill-tag">Monitoring</span><span class="skill-tag">Risk Awareness</span></div></div>
                <div class="skill-item"><div class="skill-label">Programming <span>90%</span></div><div class="skill-bar-bg"><div class="skill-bar-fill" style="width:90%"></div></div><div class="skill-tags"><span class="skill-tag">C</span><span class="skill-tag">C++</span><span class="skill-tag">Java</span><span class="skill-tag">SQL</span><span class="skill-tag">HTML/CSS</span><span class="skill-tag">Assembly</span></div></div>
                <div class="skill-item"><div class="skill-label">Business & Marketing <span>80%</span></div><div class="skill-bar-bg"><div class="skill-bar-fill" style="width:80%"></div></div><div class="skill-tags"><span class="skill-tag">Instagram Growth</span><span class="skill-tag">Customer Engagement</span><span class="skill-tag">Pricing</span></div></div>
                <div class="skill-item"><div class="skill-label">Soft Skills <span>92%</span></div><div class="skill-bar-bg"><div class="skill-bar-fill" style="width:92%"></div></div><div class="skill-tags"><span class="skill-tag">Communication</span><span class="skill-tag">Leadership</span><span class="skill-tag">Teamwork</span><span class="skill-tag">Problem Solving</span></div></div>
            </div>
        </div>

        <!-- CERTIFICATES & AWARDS -->
        <div class="section">
            <div class="section-title">Certificates & Awards</div>
            <div style="display: flex; flex-wrap: wrap; gap: 15px;">
                <div class="pill" style="background:#eef3f7;">✓ Google Project Management Professional Certificate</div>
                <div class="pill" style="background:#eef3f7;">🏅 6 Academic Awards</div>
                <div class="pill" style="background:#eef3f7;">⭐ 9 Participation Awards</div>
            </div>
        </div>

        <!-- CAREER GOAL -->
        <div class="section">
            <div class="section-title">Career Goal</div>
            <div class="about-box" style="background: #f9fbfc;">
                To build a strong career in Project Management, applying leadership, organizational, and problem-solving skills to successfully deliver projects. Aim to contribute to impactful initiatives while empowering teams through planning and innovation.
            </div>
        </div>

        <div class="footer-note">
            🌟 Plan it. Build it. Lead it. — Humna Sheraz
        </div>
    </div>
</div>
</body>
</html>
