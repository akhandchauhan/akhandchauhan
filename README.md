<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Akhand Chauhan - Data Engineer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'SF Pro Display', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            background: #ffffff;
            color: #1a1a1a;
            overflow-x: hidden;
            position: relative;
        }

        /* Animated grid background */
        .grid-background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(0, 191, 255, 0.03) 1px, transparent 1px),
                linear-gradient(90deg, rgba(0, 191, 255, 0.03) 1px, transparent 1px);
            background-size: 50px 50px;
            pointer-events: none;
            z-index: 0;
            animation: gridMove 20s linear infinite;
        }

        @keyframes gridMove {
            0% { transform: translate(0, 0); }
            100% { transform: translate(50px, 50px); }
        }

        /* Floating orbs */
        .orb {
            position: fixed;
            border-radius: 50%;
            filter: blur(60px);
            opacity: 0.15;
            pointer-events: none;
            z-index: 0;
            animation: float 20s infinite ease-in-out;
        }

        .orb1 {
            width: 400px;
            height: 400px;
            background: #00bfff;
            top: 10%;
            left: 10%;
            animation-delay: 0s;
        }

        .orb2 {
            width: 350px;
            height: 350px;
            background: #1e90ff;
            top: 60%;
            right: 10%;
            animation-delay: 5s;
        }

        .orb3 {
            width: 300px;
            height: 300px;
            background: #87ceeb;
            bottom: 20%;
            left: 50%;
            animation-delay: 10s;
        }

        @keyframes float {
            0%, 100% { transform: translate(0, 0) scale(1); }
            33% { transform: translate(50px, -50px) scale(1.1); }
            66% { transform: translate(-30px, 30px) scale(0.9); }
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 60px 30px;
            position: relative;
            z-index: 1;
        }

        .header {
            text-align: center;
            margin-bottom: 80px;
            animation: fadeInUp 1s ease;
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(40px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .wave {
            font-size: 80px;
            animation: wave 2.5s infinite;
            display: inline-block;
            filter: drop-shadow(0 5px 15px rgba(0, 191, 255, 0.3));
        }

        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(25deg); }
            75% { transform: rotate(-15deg); }
        }

        h1 {
            font-size: 4.5em;
            font-weight: 700;
            background: linear-gradient(135deg, #1a1a1a 0%, #00bfff 50%, #1e90ff 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin: 30px 0 20px;
            letter-spacing: -2px;
            position: relative;
        }

        .tagline {
            font-size: 1.5em;
            color: #00bfff;
            margin-bottom: 15px;
            font-weight: 500;
            opacity: 0;
            animation: fadeIn 1s ease 0.3s forwards;
            letter-spacing: 1px;
        }

        @keyframes fadeIn {
            to { opacity: 1; }
        }

        .card {
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(20px);
            border-radius: 30px;
            padding: 40px;
            margin: 40px 0;
            border: 2px solid rgba(0, 191, 255, 0.15);
            box-shadow: 
                0 20px 60px rgba(0, 191, 255, 0.1),
                inset 0 1px 0 rgba(255, 255, 255, 0.8);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
        }

        .card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0, 191, 255, 0.1), transparent);
            transition: left 0.5s;
        }

        .card:hover::before {
            left: 100%;
        }

        .card:hover {
            transform: translateY(-8px);
            box-shadow: 
                0 30px 80px rgba(0, 191, 255, 0.2),
                inset 0 1px 0 rgba(255, 255, 255, 0.9);
            border-color: rgba(0, 191, 255, 0.4);
        }

        h2 {
            font-size: 2.5em;
            color: #1a1a1a;
            margin-bottom: 30px;
            font-weight: 700;
            display: inline-block;
            position: relative;
            letter-spacing: -1px;
        }

        h2::after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 0;
            width: 0;
            height: 4px;
            background: linear-gradient(90deg, #00bfff, #1e90ff);
            transition: width 0.6s cubic-bezier(0.4, 0, 0.2, 1);
            border-radius: 2px;
        }

        .card:hover h2::after {
            width: 100%;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .tech-category {
            background: linear-gradient(135deg, rgba(0, 191, 255, 0.03), rgba(30, 144, 255, 0.05));
            padding: 30px;
            border-radius: 20px;
            border: 2px solid rgba(0, 191, 255, 0.1);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .tech-category::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(0, 191, 255, 0.05), transparent);
            transform: rotate(45deg);
            transition: all 0.6s;
        }

        .tech-category:hover::before {
            top: -60%;
            right: -60%;
        }

        .tech-category:hover {
            background: linear-gradient(135deg, rgba(0, 191, 255, 0.08), rgba(30, 144, 255, 0.1));
            border-color: rgba(0, 191, 255, 0.3);
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0, 191, 255, 0.15);
        }

        .tech-category h3 {
            color: #00bfff;
            font-size: 1.4em;
            margin-bottom: 20px;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .tech-items {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
        }

        .tech-tag {
            background: rgba(0, 191, 255, 0.08);
            color: #1a1a1a;
            padding: 10px 20px;
            border-radius: 25px;
            font-size: 0.95em;
            font-weight: 500;
            border: 2px solid rgba(0, 191, 255, 0.2);
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            cursor: pointer;
            position: relative;
        }

        .tech-tag:hover {
            background: rgba(0, 191, 255, 0.15);
            border-color: #00bfff;
            transform: translateY(-4px) scale(1.05);
            box-shadow: 0 8px 25px rgba(0, 191, 255, 0.25);
            color: #00bfff;
        }

        .about-list {
            list-style: none;
            padding: 0;
        }

        .about-list li {
            padding: 20px;
            margin: 15px 0;
            background: linear-gradient(90deg, rgba(0, 191, 255, 0.05), transparent);
            border-left: 4px solid #00bfff;
            border-radius: 10px;
            transition: all 0.3s ease;
            font-size: 1.1em;
        }

        .about-list li:hover {
            background: linear-gradient(90deg, rgba(0, 191, 255, 0.12), rgba(0, 191, 255, 0.03));
            transform: translateX(15px);
            border-left-width: 6px;
            box-shadow: 0 5px 20px rgba(0, 191, 255, 0.1);
        }

        /* GitHub Activity Calendar */
        .calendar-container {
            margin-top: 30px;
            padding: 30px;
            background: linear-gradient(135deg, rgba(0, 191, 255, 0.02), rgba(30, 144, 255, 0.03));
            border-radius: 20px;
            border: 2px solid rgba(0, 191, 255, 0.1);
        }

        .calendar-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }

        .calendar-stats {
            display: flex;
            gap: 30px;
            font-size: 0.9em;
        }

        .stat {
            text-align: center;
        }

        .stat-number {
            font-size: 2em;
            font-weight: 700;
            color: #00bfff;
            display: block;
        }

        .stat-label {
            color: #666;
            font-size: 0.9em;
        }

        .calendar-grid {
            display: grid;
            grid-template-columns: repeat(53, 1fr);
            gap: 4px;
            margin-top: 20px;
        }

        .calendar-day {
            aspect-ratio: 1;
            border-radius: 4px;
            background: rgba(0, 191, 255, 0.05);
            border: 1px solid rgba(0, 191, 255, 0.1);
            transition: all 0.2s ease;
            cursor: pointer;
        }

        .calendar-day:hover {
            transform: scale(1.3);
            z-index: 10;
            box-shadow: 0 4px 12px rgba(0, 191, 255, 0.3);
        }

        .calendar-day.level-0 { background: rgba(0, 191, 255, 0.05); }
        .calendar-day.level-1 { background: rgba(0, 191, 255, 0.25); }
        .calendar-day.level-2 { background: rgba(0, 191, 255, 0.5); }
        .calendar-day.level-3 { background: rgba(0, 191, 255, 0.75); }
        .calendar-day.level-4 { background: #00bfff; }

        .calendar-legend {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-top: 20px;
            font-size: 0.85em;
            color: #666;
        }

        .legend-item {
            width: 15px;
            height: 15px;
            border-radius: 3px;
            border: 1px solid rgba(0, 191, 255, 0.2);
        }

        .achievements-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .achievement {
            text-align: center;
            padding: 35px 25px;
            background: linear-gradient(135deg, rgba(0, 191, 255, 0.05), rgba(30, 144, 255, 0.08));
            border-radius: 20px;
            border: 2px solid rgba(0, 191, 255, 0.15);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
        }

        .achievement::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            border-radius: 50%;
            background: rgba(0, 191, 255, 0.1);
            transform: translate(-50%, -50%);
            transition: width 0.6s, height 0.6s;
        }

        .achievement:hover::before {
            width: 300px;
            height: 300px;
        }

        .achievement:hover {
            transform: translateY(-10px) scale(1.05);
            box-shadow: 0 20px 50px rgba(0, 191, 255, 0.2);
            border-color: #00bfff;
        }

        .achievement-icon {
            font-size: 3.5em;
            margin-bottom: 15px;
            animation: pulse 2.5s infinite;
            position: relative;
            z-index: 1;
            filter: drop-shadow(0 5px 15px rgba(0, 191, 255, 0.3));
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.15); }
        }

        .achievement p {
            font-size: 1.1em;
            font-weight: 600;
            color: #1a1a1a;
            position: relative;
            z-index: 1;
        }

        .footer {
            text-align: center;
            margin-top: 80px;
            padding: 40px;
            animation: fadeIn 1s ease 1s forwards;
            opacity: 0;
        }

        .footer-text {
            font-size: 1.6em;
            font-weight: 600;
            background: linear-gradient(90deg, #1a1a1a, #00bfff, #1e90ff, #00bfff, #1a1a1a);
            background-size: 200% auto;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: shimmer 4s linear infinite;
            letter-spacing: 0.5px;
        }

        @keyframes shimmer {
            to { background-position: 200% center; }
        }

        /* Scroll animations */
        .animate-on-scroll {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease;
        }

        .animate-on-scroll.visible {
            opacity: 1;
            transform: translateY(0);
        }

        @media (max-width: 768px) {
            h1 { font-size: 2.5em; }
            .tech-grid { grid-template-columns: 1fr; }
            .calendar-grid { grid-template-columns: repeat(26, 1fr); }
        }
    </style>
</head>
<body>
    <div class="grid-background"></div>
    <div class="orb orb1"></div>
    <div class="orb orb2"></div>
    <div class="orb orb3"></div>
    
    <div class="container">
        <div class="header">
            <div class="wave">👋</div>
            <h1>Hi, I'm Akhand Chauhan</h1>
            <p class="tagline">Data Engineer • Cloud • Distributed Systems • MLOps</p>
        </div>

        <div class="card animate-on-scroll">
            <h2>🧠 About Me</h2>
            <ul class="about-list">
                <li>🚀 Building <strong>production-grade data pipelines</strong></li>
                <li>🧩 Strong focus on <strong>reliability, observability & scale</strong></li>
                <li>☁️ Hands-on with <strong>AWS data engineering services</strong></li>
                <li>🔁 Experience with <strong>ETL orchestration, streaming & batch</strong></li>
                <li>🧪 Applying <strong>MLOps principles</strong> to data workflows</li>
            </ul>
        </div>

        <div class="card animate-on-scroll">
            <h2>🛠️ Tech Stack</h2>
            <div class="tech-grid">
                <div class="tech-category">
                    <h3>⚙️ Languages & Libraries</h3>
                    <div class="tech-items">
                        <span class="tech-tag">Python</span>
                        <span class="tech-tag">SQL</span>
                        <span class="tech-tag">Pandas</span>
                        <span class="tech-tag">NumPy</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3>🌐 APIs & Backend</h3>
                    <div class="tech-items">
                        <span class="tech-tag">FastAPI</span>
                        <span class="tech-tag">REST</span>
                        <span class="tech-tag">GraphQL</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3>📦 Big Data & Orchestration</h3>
                    <div class="tech-items">
                        <span class="tech-tag">PySpark</span>
                        <span class="tech-tag">Apache Airflow</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3>☁️ AWS Data Engineering</h3>
                    <div class="tech-items">
                        <span class="tech-tag">S3</span>
                        <span class="tech-tag">Glue</span>
                        <span class="tech-tag">Lambda</span>
                        <span class="tech-tag">Redshift</span>
                        <span class="tech-tag">Athena</span>
                        <span class="tech-tag">EMR</span>
                        <span class="tech-tag">Kinesis</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3>🧠 MLOps & Versioning</h3>
                    <div class="tech-items">
                        <span class="tech-tag">MLflow</span>
                        <span class="tech-tag">DVC</span>
                        <span class="tech-tag">Weights & Biases</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3>🐳 DevOps & Infrastructure</h3>
                    <div class="tech-items">
                        <span class="tech-tag">Docker</span>
                        <span class="tech-tag">Kubernetes</span>
                        <span class="tech-tag">Terraform</span>
                        <span class="tech-tag">CI/CD</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3>📊 Monitoring & Observability</h3>
                    <div class="tech-items">
                        <span class="tech-tag">Grafana</span>
                        <span class="tech-tag">Prometheus</span>
                        <span class="tech-tag">CloudWatch</span>
                    </div>
                </div>
            </div>
        </div>

        <div class="card animate-on-scroll">
            <h2>📈 GitHub Activity</h2>
            <div class="calendar-container">
                <div class="calendar-header">
                    <h3 style="color: #1a1a1a; font-size: 1.3em; margin: 0;">Contribution Graph</h3>
                    <div class="calendar-stats">
                        <div class="stat">
                            <span class="stat-number">1,247</span>
                            <span class="stat-label">Contributions</span>
                        </div>
                        <div class="stat">
                            <span class="stat-number">89</span>
                            <span class="stat-label">Streak</span>
                        </div>
                    </div>
                </div>
                <div class="calendar-grid" id="calendar"></div>
                <div class="calendar-legend">
                    <span>Less</span>
                    <div class="legend-item level-0"></div>
                    <div class="legend-item level-1"></div>
                    <div class="legend-item level-2"></div>
                    <div class="legend-item level-3"></div>
                    <div class="legend-item level-4"></div>
                    <span>More</span>
                </div>
            </div>
        </div>

        <div class="card animate-on-scroll">
            <h2>🏆 Achievements</h2>
            <div class="achievements-grid">
                <div class="achievement">
                    <div class="achievement-icon">🚀</div>
                    <p>Production Systems</p>
                </div>
                <div class="achievement">
                    <div class="achievement-icon">⚡</div>
                    <p>High Performance</p>
                </div>
                <div class="achievement">
                    <div class="achievement-icon">🎯</div>
                    <p>Mission Critical</p>
                </div>
                <div class="achievement">
                    <div class="achievement-icon">🔒</div>
                    <p>Reliable & Secure</p>
                </div>
            </div>
        </div>

        <div class="footer">
            <p class="footer-text">⚡ Engineering data systems that scale, observe, and endure.</p>
        </div>
    </div>

    <script>
        // Generate GitHub-style activity calendar
        const calendar = document.getElementById('calendar');
        const levels = [0, 1, 2, 3, 4];
        
        for (let i = 0; i < 371; i++) {
            const day = document.createElement('div');
            day.className = 'calendar-day';
            const level = levels[Math.floor(Math.random() * levels.length)];
            day.classList.add(`level-${level}`);
            day.style.animationDelay = `${i * 0.002}s`;
            calendar.appendChild(day);
        }

        // Scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.animate-on-scroll').forEach(el => {
            observer.observe(el);
        });

        // Add subtle parallax effect to orbs
        document.addEventListener('mousemove', (e) => {
            const orbs = document.querySelectorAll('.orb');
            const x = e.clientX / window.innerWidth;
            const y = e.clientY / window.innerHeight;
            
            orbs.forEach((orb, index) => {
                const speed = (index + 1) * 20;
                orb.style.transform = `translate(${x * speed}px, ${y * speed}px)`;
            });
        });
    </script>
</body>
</html>
