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
            font-family: 'Segoe UI', 'Roboto', sans-serif;
            padding: 40px 20px;
            display: flex;
            justify-content: center;
        }

        .cv-card {
            max-width: 1100px;
            width: 100%;
            background: white;
            border-radius: 28px;
            box-shadow: 0 25px 45px -12px rgba(0, 0, 0, 0.25);
            overflow: hidden;
        }

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
        }

        .header .tagline {
            font-size: 18px;
            font-weight: 400;
            opacity: 0.9;
            margin-bottom: 20px;
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

        .content {
            padding: 35px 40px 45px 40px;
        }

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
        }

        .about-box {
            background: #f4f9fc;
            padding: 20px 28px;
            border-radius: 20px;
            border: 1px solid #e0edf2;
        }

        .about-text {
            font-size: 16px;
            line-height: 1.6;
            color: #2c3e3f;
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
        }

        .info-row {
            display: flex;
            gap: 30px;
            margin-top: 10px;
            flex-wrap: wrap;
        }

        .info-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 14px;
            color: #2c5a62;
        }

        .edu-grid {
            display: flex;
            flex-direction: column;
            gap: 14px;
        }

        .edu-item {
            background: #fefefe;
            border-radius: 18px;
            padding: 16px 22px;
            border: 1px solid #e9f0f3;
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
            margin-bottom: 8px;
        }

        .tech-stack {
            font-size: 12px;
            color: #52828c;
            margin: 8px 0 5px;
            font-weight: 500;
        }

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
        }

        .exp-title {
            font-size: 18px;
            font-weight: 800;
            color: #1e4e5a;
            margin-bottom: 12px;
            border-bottom: 2px dashed #cae1e8;
            padding-bottom: 5px;
            display: inline-block;
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
            color: #1a4b5a;
        }

        .cert-container {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }

        .cert-pill {
            background: #eef3f7;
            border: 1px solid #c7dfe6;
            padding: 8px 18px;
            border-radius: 40px;
            font-size: 13px;
            font-weight: 500;
            color: #1e5f6b;
        }

        .career-goal-box {
            background: #f4f9fc;
            padding: 20px 28px;
            border-radius: 20px;
            border: 1px solid #e0edf2;
            font-size: 15px;
            line-height: 1.7;
            color: #2c5a62;
        }

        .footer-note {
            text-align: center;
            margin-top: 30px;
            font-size: 12px;
            color: #95b7c0;
            border-top: 1px solid #e2edf2;
            padding-top: 20px;
        }

        @media (max-width: 700px) {
            .projects-grid {
                grid-template-columns: 1fr;
            }
            .content {
                padding: 25px;
            }
            .header h1 {
                font-size: 32px;
            }
        }
    </style>
