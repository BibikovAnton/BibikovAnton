<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bibikov Anton</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            color: #fff;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            overflow-x: hidden;
            padding: 20px;
        }
        
        .container {
            text-align: center;
            max-width: 800px;
            width: 100%;
        }
        
        .gif-container {
            margin: 20px 0;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
        }
        
        .gif-container img {
            max-width: 100%;
            height: auto;
            display: block;
        }
        
        .name {
            font-size: 3.5rem;
            font-weight: 700;
            margin: 30px 0;
            color: transparent;
            background: linear-gradient(45deg, #ff8a00, #e52e71, #5c6bc0, #66bb6a);
            background-size: 300% 300%;
            -webkit-background-clip: text;
            background-clip: text;
            animation: gradientShift 8s ease infinite;
            text-shadow: 0 0 15px rgba(255, 255, 255, 0.2);
        }
        
        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        .telegram-btn {
            display: inline-block;
            background: linear-gradient(45deg, #2CA5E0, #0088cc);
            color: white;
            padding: 12px 28px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.2rem;
            margin-top: 20px;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(44, 165, 224, 0.4);
        }
        
        .telegram-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(44, 165, 224, 0.6);
        }
        
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            overflow: hidden;
        }
        
        .particle {
            position: absolute;
            background: rgba(255, 255, 255, 0.5);
            border-radius: 50%;
            animation: float 15s infinite linear;
        }
        
        @keyframes float {
            0% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(-100px) rotate(720deg);
                opacity: 0;
            }
        }
        
        @media (max-width: 768px) {
            .name {
                font-size: 2.5rem;
            }
        }
        
        @media (max-width: 480px) {
            .name {
                font-size: 2rem;
            }
            
            .telegram-btn {
                padding: 10px 20px;
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <div class="particles" id="particles"></div>
    
    <div class="container">
        <div class="gif-container">
            <img src="https://i.pinimg.com/originals/84/da/da/84dada0a5dcfd790700df3dd87897aef.gif" alt="Анимированный фон">
        </div>
        
        <h1 class="name">Bibikov Anton</h1>
        
        <a href="https://t.me/AntonBib" target="_blank" class="telegram-btn">
            Telegram @AntonBib
        </a>
    </div>

    <script>
        // Создание частиц для фона
        document.addEventListener('DOMContentLoaded', function() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = 30;
            
            for (let i = 0; i < particleCount; i++) {
                createParticle();
            }
            
            function createParticle() {
                const particle = document.createElement('div');
                particle.classList.add('particle');
                
                const size = Math.random() * 10 + 5;
                const posX = Math.random() * 100;
                const duration = Math.random() * 10 + 10;
                const delay = Math.random() * 5;
                
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                particle.style.left = `${posX}vw`;
                particle.style.animationDuration = `${duration}s`;
                particle.style.animationDelay = `${delay}s`;
                
                particlesContainer.appendChild(particle);
                
                // Пересоздание частицы после завершения анимации
                setTimeout(() => {
                    particle.remove();
                    createParticle();
                }, (duration + delay) * 1000);
            }
        });
    </script>
</body>
</html>

###

<h3 align="left">👨‍💻 Обо мне</h3>

###

👋 Привет! Меня зовут Антон

Я увлекаюсь бэкенд-разработкой на Go (Golang). Активно погружаюсь в коммерческую разработку: выполняю пет-проекты с реальными сценариями использования, изучаю best practices и работаю с популярным для Go стеком (Docker, PostgreSQL, Kafka, gRPC). Создаю полноценные сервисы — от проектирования архитектуры и API до реализации бизнес-логики, тестирования и деплоя.

🛠️ Мой Технологический Стек

Языки: Go, SQL (базовый Python для скриптов)
Фреймворки и библиотеки: Gin, GORM, стандартная библиотека Go (net/http, context, testing)
Базы данных: PostgreSQL, Redis
Инфраструктура: Docker, Docker Compose, Git, CI/CD (GitHub Actions)
Брокеры сообщений и инструменты: Apache Kafka, gRPC, REST API
Изучаю/Осваиваю: Kubernetes, продвинутые паттерны проектирования, микросервисная архитектура

📈 Мои Принципы Разработки

Чистый и читаемый код: Стремлюсь писать код, который легко поддерживать и понимать.
Тестирование: Пишу unit- и интеграционные тесты для обеспечения надежности кода.
Оптимизация: Интересуюсь вопросами производительности и эффективности алгоритмов.
Постоянное обучение: Регулярно решаю задачи на LeetCode, читаю технические блоги и смотрю доклады (GopherCon).

📫 Как со мной связаться

Email: bibikovanton.m@gmail.com

Цель: Стремлюсь к профессиональному росту в IT, хочу работать над сложными высоконагруженными проектами и развиваться как востребованный Go-разработчик.



<div align="center">
  <img src="https://raw.githubusercontent.com/BibikovAnton/BibikovAnton/main/assets/github-snake.svg" width="600" alt="contribution snake"/>
</div>

###
