<!DOCTYPE html>
<html lang="fa">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Zubair 😔</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: #0a0a1a;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            overflow: hidden;
            position: relative;
        }

        /* افکت پس‌زمینه با ستاره‌های متحرک */
        .stars {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            background: radial-gradient(2px 2px at 20px 30px, #eee, transparent),
                        radial-gradient(2px 2px at 40px 70px, rgba(255,255,255,0.8), transparent),
                        radial-gradient(2px 2px at 50px 160px, #ddd, transparent),
                        radial-gradient(2px 2px at 90px 40px, rgba(255,255,255,0.6), transparent),
                        radial-gradient(2px 2px at 130px 80px, #fff, transparent),
                        radial-gradient(2px 2px at 160px 30px, rgba(255,255,255,0.7), transparent);
            background-size: 200px 200px;
            animation: twinkle 4s ease-in-out infinite alternate;
        }

        @keyframes twinkle {
            0% { opacity: 0.3; }
            100% { opacity: 1; }
        }

        /* کارت اصلی */
        .card {
            background: linear-gradient(145deg, rgba(30, 20, 50, 0.9), rgba(15, 10, 30, 0.95));
            backdrop-filter: blur(30px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 70px 70px 40px 40px;
            padding: 55px 45px 45px;
            width: 420px;
            max-width: 92%;
            text-align: center;
            box-shadow: 0 40px 100px rgba(0, 0, 0, 0.9), inset 0 1px 0 rgba(255, 255, 255, 0.1);
            z-index: 10;
            animation: floatCard 6s ease-in-out infinite;
            position: relative;
        }

        @keyframes floatCard {
            0% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-15px) rotate(0.5deg); }
            100% { transform: translateY(0px) rotate(0deg); }
        }

        /* صورتک غمگین با انیمیشن ضربان */
        .sad-emoji {
            font-size: 100px;
            display: block;
            animation: sadPulse 2s ease-in-out infinite;
            filter: drop-shadow(0 0 50px rgba(150, 50, 200, 0.3));
            margin-bottom: 5px;
        }

        @keyframes sadPulse {
            0% { transform: scale(1); opacity: 0.8; }
            50% { transform: scale(1.08); opacity: 1; }
            100% { transform: scale(1); opacity: 0.8; }
        }

        /* متن اصلی */
        h1 {
            color: #f0e8ff;
            font-size: 3rem;
            font-weight: 300;
            letter-spacing: 8px;
            margin: 8px 0 5px;
            text-shadow: 0 0 60px rgba(180, 120, 255, 0.2);
            animation: sadText 2.5s ease-out;
        }

        @keyframes sadText {
            0% { letter-spacing: 20px; opacity: 0; transform: scale(0.8); }
            100% { letter-spacing: 8px; opacity: 1; transform: scale(1); }
        }

        .subtitle {
            color: #a898c8;
            font-size: 0.95rem;
            letter-spacing: 4px;
            margin-bottom: 30px;
            opacity: 0.7;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
            padding-bottom: 22px;
            font-weight: 300;
        }

        /* لینک‌ها */
        .links {
            display: flex;
            flex-direction: column;
            gap: 14px;
            margin: 15px 0 10px;
        }

        .link-item {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 14px;
            padding: 16px 24px;
            background: rgba(255, 255, 255, 0.03);
            border-radius: 60px;
            border: 1px solid rgba(255, 255, 255, 0.06);
            color: #d0c8e0;
            text-decoration: none;
            font-weight: 400;
            letter-spacing: 1.5px;
            transition: all 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
            font-size: 1.05rem;
            position: relative;
            overflow: hidden;
        }

        .link-item::after {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.05) 0%, transparent 70%);
            opacity: 0;
            transition: opacity 0.4s;
        }

        .link-item:hover {
            transform: translateY(-5px) scale(1.03);
            background: rgba(255, 255, 255, 0.08);
            border-color: rgba(180, 130, 255, 0.3);
            box-shadow: 0 15px 40px -10px rgba(0, 0, 0, 0.7);
            color: #f5f0ff;
        }

        .link-item:hover::after {
            opacity: 1;
        }

        .link-item .icon {
            font-size: 1.6rem;
            width: 35px;
            text-align: center;
            transition: 0.3s;
        }

        .link-item:hover .icon {
            transform: rotate(-8deg) scale(1.15);
        }

        /* فوتر */
        .footer {
            margin-top: 28px;
            color: #5a4a7a;
            font-size: 0.8rem;
            letter-spacing: 3px;
            opacity: 0.5;
            animation: footerPulse 3s ease-in-out infinite;
        }

        @keyframes footerPulse {
            0%, 100% { opacity: 0.3; }
            50% { opacity: 0.6; }
        }

        /* اشک‌های بارانی */
        .tear-drop {
            position: fixed;
            font-size: 16px;
            opacity: 0.08;
            pointer-events: none;
            animation: tearFall linear infinite;
            z-index: 1;
        }

        @keyframes tearFall {
            0% { transform: translateY(-10vh) rotate(0deg) scale(0.5); opacity: 0; }
            10% { opacity: 0.08; }
            90% { opacity: 0.08; }
            100% { transform: translateY(110vh) rotate(720deg) scale(1); opacity: 0; }
        }

        /* حلقه‌های نورانی */
        .glow-ring {
            position: fixed;
            border-radius: 50%;
            filter: blur(100px);
            pointer-events: none;
            animation: ringFloat 8s ease-in-out infinite alternate;
        }

        .ring1 {
            width: 500px;
            height: 500px;
            background: #4a1a7a;
            top: -200px;
            right: -200px;
            opacity: 0.15;
        }

        .ring2 {
            width: 400px;
            height: 400px;
            background: #1a3a8a;
            bottom: -150px;
            left: -150px;
            opacity: 0.12;
            animation-delay: 3s;
        }

        .ring3 {
            width: 300px;
            height: 300px;
            background: #8a1a3a;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            opacity: 0.08;
            animation-delay: 6s;
        }

        @keyframes ringFloat {
            0% { transform: translate(0, 0) scale(1); }
            100% { transform: translate(30px, -30px) scale(1.2); }
        }
    </style>