</head>
<body>
<div class="cv-card">
    <div class="header">
        <h1>HUMMA SHE RAZ</h1>
        <div class="tagline">Computer Science Undergraduate | Project Manager | Programmer | Small Business Owner</div>
        <div class="contact-bar">
            <span>Islamabad, Pakistan</span>
            <span>humnasheraz36@gmail.com</span>
            <span>FJWU (2024-2028)</span>
        </div>
    </div>

    <div class="content">
        <!-- About Me -->
        <div class="section">
            <div class="section-title">About Me</div>
            <div class="about-box">
                <div class="about-text">I am a dedicated BS Computer Science student at Fatima Jinnah Women University (currently in my 4th semester). My experience ranges from coding in C++, Java, and Assembly Language to running a successful Instagram-based baking business and leading community volunteer initiatives like the Ayub National Park Cleanliness Drive. I believe in blending logic with leadership, and tech with heart.</div>
                <div class="pill-container">
                    <span class="pill">4th Semester BS CS</span>
                    <span class="pill">Project Manager</span>
                    <span class="pill">Aspiring Technical Project Manager</span>
                </div>
            </div>
        </div>

        <!-- Education -->
        <div class="section">
            <div class="section-title">Education</div>
            <div class="edu-grid">
                <div class="edu-item">
                    <div class="edu-degree">BS Computer Science (4th Semester)</div>
                    <div class="edu-detail"><span>Fatima Jinnah Women University, Rawalpindi</span><span class="pill" style="background:#e7f2f5;">Currently enrolled</span></div>
                </div>
                <div class="edu-item">
                    <div class="edu-degree">FSC (ICS) | APS Humayun</div>
                    <div class="edu-detail"><span>A+ in Computer Science</span><span>77% overall</span></div>
                </div>
                <div class="edu-item">
                    <div class="edu-degree">Matriculation (Science) | Sunrise School</div>
                    <div class="edu-detail"><span>A+</span><span>86% overall</span></div>
                </div>
            </div>
        </div>

        <!-- Academic Projects -->
        <div class="section">
            <div class="section-title">Academic Projects</div>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-title">Automatic Pet Feeder</div>
                    <div class="tech-stack">Arduino, Blynk, C-style & HTML</div>
                </div>
                <div class="project-card">
                    <div class="project-title">Hangman Game</div>
                    <div class="tech-stack">C / C++</div>
                </div>
                <div class="project-card">
                    <div class="project-title">Banking System</div>
                    <div class="tech-stack">C / C++</div>
                </div>
                <div class="project-card">
                    <div class="project-title">Library Management System</div>
                    <div class="tech-stack">Java + SQL database</div>
                </div>
                <div class="project-card">
                    <div class="project-title">Virtual Machine System</div>
                    <div class="tech-stack">Computer Networks</div>
                </div>
                <div class="project-card">
                    <div class="project-title">Obscure Binary Search Tree</div>
                    <div class="tech-stack">C++</div>
                </div>
                <div class="project-card">
                    <div class="project-title">Simple Encryption Description</div>
                    <div class="tech-stack">Assembly Language + GUI</div>
                </div>
            </div>
        </div>

        <!-- Work Experience -->
        <div class="section">
            <div class="section-title">Work Experience</div>
            <div class="exp-row">
                <div class="exp-card">
                    <div class="exp-title">Home Tutor</div>
                    <ul class="exp-list">
                        <li>Personalized academic support for students</li>
                        <li>Custom lesson planning and progress tracking</li>
                        <li>Exam preparation and adaptive teaching</li>
                    </ul>
                </div>
                <div class="exp-card">
                    <div class="exp-title">Small Business Owner (Baking)</div>
                    <ul class="exp-list">
                        <li>Managed an Instagram-based online bakery</li>
                        <li>Customer service and order management</li>
                        <li>Marketing, pricing and delivery timelines</li>
                        <li>Time management and business operations</li>
                    </ul>
                </div>
            </div>
        </div>

        <!-- Volunteer Experience -->
        <div class="section">
            <div class="section-title">Volunteer Experience</div>
            <div class="vol-card">
                <div class="vol-title">Ayub National Park Cleanliness Drive</div>
                <div style="font-size:13px; margin-top: 8px;">Led community cleanup initiative, coordinated volunteers, managed supplies and schedule.</div>
            </div>
            <div class="vol-card">
                <div class="vol-title">Awareness Programs & Community Development Initiatives</div>
                <div style="font-size:13px; margin-top: 8px;">Organized sessions, coordinated speakers, collected feedback and managed outreach.</div>
            </div>
        </div>

        <!-- Skills -->
        <div class="section">
            <div class="section-title">Skills</div>
            <div class="skill-block">
                <div class="skill-item">
                    <div class="skill-label">Project Management</div>
                    <div class="skill-tags"><span class="skill-tag">Planning</span><span class="skill-tag">Organizing</span><span class="skill-tag">Monitoring</span></div>
                </div>
                <div class="skill-item">
                    <div class="skill-label">Programming</div>
                    <div class="skill-tags"><span class="skill-tag">C</span><span class="skill-tag">C++</span><span class="skill-tag">Java</span><span class="skill-tag">SQL</span><span class="skill-tag">HTML/CSS</span><span class="skill-tag">Assembly</span></div>
                </div>
                <div class="skill-item">
                    <div class="skill-label">Business & Marketing</div>
                    <div class="skill-tags"><span class="skill-tag">Instagram Growth</span><span class="skill-tag">Customer Engagement</span></div>
                </div>
                <div class="skill-item">
                    <div class="skill-label">Soft Skills</div>
                    <div class="skill-tags"><span class="skill-tag">Communication</span><span class="skill-tag">Leadership</span><span class="skill-tag">Teamwork</span><span class="skill-tag">Problem Solving</span><span class="skill-tag">Time Management</span></div>
                </div>
            </div>
        </div>

        <!-- Certificates & Awards -->
        <div class="section">
            <div class="section-title">Certificates & Awards</div>
            <div class="cert-container">
                <span class="cert-pill">Google Project Management Professional Certificate</span>
                <span class="cert-pill">6 Academic Awards - Outstanding performance in studies</span>
                <span class="cert-pill">9 Participation Awards - Extracurriculars & events</span>
            </div>
        </div>

        <!-- Career Goal -->
        <div class="section">
            <div class="section-title">Career Goal</div>
            <div class="career-goal-box">
                To build a strong career in Project Management, applying leadership, organizational, and problem-solving skills to successfully deliver projects. Aim to contribute to impactful projects while empowering others through teamwork, planning, and innovation.
            </div>
        </div>

        <div class="footer-note">
            Professional portfolio showcasing my journey in Computer Science at Fatima Jinnah Women University (2024-2028)
        </div>
    </div>
</div>
</body>
</html>
