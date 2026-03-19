# infootdel1.github.io
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CyberSecurity: Гид для школьников</title>
    <style>
        :root {
            --bg-color: #0f172a;
            --sidebar-color: #1e293b;
            --text-color: #e2e8f0;
            --accent-color: #0ea5e9;
            --success-color: #22c55e;
            --danger-color: #ef4444;
            --card-bg: #334155;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            display: flex;
            height: 100vh;
            overflow: hidden;
        }

        /* Навигация (Сайдбар) */
        nav {
            width: 250px;
            background-color: var(--sidebar-color);
            display: flex;
            flex-direction: column;
            padding: 20px;
            border-right: 1px solid #475569;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--accent-color);
            margin-bottom: 40px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .nav-btn {
            background: none;
            border: none;
            color: #94a3b8;
            text-align: left;
            padding: 15px;
            cursor: pointer;
            font-size: 1rem;
            border-radius: 8px;
            transition: 0.3s;
            margin-bottom: 5px;
        }

        .nav-btn:hover, .nav-btn.active {
            background-color: var(--accent-color);
            color: white;
            transform: translateX(5px);
        }

        /* Основной контент */
        main {
            flex: 1;
            padding: 40px;
            overflow-y: auto;
            position: relative;
        }

        .section {
            display: none;
            animation: fadeIn 0.5s ease;
            max-width: 900px;
            margin: 0 auto;
        }

        .section.active {
            display: block;
        }

        h1 {
            margin-bottom: 20px;
            font-size: 2.5rem;
            border-bottom: 2px solid var(--accent-color);
            display: inline-block;
            padding-bottom: 10px;
        }

        /* Карточки */
        .card {
            background-color: var(--card-bg);
            padding: 25px;
            border-radius: 12px;
            margin-bottom: 20px;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
        }

        /* Инструменты */
        input[type="text"], input[type="password"] {
            width: 100%;
            padding: 12px;
            border-radius: 6px;
            border: 1px solid #475569;
            background-color: #0f172a;
            color: white;
            margin-bottom: 10px;
            font-size: 1rem;
        }

        button.action-btn {
            background-color: var(--accent-color);
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 6px;
            cursor: pointer;
            font-weight: bold;
            transition: 0.2s;
        }

        button.action-btn:hover {
            opacity: 0.9;
        }

        /* Индикатор пароля */
        .strength-meter {
            height: 10px;
            background-color: #475569;
            border-radius: 5px;
            margin-top: 10px;
            overflow: hidden;
        }
        .strength-bar {
            height: 100%;
            width: 0%;
            transition: 0.3s;
        }

        /* Фишинг тест */
        .email-card {
            border: 1px solid #475569;
            padding: 15px;
            margin-bottom: 10px;
            border-radius: 8px;
            background: #1e293b;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .quiz-options {
            display: flex;
            gap: 10px;
        }

        .feedback {
            margin-top: 10px;
            font-weight: bold;
        }

        /* Чеклист */
        .checklist-item {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 10px;
            border-bottom: 1px solid #475569;
        }
        .checklist-item input {
            width: 20px;
            height: 20px;
            cursor: pointer;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Адаптив для мобильных */
        @media (max-width: 768px) {
            body { flex-direction: column; }
            nav { width: 100%; height: auto; flex-direction: row; overflow-x: auto; padding: 10px; }
            .logo { display: none; }
            .nav-btn { margin: 0 5px; white-space: nowrap; }
            main { padding: 20px; }
        }
    </style>
</head>
<body>

    <!-- Навигация -->
    <nav>
        <div class="logo">🛡️ CyberGuard</div>
        <button class="nav-btn active" onclick="showSection('dashboard')">🏠 Главная</button>
        <button class="nav-btn" onclick="showSection('passwords')">🔑 Пароли</button>
        <button class="nav-btn" onclick="showSection('phishing')">🎣 Фишинг-тест</button>
        <button class="nav-btn" onclick="showSection('checklist')">✅ Чек-лист</button>
    </nav>

    <!-- Контент -->
    <main>
        
        <!-- Секция: Главная -->
        <div id="dashboard" class="section active">
            <h1>Добро пожаловать, Агент</h1>
            <div class="card">
                <p>Твой уровень цифровой безопасности зависит от твоих действий. Здесь ты найдешь инструменты для защиты своих данных.</p>
                <br>
                <h3>Быстрые факты:</h3>
                <ul>
                    <li style="margin: 10px 0;">🔒 80% взломов происходят из-за слабых паролей.</li>
                    <li style="margin: 10px 0;">📧 Фишинг — это когда мошенники притворяются друзьями или банками.</li>
                    <li style="margin: 10px 0;">🕵️ Социальная инженерия — это манипуляция людьми, а не компьютерами.</li>
                </ul>
            </div>
            <div style="display: flex; gap: 20px;">
                <div class="card" style="flex: 1; text-align: center; border: 1px solid var(--accent-color);">
                    <h2>Твоя цель</h2>
                    <p>Пройди тесты и укрепи свои знания.</p>
                </div>
                <div class="card" style="flex: 1; text-align: center; border: 1px solid var(--danger-color);">
                    <h2>Опасность</h2>
                    <p>Не переходи по ссылкам от незнакомцев!</p>
                </div>
            </div>
        </div>

        <!-- Секция: Пароли -->
        <div id="passwords" class="section">
            <h1>Лаборатория Паролей</h1>
            <div class="card">
                <p>Введи пароль, чтобы проверить его надежность. <b>Никогда не используй реальные пароли на чужих сайтах!</b></p>
                <input type="text" id="passInput" placeholder="Введите пароль..." oninput="checkPassword()">
                <div class="strength-meter">
                    <div id="strengthBar" class="strength-bar"></div>
                </div>
                <p id="passFeedback" style="margin-top: 10px; font-weight: bold;">Ожидание ввода...</p>
            </div>
            
            <div class="card">
                <h3>Правила крутого пароля:</h3>
                <ul style="margin-left: 20px; margin-top: 10px;">
                    <li>Длина минимум 12 символов.</li>
                    <li>Смешивай буквы, цифры и символы (!@#).</li>
                    <li>Не используй дату рождения или имя питомца.</li>
                    <li>Используй разные пароли для разных сайтов.</li>
                </ul>
            </div>
        </div>

        <!-- Секция: Фишинг -->
        <div id="phishing" class="section">
            <h1>Детектор Фишинга</h1>
            <p style="margin-bottom: 20px;">Определи, является ли сообщение безопасным или это попытка обмана.</p>
            
            <div id="quizContainer">
                <!-- Сюда генерируются вопросы через JS -->
            </div>
            
            <div class="card" style="margin-top: 20px;">
                <h3>Совет детектива:</h3>
                <p>Всегда проверяй адрес отправителя. Если банк пишет с адреса <code>@gmail.com</code> — это 100% мошенники.</p>
            </div>
        </div>

        <!-- Секция: Чек-лист -->
        <div id="checklist" class="section">
            <h1>Твой щит безопасности</h1>
            <div class="card">
                <p>Отмечай пункты, которые ты уже выполнил. Данные сохраняются в браузере.</p>
                <div id="checklistContainer">
                    <!-- Чекбокс генерируется через JS -->
                </div>
                <button class="action-btn" style="margin-top: 20px;" onclick="resetChecklist()">Сбросить прогресс</button>
            </div>
        </div>

    </main>

    <script>
        // --- Логика Навигации ---
        function showSection(sectionId) {
            // Скрываем все секции
            document.querySelectorAll('.section').forEach(sec => sec.classList.remove('active'));
            document.querySelectorAll('.nav-btn').forEach(btn => btn.classList.remove('active'));
            
            // Показываем нужную
            document.getElementById(sectionId).classList.add('active');
            
            // Подсвечиваем кнопку
            const activeBtn = Array.from(document.querySelectorAll('.nav-btn')).find(b => b.getAttribute('onclick').includes(sectionId));
            if(activeBtn) activeBtn.classList.add('active');
        }

        // --- Логика Проверки Пароля ---
        function checkPassword() {
            const input = document.getElementById('passInput').value;
            const bar = document.getElementById('strengthBar');
            const feedback = document.getElementById('passFeedback');
            
            let strength = 0;
            if (input.length > 8) strength += 20;
            if (input.length > 12) strength += 20;
            if (/[A-Z]/.test(input)) strength += 20;
            if (/[0-9]/.test(input)) strength += 20;
            if (/[^A-Za-z0-9]/.test(input)) strength += 20;

            bar.style.width = strength + '%';
            
            if (strength < 40) {
                bar.style.backgroundColor = 'var(--danger-color)';
                feedback.innerText = "Слабый! Хакер взломает за секунды.";
                feedback.style.color = 'var(--danger-color)';
            } else if (strength < 80) {
                bar.style.backgroundColor = '#eab308'; // Yellow
                feedback.innerText = "Нормально, но можно лучше.";
                feedback.style.color = '#eab308';
            } else {
                bar.style.backgroundColor = 'var(--success-color)';
                feedback.innerText = "Отлично! Этот пароль надежен.";
                feedback.style.color = 'var(--success-color)';
            }
        }

        // --- Логика Фишинг-теста ---
        const phishingQuestions = [
            {
                text: "Письмо от 'Администрации ВКонтакте': 'Срочно! Ваш аккаунт будет удален. Перейдите по ссылке, чтобы подтвердить личность.'",
                isSafe: false,
                explanation: "Это фишинг! Администрация не требует переходить по ссылкам для продления аккаунта. Они создают панику."
            },
            {
                text: "Сообщение от друга в мессенджере: 'Смотри, это ты на фото?' + ссылка на странный сайт.",
                isSafe: false,
                explanation: "Друга могли взломать. Не переходи по ссылкам, даже от друзей, если сообщение странное."
            },
            {
                text: "Уведомление от Steam о покупке игры, которую ты не заказывал.",
                isSafe: true,
                explanation: "Это нормально, но нужно проверить историю покупок в официальном приложении, а не в письме."
            },
            {
                text: "Письмо от банка с темой 'Ваша карта заблокирована' и требованием ввести пин-код на сайте.",
                isSafe: false,
                explanation: "Банк никогда не просит пин-код или коды из СМС на сайтах. Это кража данных."
            }
        ];

        const quizContainer = document.getElementById('quizContainer');

        function renderQuiz() {
            quizContainer.innerHTML = '';
            phishingQuestions.forEach((q, index) => {
                const card = document.createElement('div');
                card.className = 'email-card';
                card.innerHTML = `
                    <div style="flex:1; margin-right: 15px;">
                        <strong>Сценарий ${index + 1}:</strong> ${q.text}
                    </div>
                    <div class="quiz-options">
                        <button class="action-btn" style="background-color: var(--success-color);" onclick="checkPhishing(${index}, true)">Безопасно</button>
                        <button class="action-btn" style="background-color: var(--danger-color);" onclick="checkPhishing(${index}, false)">Опасно</button>
                    </div>
                `;
                
                const feedbackDiv = document.createElement('div');
                feedbackDiv.id = `feedback-${index}`;
                feedbackDiv.className = 'feedback';
                card.appendChild(feedbackDiv);
                
                quizContainer.appendChild(card);
            });
        }

        function checkPhishing(index, userSaidSafe) {
            const q = phishingQuestions[index];
            const feedbackEl = document.getElementById(`feedback-${index}`);
            const isCorrect = (userSaidSafe === q.isSafe);

            if (isCorrect) {
                feedbackEl.style.color = 'var(--success-color)';
                feedbackEl.innerText = "Верно! " + q.explanation;
            } else {
                feedbackEl.style.color = 'var(--danger-color)';
                feedbackEl.innerText = "Ошибка! " + q.explanation;
            }
        }

        // --- Логика Чек-листа (с сохранением в LocalStorage) ---
        const checklistItems = [
            "Установил антивирус на компьютер/телефон",
            "Включил двухфакторную аутентификацию (2FA) в соцсетях",
            "Не использую один пароль для всех сайтов",
            "Регулярно обновляю приложения и систему",
            "Не публикую фото документов или билетов в интернете",
            "Проверяю настройки приватности в соцсетях"
        ];

        function renderChecklist() {
            const container = document.getElementById('checklistContainer');
            container.innerHTML = '';
            
            const savedData = JSON.parse(localStorage.getItem('cyberChecklist')) || [];

            checklistItems.forEach((item, index) => {
                const isChecked = savedData.includes(index);
                const div = document.createElement('div');
                div.className = 'checklist-item';
                div.innerHTML = `
                    <input type="checkbox" ${isChecked ? 'checked' : ''} onchange="toggleCheck(${index})">
                    <span style="${isChecked ? 'text-decoration: line-through; color: #94a3b8;' : ''}">${item}</span>
                `;
                container.appendChild(div);
            });
        }

        function toggleCheck(index) {
            let savedData = JSON.parse(localStorage.getItem('cyberChecklist')) || [];
            
            if (savedData.includes(index)) {
                savedData = savedData.filter(i => i !== index);
            } else {
                savedData.push(index);
            }
            
            localStorage.setItem('cyberChecklist', JSON.stringify(savedData));
            renderChecklist();
        }

        function resetChecklist() {
            localStorage.removeItem('cyberChecklist');
            renderChecklist();
        }

        // Инициализация при загрузке
        renderQuiz();
        renderChecklist();

    </script>
</body>
</html>
