<!DOCTYPE html>
<html lang="si">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sasi Ra*e</title>
    <style>
        /* =============================================
                   🔐 PASSWORD LIST - මෙතන පාස්වර්ඩ් දාන්න
                   ============================================= */
        /*
            පාස්වර්ඩ් ලිස්ට් එක:
            "sasi123"
            "david"
            "deepseek"
            "mysecret"
            "123456"
        */
        
        /* ===== Reset ===== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-touch-callout: none !important;
            -webkit-user-select: none !important;
            user-select: none !important;
        }

        html, body {
            height: 100%;
            overflow: hidden;
            background: #0a0a0f;
        }

        body {
            font-family: 'Segoe UI', Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 8px;
        }

        /* ===== Main Container - FULL SCREEN ===== */
        .main-container {
            width: 50%;
            height: 50vh;
            max-height: 50vh;
            display: flex;
            flex-direction: column;
            background: linear-gradient(145deg, #12121a, #1a1a2e);
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.04);
            box-shadow: 0 30px 80px rgba(0, 0, 0, 0.9);
            overflow: hidden;
            position: relative;
        }

        /* =============================================
                   LOGIN OVERLAY - උඩින්ම
                   ============================================= */
        .login-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(10, 10, 15, 0.92);
            backdrop-filter: blur(20px);
            z-index: 1000;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            transition: opacity 0.6s ease, visibility 0.6s ease;
        }

        .login-overlay.hidden {
            opacity: 0;
            visibility: hidden;
            pointer-events: none;
        }

        .login-box {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.06);
            border-radius: 32px;
            padding: 50px 45px;
            max-width: 440px;
            width: 90%;
            text-align: center;
            box-shadow: 0 40px 100px rgba(0, 0, 0, 0.6);
        }

        .login-box .lock-icon {
            font-size: 56px;
            margin-bottom: 6px;
            display: block;
        }

        .login-box h2 {
            color: #fff;
            font-size: 26px;
            font-weight: 700;
            margin-bottom: 4px;
        }

        .login-box .sub {
            color: #888;
            font-size: 14px;
            margin-bottom: 25px;
        }

        .login-box input[type="password"] {
            width: 100%;
            padding: 16px 20px;
            border-radius: 16px;
            border: 1px solid rgba(255, 255, 255, 0.06);
            background: rgba(255, 255, 255, 0.04);
            color: #fff;
            font-size: 20px;
            outline: none;
            transition: 0.3s;
            margin-bottom: 14px;
            text-align: center;
            letter-spacing: 6px;
            font-weight: 600;
        }

        .login-box input[type="password"]:focus {
            border-color: #ffd700;
            box-shadow: 0 0 40px rgba(255, 215, 0, 0.04);
        }

        .login-box input[type="password"]::placeholder {
            color: #444;
            letter-spacing: 2px;
            font-size: 15px;
            font-weight: 400;
        }

        .login-box button {
            width: 100%;
            padding: 16px;
            border: none;
            border-radius: 16px;
            background: linear-gradient(135deg, #f7971e, #ffd200);
            color: #1a1a2e;
            font-size: 18px;
            font-weight: 700;
            cursor: pointer;
            transition: 0.3s;
            letter-spacing: 1px;
        }

        .login-box button:hover {
            transform: scale(1.02);
            box-shadow: 0 0 50px rgba(255, 215, 0, 0.12);
        }

        .login-box .error {
            color: #ff6b6b;
            font-size: 14px;
            margin-top: 12px;
            min-height: 24px;
            font-weight: 500;
        }

        .login-box .hint {
            color: #555;
            font-size: 12px;
            margin-top: 16px;
            letter-spacing: 0.5px;
        }

        /* ===== SITE CONTENT - Full Screen ===== */
        .site-content {
            flex: 1;
            display: flex;
            flex-direction: column;
            width: 100%;
            height: 100%;
            padding: 12px 16px 12px 16px;
            gap: 10px;
        }

        /* ===== Header - පොඩියට ===== */
        .header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 6px 10px 8px 10px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.04);
            flex-shrink: 0;
            gap: 12px;
            flex-wrap: wrap;
        }

        .logo h1 {
            font-size: 22px;
            font-weight: 800;
            background: linear-gradient(135deg, #f7971e, #ffd200);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .logo span {
            font-size: 13px;
            color: #666;
            -webkit-text-fill-color: #666;
            background: none;
            margin-left: 4px;
        }

        .header-right {
            display: flex;
            align-items: center;
            gap: 14px;
        }

        .badge {
            background: rgba(255, 215, 0, 0.08);
            padding: 4px 14px;
            border-radius: 50px;
            color: #ffd700;
            font-size: 11px;
            font-weight: 600;
            border: 1px solid rgba(255, 215, 0, 0.08);
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .badge .dot {
            width: 7px;
            height: 7px;
            background: #4ade80;
            border-radius: 50%;
            animation: pulse 1.2s infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); opacity: 1; }
            50% { transform: scale(1.5); opacity: 0.5; }
        }

        .logout-btn {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.04);
            color: #777;
            padding: 4px 14px;
            border-radius: 30px;
            cursor: pointer;
            font-size: 12px;
            transition: 0.3s;
        }

        .logout-btn:hover {
            background: rgba(255, 107, 107, 0.08);
            border-color: #ff6b6b;
            color: #ff6b6b;
        }

        /* ===== Iframe Wrapper - Context Menu Block ===== */
        .iframe-wrapper {
            flex: 1;
            border-radius: 16px;
            overflow: hidden;
            background: #0d0d18;
            border: 1px solid rgba(255, 255, 255, 0.04);
            min-height: 0;
            position: relative;
            /* ===== Long-press context menu එක block කරන්න ===== */
            -webkit-touch-callout: none !important;
            -webkit-user-select: none !important;
            user-select: none !important;
            touch-action: none !important;
            pointer-events: auto !important;
        }

        /* ===== Iframe එකම pointer-events: none කරලා overlay එකෙන් click catch කරනවා ===== */
        .iframe-wrapper iframe {
            width: 100%;
            height: 100%;
            border: none;
            border-radius: 16px;
            pointer-events: none !important;
            /* Iframe එකට clicks යන්නේ නැහැ - overlay එකට යනවා */
        }

        /* ===== OVERLAY - මෙය clicks catch කරනවා ===== */
        .iframe-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 10;
            background: transparent;
            pointer-events: auto !important;
            /* Overlay එකට clicks යනවා - මෙය context menu block කරනවා */
            cursor: default;
            -webkit-touch-callout: none !important;
            -webkit-user-select: none !important;
            user-select: none !important;
            touch-action: none !important;
        }

        /* ===== Overlay එක හරහා iframe එකට scroll වෙන්න ඉඩ දෙන්න ===== */
        .iframe-overlay {
            /* Scroll events iframe එකට යවන්න */
            overflow: hidden;
        }

        /* ===== Footer - පොඩියට ===== */
        .footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 4px 10px 2px 10px;
            border-top: 1px solid rgba(255, 255, 255, 0.03);
            color: #555;
            font-size: 11px;
            flex-shrink: 0;
            gap: 10px;
            flex-wrap: wrap;
        }

        .footer .info {
            display: flex;
            align-items: center;
            gap: 12px;
            color: #555;
        }

        .footer .info span {
            color: #444;
        }

        /* =============================================
                   RESPONSIVE
                   ============================================= */
        @media (max-width: 768px) {
            body {
                padding: 4px;
            }
            .login-box {
                padding: 35px 25px;
            }
            .login-box h2 {
                font-size: 22px;
            }
            .site-content {
                padding: 8px 10px 8px 10px;
                gap: 6px;
            }
            .logo h1 {
                font-size: 18px;
            }
            .logo span {
                font-size: 11px;
            }
            .badge {
                font-size: 10px;
                padding: 3px 10px;
            }
            .logout-btn {
                font-size: 10px;
                padding: 3px 10px;
            }
            .footer {
                font-size: 10px;
            }
        }

        @media (max-width: 400px) {
            .login-box {
                padding: 25px 18px;
            }
            .login-box h2 {
                font-size: 18px;
            }
            .login-box input[type="password"] {
                font-size: 16px;
                padding: 12px 14px;
            }
            .logo h1 {
                font-size: 15px;
            }
        }
    </style>
