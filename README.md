<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mr-Infect | Cybersecurity Engineer</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.0.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;500;600;700&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --neon-green: #00ff41;
            --dark-bg: #0a0a0a;
            --darker-bg: #050505;
            --dark-accent: #1a1a1a;
            --terminal-green: #33ff33;
        }
        
        body {
            background-color: var(--dark-bg);
            color: #e0e0e0;
            font-family: 'Fira Code', monospace;
            line-height: 1.6;
            margin: 0;
            padding: 0;
        }
        
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        .terminal-header {
            font-family: 'Space Mono', monospace;
            border: 1px solid var(--neon-green);
            padding: 1rem;
            background-color: var(--darker-bg);
            border-radius: 8px;
            box-shadow: 0 0 15px rgba(0, 255, 65, 0.3);
            margin-bottom: 2rem;
            position: relative;
            overflow: hidden;
        }
        
        .terminal-buttons {
            position: absolute;
            top: 10px;
            left: 10px;
            display: flex;
            gap: 8px;
        }
        
        .terminal-button {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }
        
        .red { background-color: #ff5f56; }
        .yellow { background-color: #ffbd2e; }
        .green { background-color: #27c93f; }
        
        .typewriter {
            overflow: hidden;
            border-right: .15em solid var(--neon-green);
            white-space: nowrap;
            margin: 0 auto;
            letter-spacing: .15em;
            animation: typing 3.5s steps(40, end), blink-caret .75s step-end infinite;
        }
        
        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }
        
        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: var(--neon-green); }
        }
        
        .terminal-text {
            color: var(--terminal-green);
            padding: 1rem 0 0 0;
            font-size: 1.1rem;
        }
        
        .terminal-window {
            background-color: var(--darker-bg);
            padding: 1.5rem;
            border-radius: 8px;
            border: 1px solid #333;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
            margin-bottom: 2rem;
        }
        
        .section-title {
            border-bottom: 2px solid var(--neon-green);
            padding-bottom: 0.5rem;
            margin-bottom: 1.5rem;
            font-size: 1.6rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .section-title i {
            color: var(--neon-green);
        }
        
        .tech-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 0.75rem;
            margin: 1rem 0;
        }
        
        .tech-badge {
            background-color: var(--dark-accent);
            padding: 0.5rem 0.75rem;
            border-radius: 5px;
            font-size: 0.9rem;
            box-shadow: 0 0 5px rgba(0, 255, 65, 0.2);
            border: 1px solid rgba(51, 255, 51, 0.1);
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .tech-badge:hover {
            transform: translateY(-3px);
            box-shadow: 0 0 10px rgba(0, 255, 65, 0.4);
            border-color: var(--neon-green);
        }
        
        .github-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin: 1.5rem 0;
        }
        
        .github-stat-card {
            border: 1px solid #333;
            border-radius: 8px;
            overflow: hidden;
            background-color: var(--darker-bg);
            transition: transform 0.3s ease;
        }
        
        .github-stat-card:hover {
            transform: scale(1.02);
            border-color: var(--neon-green);
            box-shadow: 0 0 10px rgba(0, 255, 65, 0.3);
        }
        
        .matrix-bg {
            position: relative;
            overflow: hidden;
        }
        
        .matrix-bg::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(rgba(0, 20, 0, 0.8), rgba(0, 20, 0, 0.8)),
                        url('https://cdn.jsdelivr.net/gh/sindresorhus/css-in-readme-like-wat/dino.svg');
            background-size: cover;
            opacity: 0.1;
            z-index: -1;
        }
        
        .skill-category {
            margin-bottom: 1.5rem;
        }
        
        .skill-category-title {
            font-size: 1.2rem;
            color: var(--neon-green);
            margin-bottom: 0.75rem;
            border-left: 3px solid var(--neon-green);
            padding-left: 0.75rem;
        }
        
        .quote-container {
            background-color: var(--darker-bg);
            border-left: 4px solid var(--neon-green);
            padding: 1.5rem;
            margin: 2rem 0;
            position: relative;
            font-style: italic;
        }
        
        .quote-container::before {
            content: """;
            font-family: Georgia, serif;
            font-size: 4rem;
            position: absolute;
            left: 10px;
            top: -10px;
            color: var(--neon-green);
            opacity: 0.3;
        }
        
        .highlight {
            color: var(--neon-green);
            font-weight: bold;
        }
        
        .social-links {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin: 1.5rem 0;
        }
        
        .social-link {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            background-color: var(--dark-accent);
            padding: 0.6rem 1rem;
            border-radius: 5px;
            text-decoration: none;
            color: #e0e0e0;
            transition: all 0.3s ease;
            border: 1px solid transparent;
        }
        
        .social-link:hover {
            transform: translateY(-3px);
            border-color: var(--neon-green);
            box-shadow: 0 0 10px rgba(0, 255, 65, 0.3);
        }
        
        .social-link i {
            font-size: 1.2rem;
        }
        
        .instagram { color: #E4405F; }
        .linkedin { color: #0077B5; }
        .reddit { color: #FF4500; }
        
        .ascii-art {
            font-family: monospace;
            white-space: pre;
            font-size: 0.7rem;
            line-height: 1.1;
            color: var(--neon-green);
            margin: 2rem 0;
            text-align: center;
        }
        
        .divider {
            height: 1px;
            background: linear-gradient(90deg, transparent, var(--neon-green), transparent);
            margin: 2rem 0;
        }
        
        .visitor-counter {
            text-align: center;
            margin: 2rem 0;
            font-size: 0.9rem;
            color: #888;
        }
        
        .typing-text {
            overflow: hidden;
            white-space: nowrap;
            margin: 0;
            animation: typing 4s steps(60, end);
        }
        
        .blinking-cursor {
            animation: blink 1s step-end infinite;
        }
        
        @keyframes blink {
            from, to { color: transparent }
            50% { color: var(--neon-green); }
        }
        
        .profile-section {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 2rem;
            align-items: start;
        }
        
        @media (max-width: 768px) {
            .profile-section {
                grid-template-columns: 1fr;
            }
        }
        
        .profile-image {
            border-radius: 8px;
            border: 2px solid var(--neon-green);
            box-shadow: 0 0 20px rgba(0, 255, 65, 0.4);
            max-width: 100%;
            height: auto;
        }
        
        .glitch-text {
            position: relative;
            font-weight: bold;
            color: white;
            text-shadow: 0.05em 0 0 rgba(255,0,0,.75), 
                        -0.05em -0.025em 0 rgba(0,255,0,.75),
                        0.025em 0.05em 0 rgba(0,0,255,.75);
            animation: glitch 500ms infinite;
        }

        @keyframes glitch {
            0% { text-shadow: 0.05em 0 0 rgba(255,0,0,.75), -0.05em -0.025em 0 rgba(0,255,0,.75), 0.025em 0.05em 0 rgba(0,0,255,.75); }
            14% { text-shadow: 0.05em 0 0 rgba(255,0,0,.75), -0.05em -0.025em 0 rgba(0,255,0,.75), 0.025em 0.05em 0 rgba(0,0,255,.75); }
            15% { text-shadow: -0.05em -0.025em 0 rgba(255,0,0,.75), 0.025em 0.025em 0 rgba(0,255,0,.75), -0.05em -0.05em 0 rgba(0,0,255,.75); }
            49% { text-shadow: -0.05em -0.025em 0 rgba(255,0,0,.75), 0.025em 0.025em 0 rgba(0,255,0,.75), -0.05em -0.05em 0 rgba(0,0,255,.75); }
            50% { text-shadow: 0.025em 0.05em 0 rgba(255,0,0,.75), 0.05em 0 0 rgba(0,255,0,.75), 0 -0.05em 0 rgba(0,0,255,.75); }
            99% { text-shadow: 0.025em 0.05em 0 rgba(255,0,0,.75), 0.05em 0 0 rgba(0,255,0,.75), 0 -0.05em 0 rgba(0,0,255,.75); }
            100% { text-shadow: -0.025em 0 0 rgba(255,0,0,.75), -0.025em -0.025em 0 rgba(0,255,0,.75), -0.025em -0.05em 0 rgba(0,0,255,.75); }
        }
        
        .category-container {
            border: 1px solid #333;
            border-radius: 8px;
            padding: 1rem;
            margin-bottom: 1.5rem;
            background-color: rgba(10, 10, 10, 0.6);
            transition: all 0.3s ease;
        }
        
        .category-container:hover {
            border-color: var(--neon-green);
            box-shadow: 0 0 10px rgba(0, 255, 65, 0.2);
        }
        
        .project-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin: 1.5rem 0;
        }
        
        .project-card {
            border: 1px solid #333;
            border-radius: 8px;
            padding: 1.5rem;
            background-color: var(--darker-bg);
            transition: all 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
            border-color: var(--neon-green);
            box-shadow: 0 0 15px rgba(0, 255, 65, 0.3);
        }
        
        .project-title {
            font-size: 1.2rem;
            color: var(--neon-green);
            margin-bottom: 0.5rem;
        }
        
        .cert-badge {
            display: inline-block;
            padding: 0.3rem 0.6rem;
            margin: 0.25rem;
            border-radius: 4px;
            background-color: var(--dark-accent);
            color: #e0e0e0;
            font-size: 0.85rem;
            border: 1px solid #444;
            transition: all 0.3s ease;
        }
        
        .cert-badge:hover {
            background-color: var(--darker-bg);
            border-color: var(--neon-green);
            transform: scale(1.05);
        }
    </style>
</head>
<body class="matrix-bg">
    <div class="container">
        <!-- Header Section -->
        <div class="terminal-header">
            <div class="terminal-buttons">
                <div class="terminal-button red"></div>
                <div class="terminal-button yellow"></div>
                <div class="terminal-button green"></div>
            </div>
            <div class="terminal-text">
                <span style="color: #33ff33;">root@security:~$</span> whoami
                <h1 class="typewriter mt-4 text-3xl font-bold" style="color: #33ff33;">Mr-Infect</h1>
                <p class="mt-2" style="color: #33ff33;">
                    <span class="typing-text">Cybersecurity Engineer | Malware Analyst | Penetration Tester | VAPT Specialist</span>
                    <span class="blinking-cursor">█</span>
                </p>
            </div>
        </div>

        <!-- ASCII Art -->
        <div class="ascii-art">
           ███╗   ███╗██████╗       ██╗███╗   ██╗███████╗███████╗ ██████╗████████╗
           ████╗ ████║██╔══██╗      ██║████╗  ██║██╔════╝██╔════╝██╔════╝╚══██╔══╝
           ██╔████╔██║██████╔╝█████╗██║██╔██╗ ██║█████╗  █████╗  ██║        ██║   
           ██║╚██╔╝██║██╔══██╗╚════╝██║██║╚██╗██║██╔══╝  ██╔══╝  ██║        ██║   
           ██║ ╚═╝ ██║██║  ██║      ██║██║ ╚████║██║     ███████╗╚██████╗   ██║   
           ╚═╝     ╚═╝╚═╝  ╚═╝      ╚═╝╚═╝  ╚═══╝╚═╝     ╚══════╝ ╚═════╝   ╚═╝   
        </div>

        <!-- About Section -->
        <section class="terminal-window">
            <h2 class="section-title"><i class="fas fa-user-secret"></i> About Me</h2>
            <div class="profile-section">
                <div>
                    <img src="https://cdn.jsdelivr.net/gh/identicons/identicons/mr-infect.png" alt="Mr-Infect" class="profile-image">
                </div>
                <div>
                    <p>
                        <span class="highlight">Self-made Cybersecurity Engineer</span> with expertise in malware analysis, 
                        penetration testing, vulnerability assessment, and security operations. 
                    </p>
                    <p>
                        I've built my career through hands-on experience and continuous learning, proving that formal education 
                        isn't the only path to becoming a skilled security professional. My journey is driven by an insatiable 
                        curiosity about <span class="highlight">WHY?</span> and <span class="highlight">HOW?</span> - the questions that have truly changed our world.
                    </p>
                    <p>
                        With practical experience in security operations, I've earned multiple certifications including 
                        <span class="highlight">CCSA (Check Point Certified Security Administrator)</span> and 
                        <span class="highlight">EEH (Ethical Hacking)</span> while developing expertise in 
                        <span class="highlight">SOC LVL-1</span> operations and <span class="highlight">PJMR</span> methodologies.
                    </p>
                    <p>
                        Known professionally as a <span class="glitch-text">Researcher</span>, I approach cybersecurity with 
                        scientific rigor, examining threats methodically and developing innovative defensive strategies.
                    </p>
                    <p class="font-bold mt-3">
                        Remember: <span class="highlight">"Artificial intelligence is no match for natural STUPIDITY"</span>
                    </p>
                </div>
            </div>
        </section>

        <!-- Certifications Section -->
        <section class="terminal-window">
            <h2 class="section-title"><i class="fas fa-certificate"></i> Certifications & Expertise</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                <div class="category-container">
                    <h3 class="skill-category-title">Professional Certifications</h3>
                    <div class="flex flex-wrap gap-2">
                        <div class="cert-badge">CCSA <i class="fas fa-shield-alt text-yellow-400"></i></div>
                        <div class="cert-badge">EEH <i class="fas fa-bug text-red-400"></i></div>
                        <div class="cert-badge">SOC LVL-1 <i class="fas fa-eye text-blue-400"></i></div>
                        <div class="cert-badge">PJMR <i class="fas fa-project-diagram text-green-400"></i></div>
                        <div class="cert-badge">VAPT Specialist <i class="fas fa-search text-purple-400"></i></div>
                    </div>
                </div>
                
                <div class="category-container">
                    <h3 class="skill-category-title">Core Competencies</h3>
                    <div class="flex flex-wrap gap-2">
                        <div class="cert-badge">Malware Analysis <i class="fas fa-virus text-red-500"></i></div>
                        <div class="cert-badge">Penetration Testing <i class="fas fa-user-ninja text-gray-400"></i></div>
                        <div class="cert-badge">Vulnerability Assessment <i class="fas fa-search-plus text-blue-400"></i></div>
                        <div class="cert-badge">Cloud Security <i class="fas fa-cloud text-blue-300"></i></div>
                        <div class="cert-badge">Programming <i class="fas fa-code text-green-400"></i></div>
                        <div class="cert-badge">Threat Intelligence <i class="fas fa-brain text-purple-400"></i></div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Social Media Section -->
        <section class="terminal-window">
            <h2 class="section-title"><i class="fas fa-globe"></i> Connect With Me</h2>
            <p>Find me across the digital landscape or reach out directly through any of these channels:</p>
            
            <div class="social-links">
                <a href="https://instagram.com/Mr_Infect" target="_blank" class="social-link">
                    <i class="fab fa-instagram instagram"></i>
                    <span>Instagram</span>
                </a>
                
                <a href="https://linkedin.com/in/deepu-a-/" target="_blank" class="social-link">
                    <i class="fab fa-linkedin linkedin"></i>
                    <span>LinkedIn</span>
                </a>
                
                <a href="https://reddit.com/user/khaled1734" target="_blank" class="social-link">
                    <i class="fab fa-reddit reddit"></i>
                    <span>Reddit</span>
                </a>
            </div>
        </section>

        <!-- Tech Stack Section -->
        <section class="terminal-window">
            <h2 class="section-title"><i class="fas fa-laptop-code"></i> Tech Arsenal</h2>
            
            <div class="skill-category">
                <h3 class="skill-category-title">Programming Languages</h3>
                <div class="tech-grid">
                    <div class="tech-badge">
                        <i class="fab fa-java" style="color: #ED8B00;"></i>
                        <span>Java</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fab fa-js" style="color: #F7DF1E;"></i>
                        <span>JavaScript</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fab fa-python" style="color: #3670A0;"></i>
                        <span>Python</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fas fa-code" style="color: #00599C;"></i>
                        <span>C</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fab fa-html5" style="color: #E34F26;"></i>
                        <span>HTML5</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fab fa-css3-alt" style="color: #1572B6;"></i>
                        <span>CSS3</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fas fa-terminal" style="color: #121011;"></i>
                        <span>Shell Script</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fab fa-windows" style="color: #5391FE;"></i>
                        <span>PowerShell</span>
                    </div>
                </div>
            </div>
            
            <div class="skill-category">
                <h3 class="skill-category-title">Cloud Platforms</h3>
                <div class="tech-grid">
                    <div class="tech-badge">
                        <i class="fab fa-aws" style="color: #FF9900;"></i>
                        <span>AWS</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fab fa-microsoft" style="color: #0072C6;"></i>
                        <span>Azure</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fab fa-google" style="color: #4285F4;"></i>
                        <span>Google Cloud</span>
                    </div>
                </div>
            </div>
            
            <div class="skill-category">
                <h3 class="skill-category-title">Frameworks & Libraries</h3>
                <div class="tech-grid">
                    <div class="tech-badge">
                        <i class="fab fa-node-js" style="color: #6DA55F;"></i>
                        <span>Node.js</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fab fa-react" style="color: #61DAFB;"></i>
                        <span>React</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fas fa-flask" style="color: #000;"></i>
                        <span>Flask</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fab fa-npm" style="color: #CB3837;"></i>
                        <span>NPM</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fas fa-camera-retro" style="color: #white;"></i>
                        <span>OpenCV</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fas fa-calculator" style="color: #013243;"></i>
                        <span>NumPy</span>
                    </div>
                </div>
            </div>
            
            <div class="skill-category">
                <h3 class="skill-category-title">Databases</h3>
                <div class="tech-grid">
                    <div class="tech-badge">
                        <i class="fas fa-database" style="color: #4479A1;"></i>
                        <span>MySQL</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fas fa-server" style="color: #CC2927;"></i>
                        <span>Microsoft SQL Server</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fas fa-elephant" style="color: #336791;"></i>
                        <span>PostgreSQL</span>
                    </div>
                </div>
            </div>
            
            <div class="skill-category">
                <h3 class="skill-category-title">DevOps & Tools</h3>
                <div class="tech-grid">
                    <div class="tech-badge">
                        <i class="fab fa-docker" style="color: #0db7ed;"></i>
                        <span>Docker</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fab fa-github-alt" style="color: #2671E5;"></i>
                        <span>GitHub Actions</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fas fa-search" style="color: #005571;"></i>
                        <span>ElasticSearch</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fas fa-chart-line" style="color: #F46800;"></i>
                        <span>Grafana</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fas fa-microchip" style="color: #00979D;"></i>
                        <span>Arduino</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fab fa-raspberry-pi" style="color: #C51A4A;"></i>
                        <span>Raspberry Pi</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fas fa-phone" style="color: #F22F46;"></i>
                        <span>Twilio</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fas fa-mask" style="color: #7E4798;"></i>
                        <span>TOR</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- Projects Section -->
        <section class="terminal-window">
            <h2 class="section-title"><i class="fas fa-project-diagram"></i> Featured Projects</h2>
            <p class="mb-4">Here are some key projects that showcase my expertise in cybersecurity and development:</p>
            
            <div class="project-list">
                <div class="project-card">
                    <h3 class="project-title">Malware Analysis Framework</h3>
                    <p>A custom-built analysis environment for reverse engineering malicious code, utilizing sandboxed execution and automated behavior analysis.</p>
                    <div class="mt-3 text-sm text-gray-400">
                        <span class="mr-2"><i class="fas fa-code-branch"></i> Python</span>
                        <span class="mr-2"><i class="fas fa-vial"></i> Reverse Engineering</span>
                    </div>
                </div>
                
                <div class="project-card">
                    <h3 class="project-title">Cloud Security Posture Monitor</h3>
                    <p>Automated security assessment tool for cloud environments that identifies misconfigurations and compliance violations in AWS/Azure infrastructure.</p>
                    <div class="mt-3 text-sm text-gray-400">
                        <span class="mr-2"><i class="fas fa-cloud"></i> AWS/Azure</span>
                        <span class="mr-2"><i class="fas fa-shield-alt"></i> Compliance</span>
                    </div>
                </div>
                
                <div class="project-card">
                    <h3 class="project-title">IoT Security Assessment Framework</h3>
                    <p>Toolkit for evaluating security of IoT devices, combining hardware analysis with network vulnerability scanning.</p>
                    <div class="mt-3 text-sm text-gray-400">
                        <span class="mr-2"><i class="fas fa-microchip"></i> Hardware</span>
                        <span class="mr-2"><i class="fas fa-network-wired"></i> Network Security</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- GitHub Stats Section -->
        <section class="terminal-window">
            <h2 class="section-title"><i class="fab fa-github"></i> GitHub Activity</h2>
            
            <div class="github-stats">
                <div class="github-stat-card">
                    <img src="https://github-readme-stats.vercel.app/api?username=Mr-Infect&theme=dark&hide_border=true&include_all_commits=true&count_private=true" alt="GitHub Stats" width="100%">
                </div>
                
                <div class="github-stat-card">
                    <img src="https://github-readme-streak-stats.herokuapp.com/?user=Mr-Infect&theme=dark&hide_border=true" alt="GitHub Streak" width="100%">
                </div>
                
                <div class="github-stat-card">
                    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Mr-Infect&theme=dark&hide_border=true&include_all_commits=true&count_private=true&layout=compact" alt="Top Languages" width="100%">
                </div>
            </div>
        </section>
        
        <!-- Quote Section -->
        <div class="quote-container">
            <p class="text-lg">
                <span class="text-2xl" style="color: var(--neon-green);">❝</span>
                <img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=radical" alt="Random Dev Quote" width="100%">
                <span class="text-2xl" style="color: var(--neon-green);">❞</span>
            </p>
        </div>

        <div class="divider"></div>
        
        <!-- Footer Section -->
        <div class="visitor-counter">
            <p>Thanks for stopping by. You're visitor number:</p>
            <img src="https://visitcount.itsvg.in/api?id=Mr-Infect&icon=9&color=0" alt="Visitor Count">
        </div>
        
        <div class="terminal-text text-center mt-6">
            <p>
                <span style="color: #33ff33;">root@security:~$</span> exit
            </p>
            <p class="text-sm mt-2" style="color: #888;">
                Connection to Mr-Infect closed.
            </p>
        </div>
    </div>

    <script>
        // Animation for terminal effects and scrolling matrix background
        document.addEventListener('DOMContentLoaded', function() {
            // Add hover effects and animations
            const techBadges = document.querySelectorAll('.tech-badge');
            
            techBadges.forEach(badge => {
                badge.addEventListener('mouseenter', function() {
                    this.style.transform = 'translateY(-3px)';
                });
                
                badge.addEventListener('mouseleave', function() {
                    this.style.transform = 'translateY(0)';
                });
            });
        });
    </script>
</body>
</html>
