<!DOCTYPE html>
<html>
<head>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&family=Roboto+Mono:wght@300;400&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
            color: #fff;
            min-height: 100vh;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* Animated Header */
        .animated-header {
            text-align: center;
            margin: 30px 0;
            position: relative;
            overflow: hidden;
        }
        
        .marquee-container {
            background: rgba(255, 255, 255, 0.1);
            padding: 15px;
            border-radius: 10px;
            margin-bottom: 20px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .marquee-text {
            font-size: 2.5rem;
            font-weight: 700;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45b7d1, #96ceb4, #feca57);
            background-size: 300% 300%;
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradient 5s ease infinite;
            padding: 10px;
        }
        
        @keyframes gradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        /* Profile Section */
        .profile-section {
            text-align: center;
            padding: 40px 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            margin: 30px 0;
            position: relative;
            overflow: hidden;
        }
        
        .profile-section::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(120, 119, 198, 0.1) 0%, rgba(255, 255, 255, 0) 70%);
            animation: rotate 20s linear infinite;
        }
        
        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        .profile-title {
            font-size: 3rem;
            margin-bottom: 10px;
            position: relative;
            z-index: 2;
        }
        
        .profile-subtitle {
            font-size: 1.8rem;
            color: #4ecdc4;
            margin-bottom: 20px;
            position: relative;
            z-index: 2;
        }
        
        .profile-description {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 30px;
            line-height: 1.6;
            position: relative;
            z-index: 2;
        }
        
        /* Stats Section */
        .stats-container {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin: 30px 0;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.1);
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            min-width: 150px;
            transition: transform 0.3s ease;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .stat-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.15);
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .stat-label {
            font-size: 1rem;
            opacity: 0.8;
        }
        
        /* Skills Section */
        .skills-section {
            margin: 50px 0;
        }
        
        .section-title {
            font-size: 2rem;
            text-align: center;
            margin-bottom: 30px;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(90deg, #ff6b6b, #4ecdc4);
            border-radius: 2px;
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }
        
        .skill-item {
            background: rgba(255, 255, 255, 0.1);
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            transition: all 0.3s ease;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .skill-item:hover {
            transform: scale(1.1);
            background: rgba(255, 255, 255, 0.2);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .skill-icon {
            width: 50px;
            height: 50px;
            margin: 0 auto 10px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .skill-icon img {
            max-width: 100%;
            max-height: 100%;
            filter: drop-shadow(0 0 5px rgba(255, 255, 255, 0.5));
        }
        
        .skill-name {
            font-size: 0.9rem;
            font-weight: 600;
        }
        
        /* Contact Section */
        .contact-section {
            text-align: center;
            margin: 50px 0;
            padding: 40px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        
        .social-link {
            display: inline-block;
            padding: 15px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            transition: all 0.3s ease;
        }
        
        .social-link:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: translateY(-5px) rotate(360deg);
        }
        
        .social-link img {
            width: 30px;
            height: 30px;
        }
        
        /* Quote Section */
        .quote-section {
            text-align: center;
            margin: 40px 0;
            padding: 30px;
            position: relative;
        }
        
        .quote-text {
            font-size: 1.5rem;
            font-style: italic;
            color: #4ecdc4;
            position: relative;
            display: inline-block;
        }
        
        .quote-text::before, .quote-text::after {
            content: '"';
            font-size: 3rem;
            color: #ff6b6b;
            position: absolute;
            top: -20px;
            left: -30px;
        }
        
        .quote-text::after {
            left: auto;
            right: -30px;
            top: auto;
            bottom: -40px;
        }
        
        /* Animation for elements */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .animate-fade-in-up {
            animation: fadeInUp 0.8s ease forwards;
        }
        
        .delay-1 { animation-delay: 0.2s; }
        .delay-2 { animation-delay: 0.4s; }
        .delay-3 { animation-delay: 0.6s; }
        .delay-4 { animation-delay: 0.8s; }
        
        /* Particle Background */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            pointer-events: none;
        }
        
        .particle {
            position: absolute;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            animation: float 20s infinite linear;
        }
        
        @keyframes float {
            0% {
                transform: translateY(100vh) translateX(0) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100px) translateX(100px) rotate(360deg);
                opacity: 0;
            }
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .profile-title { font-size: 2rem; }
            .profile-subtitle { font-size: 1.3rem; }
            .stats-container { flex-direction: column; align-items: center; }
            .stat-card { width: 80%; }
            .skills-grid { grid-template-columns: repeat(auto-fill, minmax(100px, 1fr)); }
        }
    </style>
</head>
<body>
    <!-- Particle Background -->
    <div class="particles" id="particles"></div>
    
    <div class="container">
        <!-- Animated Header -->
        <div class="animated-header">
            <div class="marquee-container">
                <div class="marquee-text">Prajwal Ghotkar</div>
            </div>
            
            <div class="logo-container">
                <img src="https://images.squarespace-cdn.com/content/v1/5eea681ba10cc5139559fcca/99933882-3dea-4096-a207-835d29abc1e6/Humans+vs+AI.png?format=1500w" 
                     alt="Humans vs AI Logo" 
                     style="max-width: 300px; margin: 20px auto; display: block; border-radius: 10px; box-shadow: 0 10px 30px rgba(0,0,0,0.3);">
            </div>
        </div>
        
        <!-- Profile Section -->
        <section class="profile-section animate-fade-in-up">
            <h1 class="profile-title">Hi 👋, I'm Prajwal Ghotkar</h1>
            <h2 class="profile-subtitle">Data Analysis World</h2>
            <p class="profile-description">
                🌟 Welcome to my corner of the coding universe! 🌟<br>
                I'm passionate about transforming raw data into meaningful insights and building intelligent solutions.
            </p>
            
            <!-- Stats Section -->
            <div class="stats-container">
                <div class="stat-card animate-fade-in-up delay-1">
                    <div class="stat-number" id="github-views">0</div>
                    <div class="stat-label">Profile Views</div>
                </div>
                <div class="stat-card animate-fade-in-up delay-2">
                    <div class="stat-number">10+</div>
                    <div class="stat-label">Tools & Technologies</div>
                </div>
                <div class="stat-card animate-fade-in-up delay-3">
                    <div class="stat-number">24/7</div>
                    <div class="stat-label">Learning Mode</div>
                </div>
            </div>
        </section>
        
        <!-- About Section -->
        <section class="profile-section animate-fade-in-up delay-2">
            <h2 class="section-title">About Me</h2>
            <div class="profile-description">
                <p>🌱 I'm currently exploring Data Science and working to become proficient in it.</p>
                <p>💬 Ask me about Python | SQL | NumPy | Pandas | Matplotlib | Seaborn | scikit-learn | Machine Learning | FastAPI | Pydantic | OpenCV | Tableau | Power BI</p>
                <p>📫 How to reach me: <strong>pmghotkar05@gmail.com</strong></p>
                <p class="quote-text">The world is one big data problem 📊👨🏻‍💻</p>
            </div>
        </section>
        
        <!-- Skills Section -->
        <section class="skills-section animate-fade-in-up delay-3">
            <h2 class="section-title">Languages & Tools</h2>
            <div class="skills-grid">
                <!-- Python -->
                <div class="skill-item">
                    <div class="skill-icon">
                        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="Python">
                    </div>
                    <div class="skill-name">Python</div>
                </div>
                
                <!-- NumPy -->
                <div class="skill-item">
                    <div class="skill-icon">
                        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/numpy/numpy-original.svg" alt="NumPy">
                    </div>
                    <div class="skill-name">NumPy</div>
                </div>
                
                <!-- Pandas -->
                <div class="skill-item">
                    <div class="skill-icon">
                        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/pandas/pandas-original.svg" alt="Pandas">
                    </div>
                    <div class="skill-name">Pandas</div>
                </div>
                
                <!-- Matplotlib -->
                <div class="skill-item">
                    <div class="skill-icon">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/8/84/Matplotlib_icon.svg" alt="Matplotlib">
                    </div>
                    <div class="skill-name">Matplotlib</div>
                </div>
                
                <!-- Seaborn -->
                <div class="skill-item">
                    <div class="skill-icon">
                        <img src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" alt="Seaborn">
                    </div>
                    <div class="skill-name">Seaborn</div>
                </div>
                
                <!-- Scikit-learn -->
                <div class="skill-item">
                    <div class="skill-icon">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="Scikit-learn">
                    </div>
                    <div class="skill-name">Scikit-learn</div>
                </div>
                
                <!-- SQL -->
                <div class="skill-item">
                    <div class="skill-icon">
                        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original.svg" alt="SQL">
                    </div>
                    <div class="skill-name">SQL</div>
                </div>
                
                <!-- Power BI -->
                <div class="skill-item">
                    <div class="skill-icon">
                        <img src="https://raw.githubusercontent.com/microsoft/PowerBI-Icons/main/SVG/Power-BI.svg" alt="Power BI">
                    </div>
                    <div class="skill-name">Power BI</div>
                </div>
                
                <!-- Tableau -->
                <div class="skill-item">
                    <div class="skill-icon">
                        <img src="https://cdn.worldvectorlogo.com/logos/tableau-software.svg" alt="Tableau">
                    </div>
                    <div class="skill-name">Tableau</div>
                </div>
                
                <!-- OpenCV -->
                <div class="skill-item">
                    <div class="skill-icon">
                        <img src="https://raw.githubusercontent.com/opencv/opencv/master/doc/opencv-logo2.png" alt="OpenCV">
                    </div>
                    <div class="skill-name">OpenCV</div>
                </div>
                
                <!-- FastAPI -->
                <div class="skill-item">
                    <div class="skill-icon">
                        <img src="https://fastapi.tiangolo.com/img/logo-margin/logo-teal.png" alt="FastAPI">
                    </div>
                    <div class="skill-name">FastAPI</div>
                </div>
                
                <!-- Docker -->
                <div class="skill-item">
                    <div class="skill-icon">
                        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original.svg" alt="Docker">
                    </div>
                    <div class="skill-name">Docker</div>
                </div>
            </div>
        </section>
        
        <!-- Contact Section -->
        <section class="contact-section animate-fade-in-up delay-4">
            <h2 class="section-title">Connect With Me</h2>
            <div class="social-links">
                <a href="https://linkedin.com/in/prajwal-ghotkar-9618272a5" target="_blank" class="social-link">
                    <img src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="LinkedIn">
                </a>
                <a href="https://www.instagram.com/invites/contact/?igsh=17hkb01x0fkpr&utm_content=nad16fs" target="_blank" class="social-link">
                    <img src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/instagram.svg" alt="Instagram">
                </a>
                <a href="mailto:pmghotkar05@gmail.com" class="social-link">
                    <img src="https://cdn-icons-png.flaticon.com/512/732/732200.png" alt="Email" style="filter: invert(1);">
                </a>
            </div>
        </section>
        
        <!-- GitHub Stats -->
        <section class="profile-section">
            <h2 class="section-title">GitHub Stats</h2>
            <div style="text-align: center; margin: 30px 0;">
                <img src="https://github-readme-streak-stats-eight.vercel.app/?user=prajwalghotkar&theme=dark&background=0f2027&border=2c5364&stroke=4ecdc4&ring=ff6b6b&fire=ff6b6b&currStreakNum=4ecdc4&sideNums=4ecdc4&currStreakLabel=4ecdc4&sideLabels=4ecdc4&dates=96ceb4" 
                     alt="GitHub Streak Stats"
                     style="border-radius: 10px; max-width: 100%;">
            </div>
        </section>
    </div>

    <script>
        // Create floating particles
        function createParticles() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = 50;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.classList.add('particle');
                
                // Random size
                const size = Math.random() * 10 + 5;
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                
                // Random position
                particle.style.left = `${Math.random() * 100}vw`;
                particle.style.top = `${Math.random() * 100}vh`;
                
                // Random animation delay and duration
                const delay = Math.random() * 20;
                const duration = Math.random() * 10 + 15;
                particle.style.animationDelay = `${delay}s`;
                particle.style.animationDuration = `${duration}s`;
                
                // Random color
                const colors = [
                    'rgba(78, 205, 196, 0.3)',
                    'rgba(255, 107, 107, 0.3)',
                    'rgba(69, 183, 209, 0.3)',
                    'rgba(150, 206, 180, 0.3)',
                    'rgba(254, 202, 87, 0.3)'
                ];
                particle.style.background = colors[Math.floor(Math.random() * colors.length)];
                
                particlesContainer.appendChild(particle);
            }
        }
        
        // Animate counter for stats
        function animateCounter(elementId, finalValue, duration = 2000) {
            const element = document.getElementById(elementId);
            let startValue = 0;
            const increment = finalValue / (duration / 16); // 60fps
            
            const timer = setInterval(() => {
                startValue += increment;
                if (startValue >= finalValue) {
                    element.textContent = finalValue;
                    clearInterval(timer);
                } else {
                    element.textContent = Math.floor(startValue);
                }
            }, 16);
        }
        
        // Initialize when page loads
        document.addEventListener('DOMContentLoaded', function() {
            createParticles();
            
            // Simulate GitHub views counter (you can replace with actual API call)
            setTimeout(() => {
                animateCounter('github-views', 1284); // Example number
            }, 1000);
            
            // Add scroll animations
            const observerOptions = {
                threshold: 0.1,
                rootMargin: '0px 0px -50px 0px'
            };
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('animate-fade-in-up');
                    }
                });
            }, observerOptions);
            
            // Observe all sections
            document.querySelectorAll('section').forEach(section => {
                observer.observe(section);
            });
        });
    </script>
</body>
</html>
