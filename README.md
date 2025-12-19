<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vicente Surigao - Creative Portfolio</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        
        * {
            font-family: 'Inter', sans-serif;
        }
        
        .gradient-bg {
            background: linear-gradient(135deg, #030303 0%, #070707 100%);
        }
        
        .glass-effect {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .floating {
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }
        
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.6s ease;
        }
        
        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        .project-card {
            transition: all 0.3s ease;
            transform: perspective(1000px) rotateX(0deg);
        }
        
        .project-card:hover {
            transform: perspective(1000px) rotateX(5deg) translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
        }
        
        .skill-bar {
            width: 0%;
            transition: width 2s ease-in-out;
        }
        
        .skill-bar.animate {
            width: var(--width);
        }
        
        .typing {
            border-right: 2px solid #667eea;
            animation: blink 1s infinite;
        }
        
        @keyframes blink {
            0%, 50% { border-color: transparent; }
            51%, 100% { border-color: #667eea; }
        }
        
        .parallax {
            transform: translateY(0);
            transition: transform 0.1s ease-out;
        }
    </style>
</head>
<body class="bg-gray-900 text-white overflow-x-hidden">
    <!-- Navigation -->
    <nav class="fixed top-0 w-full z-50 glass-effect">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center py-4">
                <div class="text-2xl font-bold gradient-text">AM</div>
                <div class="hidden md:flex space-x-8">
                    <a href="#home" class="nav-link hover:text-purple-400 transition-colors">Home</a>
                    <a href="#about" class="nav-link hover:text-purple-400 transition-colors">About</a>
                    <a href="#projects" class="nav-link hover:text-purple-400 transition-colors">Projects</a>
                    <a href="#skills" class="nav-link hover:text-purple-400 transition-colors">Skills</a>
                    <a href="#contact" class="nav-link hover:text-purple-400 transition-colors">Contact</a>
                </div>
                <button id="theme-toggle" class="p-2 rounded-lg hover:bg-white hover:bg-opacity-10 transition-colors">
                    🌙
                </button>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="min-h-screen gradient-bg flex items-center justify-center relative overflow-hidden">
        <div class="absolute inset-0 opacity-20">
            <div class="floating absolute top-20 left-20 w-72 h-72 bg-purple-500 rounded-full mix-blend-multiply filter blur-xl"></div>
            <div class="floating absolute top-40 right-20 w-72 h-72 bg-yellow-500 rounded-full mix-blend-multiply filter blur-xl" style="animation-delay: 2s;"></div>
            <div class="floating absolute bottom-20 left-1/2 w-72 h-72 bg-pink-500 rounded-full mix-blend-multiply filter blur-xl" style="animation-delay: 4s;"></div>
        </div>
        
        <div class="text-center z-10 px-4">
            <h1 class="text-6xl md:text-8xl font-bold mb-6 fade-in">
                Vicente<span class="text-yellow-400">Surigao</span>
            </h1>
            <p class="text-xl md:text-2xl mb-8 fade-in typing" id="typing-text">Creative Developer & Designer</p>
            <div class="flex flex-col sm:flex-row gap-4 justify-center fade-in">
                <button onclick="scrollToSection('projects')" class="px-8 py-3 bg-white text-purple-900 rounded-full font-semibold hover:bg-opacity-90 transition-all transform hover:scale-105">
                    View My Work
                </button>
                <button onclick="scrollToSection('contact')" class="px-8 py-3 border-2 border-white rounded-full font-semibold hover:bg-white hover:text-purple-900 transition-all transform hover:scale-105">
                    Get In Touch
                </button>
            </div>
        </div>
        
        <div class="absolute bottom-10 left-1/2 transform -translate-x-1/2 animate-bounce">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
            </svg>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 bg-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid md:grid-cols-2 gap-12 items-center">
                <div class="fade-in">
                    <h2 class="text-4xl font-bold mb-6">About Me</h2>
                    <p class="text-lg text-gray-300 mb-6">
                        I'm a passionate creative developer with 5+ years of experience crafting digital experiences that blend beautiful design with powerful functionality. I specialize in modern web technologies and love bringing ideas to life.
                    </p>
                    <p class="text-lg text-gray-300 mb-8">
                        When I'm not coding, you'll find me exploring new design trends, contributing to open source projects, or capturing moments through photography.
                    </p>
                    <div class="flex space-x-4">
                        <div class="text-center">
                            <div class="text-3xl font-bold text-purple-400">50+</div>
                            <div class="text-sm text-gray-400">Projects</div>
                        </div>
                        <div class="text-center">
                            <div class="text-3xl font-bold text-purple-400">5+</div>
                            <div class="text-sm text-gray-400">Years</div>
                        </div>
                        <div class="text-center">
                            <div class="text-3xl font-bold text-purple-400">30+</div>
                            <div class="text-sm text-gray-400">Clients</div>
                        </div>
                    </div>
                </div>
                <div class="fade-in">
                    <div class="relative">
                        <div class="w-80 h-80 mx-auto bg-gradient-to-br from-purple-500 to-pink-500 rounded-full flex items-center justify-center text-6xl">
                            👨‍💻
                        </div>
                        <div class="absolute -top-4 -right-4 w-24 h-24 bg-yellow-400 rounded-full flex items-center justify-center text-2xl floating">
                            ⚡
                        </div>
                        <div class="absolute -bottom-4 -left-4 w-20 h-20 bg-green-400 rounded-full flex items-center justify-center text-xl floating" style="animation-delay: 1s;">
                            🎨
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-20 bg-gray-900">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <h2 class="text-4xl font-bold text-center mb-12 fade-in">Featured Projects</h2>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="project-card bg-gray-800 rounded-xl overflow-hidden fade-in">
                    <div class="h-48 bg-gradient-to-br from-blue-500 to-purple-600 flex items-center justify-center text-4xl">
                        🚀
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2">E-Commerce Platform</h3>
                        <p class="text-gray-400 mb-4">Modern shopping experience with React and Node.js</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="px-3 py-1 bg-blue-600 rounded-full text-sm">React</span>
                            <span class="px-3 py-1 bg-green-600 rounded-full text-sm">Node.js</span>
                            <span class="px-3 py-1 bg-purple-600 rounded-full text-sm">MongoDB</span>
                        </div>
                        <button class="w-full py-2 bg-purple-600 hover:bg-purple-700 rounded-lg transition-colors">
                            View Project
                        </button>
                    </div>
                </div>

                <div class="project-card bg-gray-800 rounded-xl overflow-hidden fade-in">
                    <div class="h-48 bg-gradient-to-br from-green-500 to-teal-600 flex items-center justify-center text-4xl">
                        📱
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2">Mobile Banking App</h3>
                        <p class="text-gray-400 mb-4">Secure and intuitive financial management</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="px-3 py-1 bg-blue-600 rounded-full text-sm">Flutter</span>
                            <span class="px-3 py-1 bg-orange-600 rounded-full text-sm">Firebase</span>
                            <span class="px-3 py-1 bg-red-600 rounded-full text-sm">API</span>
                        </div>
                        <button class="w-full py-2 bg-purple-600 hover:bg-purple-700 rounded-lg transition-colors">
                            View Project
                        </button>
                    </div>
                </div>

                <div class="project-card bg-gray-800 rounded-xl overflow-hidden fade-in">
                    <div class="h-48 bg-gradient-to-br from-pink-500 to-red-600 flex items-center justify-center text-4xl">
                        🎨
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2">Creative Agency Site</h3>
                        <p class="text-gray-400 mb-4">Award-winning portfolio with stunning animations</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="px-3 py-1 bg-yellow-600 rounded-full text-sm">Vue.js</span>
                            <span class="px-3 py-1 bg-green-600 rounded-full text-sm">GSAP</span>
                            <span class="px-3 py-1 bg-blue-600 rounded-full text-sm">CSS3</span>
                        </div>
                        <button class="w-full py-2 bg-purple-600 hover:bg-purple-700 rounded-lg transition-colors">
                            View Project
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="py-20 bg-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <h2 class="text-4xl font-bold text-center mb-12 fade-in">Skills & Expertise</h2>
            
            <div class="grid md:grid-cols-2 gap-12">
                <div class="fade-in">
                    <h3 class="text-2xl font-bold mb-6">Technical Skills</h3>
                    <div class="space-y-4">
                        <div class="skill-item">
                            <div class="flex justify-between mb-2">
                                <span>JavaScript/TypeScript</span>
                                <span>95%</span>
                            </div>
                            <div class="w-full bg-gray-700 rounded-full h-2">
                                <div class="skill-bar bg-gradient-to-r from-yellow-400 to-orange-500 h-2 rounded-full" style="--width: 95%"></div>
                            </div>
                        </div>
                        
                        <div class="skill-item">
                            <div class="flex justify-between mb-2">
                                <span>React/Vue.js</span>
                                <span>90%</span>
                            </div>
                            <div class="w-full bg-gray-700 rounded-full h-2">
                                <div class="skill-bar bg-gradient-to-r from-blue-400 to-purple-500 h-2 rounded-full" style="--width: 90%"></div>
                            </div>
                        </div>
                        
                        <div class="skill-item">
                            <div class="flex justify-between mb-2">
                                <span>Node.js/Python</span>
                                <span>85%</span>
                            </div>
                            <div class="w-full bg-gray-700 rounded-full h-2">
                                <div class="skill-bar bg-gradient-to-r from-green-400 to-teal-500 h-2 rounded-full" style="--width: 85%"></div>
                            </div>
                        </div>
                        
                        <div class="skill-item">
                            <div class="flex justify-between mb-2">
                                <span>UI/UX Design</span>
                                <span>88%</span>
                            </div>
                            <div class="w-full bg-gray-700 rounded-full h-2">
                                <div class="skill-bar bg-gradient-to-r from-pink-400 to-red-500 h-2 rounded-full" style="--width: 88%"></div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="fade-in">
                    <h3 class="text-2xl font-bold mb-6">Tools & Technologies</h3>
                    <div class="grid grid-cols-3 gap-4">
                        <div class="text-center p-4 bg-gray-700 rounded-lg hover:bg-gray-600 transition-colors">
                            <div class="text-3xl mb-2">⚛️</div>
                            <div class="text-sm">React</div>
                        </div>
                        <div class="text-center p-4 bg-gray-700 rounded-lg hover:bg-gray-600 transition-colors">
                            <div class="text-3xl mb-2">🟢</div>
                            <div class="text-sm">Node.js</div>
                        </div>
                        <div class="text-center p-4 bg-gray-700 rounded-lg hover:bg-gray-600 transition-colors">
                            <div class="text-3xl mb-2">🐍</div>
                            <div class="text-sm">Python</div>
                        </div>
                        <div class="text-center p-4 bg-gray-700 rounded-lg hover:bg-gray-600 transition-colors">
                            <div class="text-3xl mb-2">🎨</div>
                            <div class="text-sm">Figma</div>
                        </div>
                        <div class="text-center p-4 bg-gray-700 rounded-lg hover:bg-gray-600 transition-colors">
                            <div class="text-3xl mb-2">🐳</div>
                            <div class="text-sm">Docker</div>
                        </div>
                        <div class="text-center p-4 bg-gray-700 rounded-lg hover:bg-gray-600 transition-colors">
                            <div class="text-3xl mb-2">☁️</div>
                            <div class="text-sm">AWS</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 bg-gray-900">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h2 class="text-4xl font-bold text-center mb-12 fade-in">Let's Work Together</h2>
            
            <div class="grid md:grid-cols-2 gap-12">
                <div class="fade-in">
                    <h3 class="text-2xl font-bold mb-6">Get In Touch</h3>
                    <p class="text-gray-300 mb-8">
                        Ready to bring your ideas to life? I'm always excited to work on new projects and collaborate with amazing people.
                    </p>
                    
                    <div class="space-y-4">
                        <div class="flex items-center space-x-4">
                            <div class="w-12 h-12 bg-purple-600 rounded-full flex items-center justify-center">
                                📧
                            </div>
                            <div>
                                <div class="font-semibold">Email</div>
                                <div class="text-gray-400">vicente@example.com</div>
                            </div>
                        </div>
                        
                        <div class="flex items-center space-x-4">
                            <div class="w-12 h-12 bg-purple-600 rounded-full flex items-center justify-center">
                                📱
                            </div>
                            <div>
                                <div class="font-semibold">Phone</div>
                                <div class="text-gray-400">+1 (555) 123-4567</div>
                            </div>
                        </div>
                        
                        <div class="flex items-center space-x-4">
                            <div class="w-12 h-12 bg-purple-600 rounded-full flex items-center justify-center">
                                📍
                            </div>
                            <div>
                                <div class="font-semibold">Masbate</div>
                                <div class="text-gray-400">Pob.East</div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="flex space-x-4 mt-8">
                        <button class="w-12 h-12 bg-blue-600 hover:bg-blue-700 rounded-full flex items-center justify-center transition-colors">
                            📘
                        </button>
                        <button class="w-12 h-12 bg-blue-400 hover:bg-blue-500 rounded-full flex items-center justify-center transition-colors">
                            🐦
                        </button>
                        <button class="w-12 h-12 bg-purple-600 hover:bg-purple-700 rounded-full flex items-center justify-center transition-colors">
                            💼
                        </button>
                        <button class="w-12 h-12 bg-gray-700 hover:bg-gray-600 rounded-full flex items-center justify-center transition-colors">
                            🐙
                        </button>
                    </div>
                </div>
                
                <div class="fade-in">
                    <form class="space-y-6" onsubmit="handleSubmit(event)">
                        <div>
                            <label class="block text-sm font-medium mb-2">Name</label>
                            <input type="text" required class="w-full px-4 py-3 bg-gray-800 border border-gray-700 rounded-lg focus:ring-2 focus:ring-purple-500 focus:border-transparent transition-all">
                        </div>
                        
                        <div>
                            <label class="block text-sm font-medium mb-2">Email</label>
                            <input type="email" required class="w-full px-4 py-3 bg-gray-800 border border-gray-700 rounded-lg focus:ring-2 focus:ring-purple-500 focus:border-transparent transition-all">
                        </div>
                        
                        <div>
                            <label class="block text-sm font-medium mb-2">Subject</label>
                            <input type="text" required class="w-full px-4 py-3 bg-gray-800 border border-gray-700 rounded-lg focus:ring-2 focus:ring-purple-500 focus:border-transparent transition-all">
                        </div>
                        
                        <div>
                            <label class="block text-sm font-medium mb-2">Message</label>
                            <textarea rows="5" required class="w-full px-4 py-3 bg-gray-800 border border-gray-700 rounded-lg focus:ring-2 focus:ring-purple-500 focus:border-transparent transition-all resize-none"></textarea>
                        </div>
                        
                        <button type="submit" class="w-full py-3 bg-gradient-to-r from-purple-600 to-pink-600 hover:from-purple-700 hover:to-pink-700 rounded-lg font-semibold transition-all transform hover:scale-105">
                            Send Message
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="py-8 bg-gray-800 border-t border-gray-700">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center">
                <p class="text-gray-400">© 2025 Vicente Surigao. All rights reserved.</p>
                <p class="text-gray-500 text-sm mt-2">Built with passion and lots of coffee ☕</p>
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling
        function scrollToSection(sectionId) {
            document.getElementById(sectionId).scrollIntoView({
                behavior: 'smooth'
            });
        }

        // Navigation links smooth scroll
        document.querySelectorAll('.nav-link').forEach(link => {
            link.addEventListener('click', (e) => {
                e.preventDefault();
                const targetId = link.getAttribute('href').substring(1);
                scrollToSection(targetId);
            });
        });

        // Intersection Observer for fade-in animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                    
                    // Animate skill bars when skills section is visible
                    if (entry.target.id === 'skills') {
                        setTimeout(() => {
                            document.querySelectorAll('.skill-bar').forEach(bar => {
                                bar.classList.add('animate');
                            });
                        }, 500);
                    }
                }
            });
        }, observerOptions);

        // Observe all fade-in elements
        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });

        // Observe sections for skill animation
        observer.observe(document.getElementById('skills'));

        // Typing animation
        const typingText = document.getElementById('typing-text');
        const texts = [
            'Creative Developer & Designer',
            'Full-Stack Engineer',
            'UI/UX Enthusiast',
            'Problem Solver'
        ];
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;

        function typeWriter() {
            const currentText = texts[textIndex];
            
            if (isDeleting) {
                typingText.textContent = currentText.substring(0, charIndex - 1);
                charIndex--;
            } else {
                typingText.textContent = currentText.substring(0, charIndex + 1);
                charIndex++;
            }

            let typeSpeed = isDeleting ? 50 : 100;

            if (!isDeleting && charIndex === currentText.length) {
                typeSpeed = 2000;
                isDeleting = true;
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                textIndex = (textIndex + 1) % texts.length;
                typeSpeed = 500;
            }

            setTimeout(typeWriter, typeSpeed);
        }

        // Start typing animation after page load
        setTimeout(typeWriter, 1000);

        // Theme toggle
        const themeToggle = document.getElementById('theme-toggle');
        let isDark = true;

        themeToggle.addEventListener('click', () => {
            isDark = !isDark;
            themeToggle.textContent = isDark ? '🌙' : '☀️';
            
            if (isDark) {
                document.body.classList.remove('bg-white', 'text-gray-900');
                document.body.classList.add('bg-gray-900', 'text-white');
            } else {
                document.body.classList.remove('bg-gray-900', 'text-white');
                document.body.classList.add('bg-white', 'text-gray-900');
            }
        });

        // Parallax effect
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const parallaxElements = document.querySelectorAll('.parallax');
            
            parallaxElements.forEach(element => {
                const speed = element.dataset.speed || 0.5;
                element.style.transform = `translateY(${scrolled * speed}px)`;
            });
        });

        // Form submission
        function handleSubmit(event) {
            event.preventDefault();
            
            // Show success message
            const button = event.target.querySelector('button[type="submit"]');
            const originalText = button.textContent;
            
            button.textContent = 'Sending...';
            button.disabled = true;
            
            setTimeout(() => {
                button.textContent = 'Message Sent! ✓';
                button.classList.add('bg-green-600');
                
                setTimeout(() => {
                    button.textContent = originalText;
                    button.disabled = false;
                    button.classList.remove('bg-green-600');
                    event.target.reset();
                }, 2000);
            }, 1500);
        }

        // Add some interactive particles
        function createParticle() {
            const particle = document.createElement('div');
            particle.className = 'fixed w-2 h-2 bg-purple-400 rounded-full opacity-70 pointer-events-none z-0';
            particle.style.left = Math.random() * window.innerWidth + 'px';
            particle.style.top = window.innerHeight + 'px';
            
            document.body.appendChild(particle);
            
            const animation = particle.animate([
                { transform: 'translateY(0px)', opacity: 0.7 },
                { transform: `translateY(-${window.innerHeight + 100}px)`, opacity: 0 }
            ], {
                duration: Math.random() * 3000 + 2000,
                easing: 'linear'
            });
            
            animation.onfinish = () => particle.remove();
        }

        // Create particles periodically
        setInterval(createParticle, 2000);

        // Initialize animations on load
        window.addEventListener('load', () => {
            document.querySelectorAll('.fade-in').forEach((el, index) => {
                setTimeout(() => {
                    el.style.transitionDelay = `${index * 0.1}s`;
                }, 100);
            });
        });
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9b05768985e7bc4f',t:'MTc2NjEzMjI0MS4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
