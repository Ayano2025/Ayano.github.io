# aefbi.github.io
index.html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>@aefbi | Инфо</title>
    <style>
        :root {
            --bg: #050505;
            --card-bg: rgba(255, 255, 255, 0.03);
            --text-main: #ffffff;
            --text-secondary: rgba(255, 255, 255, 0.4);
            --accent: #007AFF; 
            --font: -apple-system, BlinkMacSystemFont, "SF Pro Display", "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            background-color: var(--bg);
            color: var(--text-main);
            font-family: var(--font);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            overflow: hidden;
            -webkit-font-smoothing: antialiased;
        }

        .glow {
            position: absolute;
            width: 350px;
            height: 350px;
            background: var(--accent);
            filter: blur(160px);
            opacity: 0.12;
            z-index: 0;
            animation: move 12s infinite alternate ease-in-out;
        }

        @keyframes move {
            from { transform: translate(-30%, -10%); }
            to { transform: translate(30%, 10%); }
        }

        .container {
            position: relative;
            z-index: 1;
            text-align: center;
            padding: 24px;
            width: 100%;
            max-width: 400px;
        }

        .header {
            margin-bottom: 40px;
            opacity: 0;
            animation: fadeInUp 0.8s forwards ease-out;
        }

        .nickname {
            font-size: 1.4rem;
            font-weight: 600;
            letter-spacing: -0.03em;
        }

        .sub-header {
            color: var(--text-secondary);
            font-size: 0.95rem;
            margin-top: 6px;
        }

        .rules-list {
            list-style: none;
            margin-bottom: 30px;
        }

        .rule-item {
            background: var(--card-bg);
            backdrop-filter: blur(25px);
            -webkit-backdrop-filter: blur(25px);
            border: 1px solid rgba(255, 255, 255, 0.06);
            padding: 18px;
            border-radius: 20px;
            margin-bottom: 12px;
            font-size: 1rem;
            opacity: 0;
            transform: translateY(20px);
        }

        .red-flag {
            color: #FF453A;
            font-weight: 500;
        }

        /* Кнопка Telegram */
        .tg-link {
            display: flex;
            align-items: center;
            justify-content: center;
            background: var(--accent);
            color: white;
            text-decoration: none;
            padding: 16px;
            border-radius: 20px;
            font-weight: 600;
            font-size: 1rem;
            transition: transform 0.2s ease, filter 0.2s ease;
            opacity: 0;
            transform: translateY(20px);
            animation: fadeInUp 0.8s 1s forwards ease-out; /* Появляется последней */
            box-shadow: 0 10px 30px rgba(0, 122, 255, 0.2);
        }

        .tg-link:active {
            transform: scale(0.96);
            filter: brightness(1.1);
        }

        /* Анимации появления */
        .rule-item:nth-child(1) { animation: fadeInUp 0.8s 0.2s forwards; }
        .rule-item:nth-child(2) { animation: fadeInUp 0.8s 0.4s forwards; }
        .rule-item:nth-child(3) { animation: fadeInUp 0.8s 0.6s forwards; }
        .rule-item:nth-child(4) { animation: fadeInUp 0.8s 0.8s forwards; }

        @keyframes fadeInUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .footer {
            margin-top: 40px;
            font-size: 0.7rem;
            color: var(--text-secondary);
            letter-spacing: 0.05em;
            text-transform: uppercase;
            opacity: 0;
            animation: fadeIn 2s 1.5s forwards;
        }

        @keyframes fadeIn {
            to { opacity: 1; }
        }
    </style>
</head>
<body>

    <div class="glow"></div>

    <div class="container">
        <div class="header">
            <div class="nickname">@aefbi</div>
            <div class="sub-header">и зачем ему писать?</div>
        </div>

        <div class="rules-list">
            <div class="rule-item">Не пиши по херне</div>
            <div class="rule-item red-flag">Угрозы — ЧС</div>
            <div class="rule-item">Уважай моё и своё время</div>
            <div class="rule-item">Хочешь дела? Пиши по делу</div>
        </div>

        <a href="https://t.me/aefbi" class="tg-link" target="_blank">
            Написать в Telegram
        </a>

        <div class="footer">
            Personal Space • 2026
        </div>
    </div>

</body>
</html>