</head>
<body>

    <!-- حلقه‌های نورانی -->
    <div class="glow-ring ring1"></div>
    <div class="glow-ring ring2"></div>
    <div class="glow-ring ring3"></div>

    <!-- ستاره‌ها -->
    <div class="stars"></div>

    <!-- کارت اصلی -->
    <div class="card">
        <span class="sad-emoji">😔</span>
        <h1>Zubair</h1>
        <div class="subtitle">✦ در دل شب، روشنایی‌ست ✦</div>

        <div class="links">
            <a href="https://instagram.com" target="_blank" class="link-item">
                <span class="icon">📸</span> Instagram
            </a>
            <a href="https://tiktok.com" target="_blank" class="link-item">
                <span class="icon">🎵</span> TikTok
            </a>
            <a href="https://capcut.com" target="_blank" class="link-item">
                <span class="icon">🎬</span> CapCut
            </a>
            <a href="https://telegram.org" target="_blank" class="link-item">
                <span class="icon">✈️</span> Telegram
            </a>
        </div>

        <div class="footer">✦ ساخته شده با ❤️ توسط Zubair ✦</div>
    </div>

    <!-- ایجاد اشک‌های بارانی با جاوااسکریپت -->
    <script>
        (function createRain() {
            const tears = ['💧', '•', '✦', '·'];
            for (let i = 0; i < 40; i++) {
                const drop = document.createElement('div');
                drop.className = 'tear-drop';
                drop.textContent = tears[i % tears.length];
                drop.style.left = Math.random() * 100 + 'vw';
                drop.style.fontSize = (10 + Math.random() * 20) + 'px';
                drop.style.animationDuration = (8 + Math.random() * 25) + 's';
                drop.style.animationDelay = (Math.random() * 20) + 's';
                drop.style.opacity = 0.03 + Math.random() * 0.08;
                document.body.appendChild(drop);
            }
        })();
    </script>

</body>
</html>