</head>
<body>

    <!-- =============================================
    🔐 PASSWORD LIST - ඔයාට ඕනෙ තරම් දාන්න
    ============================================= -->
    <script>
        // =============================================
        // 🔑 පාස්වර්ඩ් ලිස්ට් එක - මෙතන එකතු කරන්න
        // =============================================
        const VALID_PASSWORDS = [
            "sasi123",
            "admin2026",
            "deepseek",
            "mysecret",
            "123456"
        ];

        // =============================================
        // 🚫 Context Menu (Long-press) එක Block කරන්න - Global
        // =============================================
        // මුළු page එකටම
        document.addEventListener('contextmenu', function(e) {
            e.preventDefault();
            e.stopPropagation();
            return false;
        }, true);

        // =============================================
        // ඉතුරු කේතය
        // =============================================
    </script>

    <!-- =============================================
    MAIN CONTAINER
    ============================================= -->
    <div class="main-container">

        <!-- ===== LOGIN OVERLAY (උඩින්ම) ===== -->
        <div class="login-overlay" id="loginOverlay">
            <div class="login-box">
                <span class="lock-icon">🔐</span>
                <h2>Enter Password</h2>
                <p class="sub">මෙම site එක බැලීමට මුරපදය ඇතුළත් කරන්න</p>
                <input type="password" id="passwordInput" placeholder="••••••••" autofocus>
                <button onclick="checkPassword()">🔓 ඇතුළු වන්න</button>
                <div class="error" id="errorMsg"></div>
                <div class="hint">💡 පාස්වර්ඩ් කීපයක් තියෙනවා</div>
            </div>
        </div>

        <!-- ===== SITE CONTENT (Full Screen) ===== -->
        <div class="site-content" id="siteContent">

            <!-- Header - පොඩියට -->
            <div class="header">
                <div class="logo">
                    <h1>🚀 Sasi Ra*e</h1>
                </div>
                <div class="header-right">
                    <div class="badge">
                        <span class="dot"></span>
                        <span>LIVE</span>
                    </div>
                    <button class="logout-btn" onclick="logout()">🚪 පිටවන්න</button>
                </div>
            </div>

            <!-- ===== Iframe - Context Menu Block ===== -->
            <div class="iframe-wrapper" id="iframeWrapper">
                <!-- Overlay - මෙය clicks catch කරනවා -->
                <div class="iframe-overlay" id="iframeOverlay"></div>
                
                <!-- Iframe - pointer-events: none -->
                <iframe 
                    id="mainIframe"
                    src="https://forcedsex.org/" 
                    sandbox="allow-scripts allow-same-origin allow-forms allow-popups allow-modals"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen
                    loading="eager"
                ></iframe>
            </div>

            <!-- Footer - පොඩියට -->
            <div class="footer">
                <div class="info">
                    <span>✨ Sasi Ra*e</span>
                    <span style="color:#333;">|</span>
                    <span>🔒 Protected</span>
                </div>
                <div style="color:#444;">
                    © 2026 Sasi Ra*e
                </div>
            </div>

        </div>

    </div>

    <!-- =============================================
    JAVASCRIPT
    ============================================= -->
    <script>
        // ===== DOM Elements =====
        const loginOverlay = document.getElementById('loginOverlay');
        const siteContent = document.getElementById('siteContent');
        const passwordInput = document.getElementById('passwordInput');
        const errorMsg = document.getElementById('errorMsg');
        const iframeWrapper = document.getElementById('iframeWrapper');
        const iframeOverlay = document.getElementById('iframeOverlay');
        const mainIframe = document.getElementById('mainIframe');

        // ===== Check Password =====
        function checkPassword() {
            const entered = passwordInput.value.trim();

            if (VALID_PASSWORDS.includes(entered)) {
                loginOverlay.classList.add('hidden');
                errorMsg.textContent = '';
                passwordInput.value = '';
            } else {
                errorMsg.textContent = '❌ වැරදි මුරපදයකි. නැවත උත්සාහ කරන්න.';
                passwordInput.value = '';
                passwordInput.focus();
                document.querySelector('.login-box').style.animation = 'shake 0.4s ease';
                setTimeout(() => document.querySelector('.login-box').style.animation = '', 500);
            }
        }

        // ===== Enter key =====
        passwordInput.addEventListener('keydown', function(e) {
            if (e.key === 'Enter') {
                checkPassword();
            }
        });

        // ===== Logout =====
        function logout() {
            loginOverlay.classList.remove('hidden');
            passwordInput.value = '';
            passwordInput.focus();
            errorMsg.textContent = '';
        }

        // =============================================
        // 🚫 CONTEXT MENU BLOCK - හැම තැනම
        // =============================================
        
        // 1. මුළු page එකටම
        document.addEventListener('contextmenu', function(e) {
            e.preventDefault();
            e.stopPropagation();
            return false;
        }, true);

        // 2. Iframe wrapper එකට
        iframeWrapper.addEventListener('contextmenu', function(e) {
            e.preventDefault();
            e.stopPropagation();
            return false;
        }, true);

        // 3. Overlay එකට - මෙය වැදගත්ම
        iframeOverlay.addEventListener('contextmenu', function(e) {
            e.preventDefault();
            e.stopPropagation();
            return false;
        }, true);

        // 4. Iframe එකටම (Cross-origin නිසා වැඩ නොකරයි, ඒත් overlay එක වැඩ කරයි)
        try {
            mainIframe.addEventListener('contextmenu', function(e) {
                e.preventDefault();
                e.stopPropagation();
                return false;
            }, true);
        } catch(e) {
            // Cross-origin error - ignore
        }

        // 5. Long-press (touch) events block
        let pressTimer = null;
        document.addEventListener('touchstart', function(e) {
            pressTimer = setTimeout(() => {
                e.preventDefault();
                e.stopPropagation();
                return false;
            }, 300);
        }, { passive: false });

        document.addEventListener('touchend', function(e) {
            if (pressTimer) {
                clearTimeout(pressTimer);
                pressTimer = null;
            }
        }, { passive: false });

        document.addEventListener('touchmove', function(e) {
            if (pressTimer) {
                clearTimeout(pressTimer);
                pressTimer = null;
            }
        }, { passive: false });

        // 6. Select all text disable
        document.addEventListener('selectstart', function(e) {
            e.preventDefault();
            e.stopPropagation();
            return false;
        }, true);

        // 7. Copy, Cut, Paste disable
        document.addEventListener('copy', function(e) {
            e.preventDefault();
            e.stopPropagation();
            return false;
        }, true);
        document.addEventListener('cut', function(e) {
            e.preventDefault();
            e.stopPropagation();
            return false;
        }, true);
        document.addEventListener('paste', function(e) {
            e.preventDefault();
            e.stopPropagation();
            return false;
        }, true);

        // =============================================
        // OVERLAY හරහා iframe එකට click events relay කරන්න
        // =============================================
        // Overlay එක මත click කළාම iframe එකට click relay කරන්න
        iframeOverlay.addEventListener('click', function(e) {
            // Iframe එකට focus දෙන්න
            mainIframe.focus();
            // Click event එක iframe එකට relay කරන්න (Cross-origin නිසා සම්පූර්ණ නැහැ)
            try {
                mainIframe.contentWindow.focus();
            } catch(e) {
                // Cross-origin - ignore
            }
        });

        // Scroll events iframe එකට relay කරන්න
        iframeOverlay.addEventListener('wheel', function(e) {
            // Overlay හරහා scroll වෙන්න ඉඩ දෙන්න
            // Iframe එකට scroll event එක relay කරන්න බැහැ cross-origin නිසා
            // ඒත් overlay එක scrollable නැති නිසා iframe එක scroll වෙයි
        }, { passive: true });

        // =============================================
        // Shake Animation
        // =============================================
        const style = document.createElement('style');
        style.textContent = `
            @keyframes shake {
                0%, 100% { transform: translateX(0); }
                20% { transform: translateX(-12px); }
                40% { transform: translateX(12px); }
                60% { transform: translateX(-8px); }
                80% { transform: translateX(8px); }
            }
        `;
        document.head.appendChild(style);

        // ===== Auto-focus =====
        window.addEventListener('load', function() {
            setTimeout(() => passwordInput.focus(), 300);
        });

        document.addEventListener('click', function() {
            if (!loginOverlay.classList.contains('hidden')) {
                passwordInput.focus();
            }
        });

        console.log('🔒 Context Menu Blocked!');
        console.log('🔑 Valid Passwords:', VALID_PASSWORDS);
        console.log('📌 Iframe pointer-events: none, Overlay catches all clicks');
    </script>

</body>
</html>
