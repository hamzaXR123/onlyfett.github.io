
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ONLYFEET | Premium Foot Content Platform</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #8a2be2;
            --primary-dark: #6a1b9a;
            --secondary: #ff6b6b;
            --dark: #0f0c29;
            --darker: #07051a;
            --light: #f8f9fa;
            --text: #ffffff;
            --text-secondary: rgba(255, 255, 255, 0.7);
            --success: #4caf50;
            --error: #f44336;
            --warning: #ff9800;
        }

        @keyframes gradientBG {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
            100% { transform: translateY(0px); }
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background: linear-gradient(-45deg, var(--darker), var(--dark), var(--primary-dark), var(--primary));
            background-size: 400% 400%;
            animation: gradientBG 15s ease infinite;
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            display: flex;
            width: 90%;
            max-width: 1200px;
            background: rgba(255, 255, 255, 0.08);
            border-radius: 20px;
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            box-shadow: 0 25px 45px rgba(0, 0, 0, 0.3);
            overflow: hidden;
            margin: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            animation: fadeIn 0.8s ease-out;
        }

        .login-section {
            width: 50%;
            padding: 50px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            position: relative;
            z-index: 2;
        }

        .brand {
            text-align: center;
            margin-bottom: 40px;
            animation: fadeIn 1s ease-out 0.2s both;
        }

        .brand h1 {
            font-size: 2.8rem;
            margin-bottom: 10px;
            background: linear-gradient(to right, var(--light), var(--secondary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 700;
            letter-spacing: 1px;
        }

        .brand p {
            color: var(--text-secondary);
            font-size: 1rem;
            max-width: 400px;
            margin: 0 auto;
        }

        .login-form {
            animation: fadeIn 1s ease-out 0.4s both;
        }

        .input-group {
            margin-bottom: 25px;
            position: relative;
        }

        .input-group label {
            display: block;
            margin-bottom: 10px;
            color: var(--text);
            font-weight: 500;
            font-size: 0.95rem;
        }

        .input-group input {
            width: 100%;
            padding: 16px 20px;
            border: none;
            border-radius: 10px;
            font-size: 1rem;
            background: rgba(255, 255, 255, 0.12);
            color: var(--text);
            outline: none;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .input-group input:focus {
            background: rgba(255, 255, 255, 0.2);
            border-color: var(--secondary);
            box-shadow: 0 0 0 3px rgba(255, 107, 107, 0.3);
        }

        .input-group input::placeholder {
            color: var(--text-secondary);
            opacity: 0.7;
        }

        .password-container {
            position: relative;
        }

        .toggle-password {
            position: absolute;
            right: 15px;
            top: 50%;
            transform: translateY(-50%);
            cursor: pointer;
            color: var(--text-secondary);
            transition: all 0.3s;
            background: none;
            border: none;
            font-size: 1rem;
        }

        .toggle-password:hover {
            color: var(--text);
            transform: translateY(-50%) scale(1.1);
        }

        .additional-options {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin: 20px 0;
            font-size: 0.9rem;
        }

        .remember-me {
            display: flex;
            align-items: center;
        }

        .remember-me input {
            margin-right: 8px;
            accent-color: var(--secondary);
            cursor: pointer;
        }

        .remember-me label {
            cursor: pointer;
            user-select: none;
        }

        .forgot-password a {
            color: var(--secondary);
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s;
        }

        .forgot-password a:hover {
            text-decoration: underline;
            color: var(--text);
        }

        .login-btn {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 16px;
            border: none;
            border-radius: 10px;
            width: 100%;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.4s ease;
            margin-top: 10px;
            box-shadow: 0 8px 20px rgba(138, 43, 226, 0.4);
            position: relative;
            overflow: hidden;
        }

        .login-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 25px rgba(138, 43, 226, 0.6);
        }

        .login-btn:active {
            transform: translateY(0);
        }

        .login-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: 0.5s;
        }

        .login-btn:hover::before {
            left: 100%;
        }

        .divider {
            display: flex;
            align-items: center;
            margin: 30px 0;
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        .divider::before, .divider::after {
            content: "";
            flex: 1;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .divider::before {
            margin-right: 15px;
        }

        .divider::after {
            margin-left: 15px;
        }

        .social-login {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 25px;
        }

        .social-btn {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.08);
            color: var(--text);
            font-size: 1.2rem;
            transition: all 0.4s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
            position: relative;
            overflow: hidden;
        }

        .social-btn:hover {
            background: rgba(255, 255, 255, 0.15);
            transform: translateY(-3px) scale(1.1);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .social-btn::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at center, rgba(255, 255, 255, 0.3) 0%, transparent 70%);
            opacity: 0;
            transition: opacity 0.3s;
        }

        .social-btn:hover::after {
            opacity: 1;
        }

        .register-link {
            text-align: center;
            margin-top: 25px;
            font-size: 0.95rem;
        }

        .register-link a {
            color: var(--secondary);
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s;
            position: relative;
        }

        .register-link a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -2px;
            left: 0;
            background-color: var(--secondary);
            transition: width 0.3s;
        }

        .register-link a:hover::after {
            width: 100%;
        }

        .image-section {
            width: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 40px;
            background: linear-gradient(135deg, rgba(138, 43, 226, 0.2), rgba(255, 107, 107, 0.2));
            position: relative;
            overflow: hidden;
        }

        .image-section::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle at center, rgba(255, 255, 255, 0.05) 0%, transparent 70%);
            animation: float 6s ease-in-out infinite;
        }

        .image-section img {
            max-width: 100%;
            max-height: 500px;
            border-radius: 10px;
            object-fit: cover;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.4);
            z-index: 2;
            animation: fadeIn 1s ease-out 0.6s both, float 4s ease-in-out infinite 1s;
        }

        .particles {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 1;
            overflow: hidden;
        }

        .particle {
            position: absolute;
            background: rgba(255, 255, 255, 0.6);
            border-radius: 50%;
            animation: float 6s infinite linear;
        }

        /* Alert styles */
        .alert {
            position: fixed;
            top: 20px;
            right: 20px;
            padding: 16px 24px;
            border-radius: 8px;
            color: white;
            display: flex;
            align-items: center;
            gap: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            z-index: 1000;
            animation: fadeIn 0.5s ease-out;
            transform-origin: top right;
        }

        .alert.success {
            background: var(--success);
        }

        .alert.error {
            background: var(--error);
        }

        .alert.warning {
            background: var(--warning);
        }

        .alert i {
            font-size: 1.2rem;
        }

        /* Responsive design */
        @media (max-width: 992px) {
            .container {
                flex-direction: column;
            }

            .login-section, .image-section {
                width: 100%;
            }

            .image-section {
                padding: 30px;
                order: -1;
                min-height: 300px;
            }

            .login-section {
                padding: 40px;
            }

            .brand h1 {
                font-size: 2.4rem;
            }
        }

        @media (max-width: 768px) {
            .container {
                width: 95%;
                margin: 10px;
            }

            .login-section {
                padding: 30px;
            }

            .brand h1 {
                font-size: 2.2rem;
            }

            .input-group input {
                padding: 14px 18px;
            }

            .login-btn {
                padding: 14px;
            }
        }

        @media (max-width: 480px) {
            .container {
                border-radius: 15px;
            }

            .login-section {
                padding: 25px;
            }

            .image-section {
                padding: 20px;
                min-height: 250px;
            }

            .brand h1 {
                font-size: 2rem;
            }

            .input-group input {
                padding: 12px 16px;
            }

            .login-btn {
                padding: 12px;
            }

            .social-btn {
                width: 45px;
                height: 45px;
                font-size: 1.1rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="login-section">
            <div class="brand">
                <h1>ONLYFEET</h1>
                <p>Exclusive premium foot content from top creators worldwide</p>
            </div>
            
            <form id="loginForm" class="login-form">
                <div class="input-group">
                    <label for="username">Username or Email</label>
                    <input type="text" id="username" placeholder="Enter your username or email" required autocomplete="username">
                </div>
                
                <div class="input-group">
                    <label for="password">Password</label>
                    <div class="password-container">
                        <input type="password" id="password" placeholder="Enter your password" required autocomplete="current-password">
                        <button type="button" class="toggle-password" id="togglePassword" aria-label="Toggle password visibility">
                            <i class="fas fa-eye"></i>
                        </button>
                    </div>
                </div>
                
                <div class="additional-options">
                    <div class="remember-me">
                        <input type="checkbox" id="remember" name="remember">
                        <label for="remember">Remember me</label>
                    </div>
                    <div class="forgot-password">
                        <a href="enterrr.html" id="forgotPassword">Forgot password?</a>
                    </div>
                </div>
                
                <button type="submit" class="login-btn" id="loginButton">
                    <span id="loginText">Sign In</span>
                    <span id="loginSpinner" style="display: none;">
                        <a href="enterrr.html" class="fas fa-spinner fa-spin"></a>
                    </span>
                </button>
                
                <div class="divider">or continue with</div>
                
                <div class="social-login">
                    <a href="#" class="social-btn" title="Login with Google" aria-label="Login with Google">
                        <i class="fab fa-google"></i>
                    </a>
                    <a href="#" class="social-btn" title="Login with Apple" aria-label="Login with Apple">
                        <i class="fab fa-apple"></i>
                    </a>
                    <a href="#" class="social-btn" title="Login with Twitter" aria-label="Login with Twitter">
                        <i class="fab fa-twitter"></i>
                    </a>
                </div>
                
                <div class="register-link">
                    New to ONLYFEET? <a href="enterrr.html" id="registerLink">Create an account</a>
                </div>
            </form>
        </div>
        
        <div class="image-section">
            <div class="particles" id="particles"></div>
            <img src="data:image/jpeg;base64,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" alt="Premium Foot Content">![Uploading image.png…]()

        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // DOM Elements
            const loginForm = document.getElementById('loginForm');
            const togglePassword = document.getElementById('togglePassword');
            const passwordInput = document.getElementById('password');
            const loginButton = document.getElementById('loginButton');
            const loginText = document.getElementById('loginText');
            const loginSpinner = document.getElementById('loginSpinner');
            const forgotPassword = document.getElementById('forgotPassword');
            const registerLink = document.getElementById('registerLink');
            const particlesContainer = document.getElementById('particles');
            
            // Create particles
            createParticles();
            
            // Toggle password visibility
            togglePassword.addEventListener('click', function() {
                const type = passwordInput.getAttribute('type') === 'password' ? 'text' : 'password';
                passwordInput.setAttribute('type', type);
                const icon = this.querySelector('i');
                icon.classList.toggle('fa-eye');
                icon.classList.toggle('fa-eye-slash');
                
                // Add animation
                this.style.transform = 'translateY(-50%) scale(1.2)';
                setTimeout(() => {
                    this.style.transform = 'translateY(-50%) scale(1)';
                }, 200);
            });
            
            // Form submission
            loginForm.addEventListener('submit', async function(e) {
                e.preventDefault();
                
                const username = document.getElementById('username').value.trim();
                const password = document.getElementById('password').value;
                const rememberMe = document.getElementById('remember').checked;
                
                // Validate inputs
                if (!username || !password) {
                    showAlert('Please fill in all fields', 'error');
                    return;
                }
                
                // Show loading state
                loginText.style.display = 'none';
                loginSpinner.style.display = 'inline-block';
                loginButton.disabled = true;
                
                try {
                    // Simulate API call (replace with actual fetch)
                    const response = await simulateLogin(username, password, rememberMe);
                    
                    if (response.success) {
                        showAlert('Login successful! Redirecting...', 'success');
                        
                        // Store user data if remember me is checked
                        if (rememberMe) {
                            localStorage.setItem('onlyfeet_rememberedUser', username);
                        } else {
                            sessionStorage.setItem('onlyfeet_currentUser', username);
                        }
                        
                        // Redirect after delay
                        setTimeout(() => {
                            window.location.href ="enterrr.html";
                        }, 1500);
                    } else {
                        showAlert(response.message || 'Invalid credentials', 'error');
                        loginText.style.display = 'inline-block';
                        loginSpinner.style.display = 'none';
                        loginButton.disabled = false;
                    }
                } catch (error) {
                    showAlert('An error occurred. Please try again.', 'error');
                    console.error('Login error:', error);
                    loginText.style.display = 'inline-block';
                    loginSpinner.style.display = 'none';
                    loginButton.disabled = false;
                }
            });
            
            // Forgot password handler
            forgotPassword.addEventListener('click', function(e) {
                e.preventDefault();
                showAlert('Password reset link sent to your email (simulated)', 'success');
            });
            
            // Register link handler
            registerLink.addEventListener('click', function(e) {
                e.preventDefault();
                showAlert('Redirecting to registration page (simulated)', 'warning');
                // In a real app: window.location.href = 'register.html';
            });
            
            // Check for remembered user
            const rememberedUser = localStorage.getItem('onlyfeet_rememberedUser');
            if (rememberedUser) {
                document.getElementById('username').value = rememberedUser;
                document.getElementById('remember').checked = true;
            }
            
            // Functions
            function createParticles() {
                const particleCount = window.innerWidth < 768 ? 15 : 30;
                
                for (let i = 0; i < particleCount; i++) {
                    const particle = document.createElement('div');
                    particle.classList.add('particle');
                    
                    // Random properties
                    const size = Math.random() * 5 + 2;
                    const posX = Math.random() * 100;
                    const posY = Math.random() * 100;
                    const opacity = Math.random() * 0.5 + 0.1;
                    const duration = Math.random() * 10 + 5;
                    const delay = Math.random() * 5;
                    
                    // Apply styles
                    particle.style.width = `${size}px`;
                    particle.style.height = `${size}px`;
                    particle.style.left = `${posX}%`;
                    particle.style.top = `${posY}%`;
                    particle.style.opacity = opacity;
                    particle.style.animationDuration = `${duration}s`;
                    particle.style.animationDelay = `${delay}s`;
                    
                    particlesContainer.appendChild(particle);
                }
            }
            
            async function simulateLogin(username, password, remember) {
                // Simulate network delay
                await new Promise(resolve => setTimeout(resolve, 1500));
                
                // For demo purposes, accept any non-empty password
                if (password.length > 0) {
                    return {
                        success: true,
                        user: {
                            id: 'user_' + Math.random().toString(36).substr(2, 9),
                            username: username,
                            token: 'simulated_token_' + Math.random().toString(36).substr(2, 16)
                        }
                    };
                } else {
                    return {
                        success: false,
                        message: 'Invalid password'
                    };
                }
            }
            
            function showAlert(message, type) {
                // Remove existing alerts
                const existingAlert = document.querySelector('.alert');
                if (existingAlert) existingAlert.remove();
                
                const alertDiv = document.createElement('div');
                alertDiv.className = `alert ${type}`;
                alertDiv.innerHTML = `
                    <i class="fas ${type === 'success' ? 'fa-check-circle' : type === 'error' ? 'fa-exclamation-circle' : 'fa-exclamation-triangle'}"></i>
                    ${message}
                `;
                
                document.body.appendChild(alertDiv);
                
                // Auto-remove after delay
                setTimeout(() => {
                    alertDiv.style.opacity = '0';
                    setTimeout(() => alertDiv.remove(), 300);
                }, 3000);
            }
        });
    </script>
</body>
</html>
