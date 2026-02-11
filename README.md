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
            --accent: #007AFF; /* Классический Apple Blue */
            --font: -apple-system, BlinkMacSystemFont, "SF Pro Display", "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
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

        /* Задний фон с мягким свечением */
        .glow {
            position: absolute;
            width: 300px;
            height: 300px;
            background: var(--accent);
            filter: blur(150px);
            opacity: 0.15;
            z-index: 0;
            animation: move 10s infinite alternate ease-in-out;
        }

        @keyframes move {
            from { transform: translate(-20%, -20%); }
            to { transform: translate(20%, 20%); }
        }

        .container {
            position: relative;
            z-index: 1;
            text-align: center;
            padding: 20px;
            width: 100%;
            max-width: 400px;
        }

        /* Шапка */
        .header {
            margin-bottom: 40px;
            opacity: 0;
            animation: fadeInUp 0.8s forwards ease-out;
        }

        .nickname {
            font-size: 1.2rem;
            font-weight: 600;
            letter-spacing: -0.02em;
        }

        .sub-header {
            color: var(--text-secondary);
            font-size: 0.9rem;
            margin-top: 5px;
        }

        /* Список правил */
        .rules-list {
            list-style: none;
        }

        .rule-item {
            background: var(--card-bg);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.05);
            padding: 18px;
            border-radius: 22px;
            margin-bottom: 12px;
            font-size: 1rem;
            font-weight: 400;
            opacity: 0;
            transform: translateY(20px);
            transition: transform 0.3s ease, background 0.3s ease;
        }

        .rule-item:hover {
            background: rgba(255, 255, 255, 0.07);
            transform: scale(1.02);
        }

        /* Анимация появления элементов по очереди */
        .rule-item:nth-child(1) { animation: fadeInUp 0.8s 0.2s forwards; }
        .rule-item:nth-child(2) { animation: fadeInUp 0.8s 0.4s forwards; }
        .rule-item:nth-child(3) { animation: fadeInUp 0.8s 0.6s forwards; }
        .rule-item:nth-child(4) { animation: fadeInUp 0.8s 0.8s forwards; }

        .red-flag {
            color: #FF453A; /* iOS Red */
            font-weight: 500;
        }

        /* Подпись внизу */
        .footer {
            margin-top: 40px;
            font-size: 0.75rem;
            color: var(--text-secondary);
            opacity: 0;
            animation: fadeIn 2s 1.2s forwards;
        }

        @keyframes fadeInUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeIn {
            to { opacity: 1; }
        }

        /* Эффект касания для мобилок */
        .rule-item:active {
            transform: scale(0.95);
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
            <div class="rule-item">Хочешь дела? Пиши по делу.</div>
        </div>

        <div class="footer">
            Design inspired by iOS 26 Visual Language
        </div>
    </div>

</body>
</html>
