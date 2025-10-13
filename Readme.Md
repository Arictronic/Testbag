<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Atom-Assistant - AI помощник для инвестиционных презентаций</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        .header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 30px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .logo {
            font-size: 3.5em;
            font-weight: bold;
            background: linear-gradient(135deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 10px;
        }
        
        .tagline {
            font-size: 1.4em;
            color: #666;
            margin-bottom: 30px;
        }
        
        .badges {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
            margin-bottom: 30px;
        }
        
        .badge {
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9em;
            font-weight: 600;
            text-decoration: none;
            transition: transform 0.3s ease;
        }
        
        .badge:hover {
            transform: translateY(-2px);
        }
        
        .badge.python {
            background: #3776AB;
            color: white;
        }
        
        .badge.fastapi {
            background: #009688;
            color: white;
        }
        
        .badge.streamlit {
            background: #FF4B4B;
            color: white;
        }
        
        .badge.license {
            background: #FFD700;
            color: #333;
        }
        
        .main-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .card {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: transform 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-5px);
        }
        
        .card h2 {
            color: #4a5568;
            margin-bottom: 20px;
            font-size: 1.5em;
            border-bottom: 2px solid #e2e8f0;
            padding-bottom: 10px;
        }
        
        .card h3 {
            color: #2d3748;
            margin: 20px 0 10px 0;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }
        
        .feature {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .feature-icon {
            font-size: 2.5em;
            margin-bottom: 15px;
        }
        
        .tech-stack {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }
        
        .tech-item {
            background: #f7fafc;
            padding: 15px;
            border-radius: 10px;
            border-left: 4px solid #667eea;
        }
        
        .code-block {
            background: #2d3748;
            color: #e2e8f0;
            padding: 20px;
            border-radius: 10px;
            font-family: 'Courier New', monospace;
            margin: 15px 0;
            overflow-x: auto;
        }
        
        .file-structure {
            background: #1a202c;
            color: #e2e8f0;
            padding: 20px;
            border-radius: 10px;
            font-family: 'Courier New', monospace;
            margin: 15px 0;
            line-height: 1.8;
        }
        
        .directory {
            color: #63b3ed;
        }
        
        .file {
            color: #68d391;
        }
        
        .footer {
            text-align: center;
            padding: 40px;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            margin-top: 30px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .heart {
            color: #e53e3e;
        }
        
        @media (max-width: 768px) {
            .main-content {
                grid-template-columns: 1fr;
            }
            
            .features-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div class="logo">🦾 Atom-Assistant</div>
            <div class="tagline">AI-помощник для автоматической генерации инвестиционных презентаций</div>
            
            <div class="badges">
                <span class="badge python">Python 3.9+</span>
                <span class="badge fastapi">FastAPI 0.104+</span>
                <span class="badge streamlit">Streamlit 1.28+</span>
                <span class="badge license">MIT License</span>
            </div>
            
            <p>Умный веб-сервис для анализа документов и создания презентаций в корпоративном стиле Росатома</p>
        </div>

        <div class="features-grid">
            <div class="feature">
                <div class="feature-icon">📁</div>
                <h3>Мультиформатный парсинг</h3>
                <p>Поддержка PDF, DOCX, XLSX, PPTX документов</p>
            </div>
            <div class="feature">
                <div class="feature-icon">🤖</div>
                <h3>AI-анализ Qwen-1.7B</h3>
                <p>Интеллектуальная обработка контента</p>
            </div>
            <div class="feature">
                <div class="feature-icon">🎨</div>
                <h3>Корпоративный стиль</h3>
                <p>Автоматическое оформление по стандартам Росатома</p>
            </div>
            <div class="feature">
                <div class="feature-icon">⚡</div>
                <h3>Быстрая генерация</h3>
                <p>Создание презентаций за минуты вместо дней</p>
            </div>
        </div>

        <div class="main-content">
            <div class="card">
                <h2>🚀 Быстрый старт</h2>
                
                <h3>Предварительные требования</h3>
                <ul>
                    <li>Python 3.9+</li>
                    <li>Hugging Face API token</li>
                    <li>1 ГБ свободного места</li>
                </ul>

                <h3>Установка</h3>
                <div class="code-block">
git clone https://github.com/your-username/atom-assistant.git<br>
cd atom-assistant<br>
python -m venv venv<br>
source venv/bin/activate  # Linux/MacOS<br>
pip install -r requirements.txt
                </div>

                <h3>Настройка</h3>
                <div class="code-block">
cp .env.example .env<br>
# Добавьте HUGGINGFACEHUB_API_TOKEN в .env файл
                </div>

                <h3>Запуск</h3>
                <div class="code-block">
# Бэкенд (терминал 1)<br>
cd app && uvicorn main:app --reload<br><br>

# Фронтенд (терминал 2)<br>
cd frontend && streamlit run app.py<br><br>

# Открыть в браузере:<br>
http://localhost:8501
                </div>
            </div>

            <div class="card">
                <h2>🛠 Технологический стек</h2>
                
                <h3>Бэкенд</h3>
                <div class="tech-stack">
                    <div class="tech-item">
                        <strong>FastAPI</strong><br>
                        Асинхронный веб-фреймворк
                    </div>
                    <div class="tech-item">
                        <strong>Qwen-1.7B</strong><br>
                        Локальная LLM модель
                    </div>
                    <div class="tech-item">
                        <strong>ChromaDB</strong><br>
                        Векторная база данных
                    </div>
                    <div class="tech-item">
                        <strong>LangChain</strong><br>
                        RAG пайплайн
                    </div>
                </div>

                <h3>Фронтенд</h3>
                <div class="tech-stack">
                    <div class="tech-item">
                        <strong>Streamlit</strong><br>
                        Веб-интерфейс
                    </div>
                    <div class="tech-item">
                        <strong>Python-pptx</strong><br>
                        Генерация презентаций
                    </div>
                </div>

                <h3>Парсинг документов</h3>
                <div class="tech-stack">
                    <div class="tech-item">PyPDF2 / pdfplumber</div>
                    <div class="tech-item">Python-docx</div>
                    <div class="tech-item">Openpyxl</div>
                    <div class="tech-item">Python-pptx</div>
                </div>

                <h3>API Endpoints</h3>
                <div class="code-block">
POST /upload          # Загрузка документов<br>
POST /generate        # Генерация презентации<br>
GET  /presentation/{id} # Получение презентации<br>
PUT  /slides/{id}     # Обновление слайда
                </div>
            </div>
        </div>

        <div class="card">
            <h2>📁 Структура проекта</h2>
            <div class="file-structure">
<span class="directory">atom-assistant/</span><br>
├── <span class="directory">app/</span><br>
│   ├── <span class="file">__init__.py</span><br>
│   ├── <span class="file">main.py</span>                 <span class="comment"># FastAPI приложение</span><br>
│   ├── <span class="directory">api/</span><br>
│   │   ├── <span class="file">__init__.py</span><br>
│   │   ├── <span class="file">endpoints.py</span>       <span class="comment"># Эндпоинты API</span><br>
│   │   └── <span class="file">dependencies.py</span>    <span class="comment"># Зависимости</span><br>
│   ├── <span class="directory">core/</span><br>
│   │   ├── <span class="file">__init__.py</span><br>
│   │   ├── <span class="file">config.py</span>          <span class="comment"># Конфигурация</span><br>
│   │   └── <span class="file">security.py</span>        <span class="comment"># Безопасность</span><br>
│   ├── <span class="directory">services/</span><br>
│   │   ├── <span class="file">__init__.py</span><br>
│   │   ├── <span class="file">parser_service.py</span>  <span class="comment"># Парсинг документов</span><br>
│   │   ├── <span class="file">rag_service.py</span>    <span class="comment"># RAG пайплайн</span><br>
│   │   ├── <span class="file">llm_service.py</span>    <span class="comment"># Работа с Qwen-1.7B</span><br>
│   │   └── <span class="file">presentation_service.py</span> <span class="comment"># Генерация презентаций</span><br>
│   ├── <span class="directory">models/</span><br>
│   │   ├── <span class="file">__init__.py</span><br>
│   │   ├── <span class="file">schemas.py</span>         <span class="comment"># Pydantic схемы</span><br>
│   │   └── <span class="file">database.py</span>        <span class="comment"># Модели БД</span><br>
│   └── <span class="directory">utils/</span><br>
│       ├── <span class="file">__init__.py</span><br>
│       ├── <span class="file">file_handlers.py</span>   <span class="comment"># Обработчики файлов</span><br>
│       └── <span class="file">logger.py</span>         <span class="comment"># Логирование</span><br>
├── <span class="directory">frontend/</span><br>
│   ├── <span class="file">app.py</span>                <span class="comment"># Streamlit приложение</span><br>
│   ├── <span class="directory">components/</span><br>
│   │   ├── <span class="file">file_upload.py</span>    <span class="comment"># Загрузка файлов</span><br>
│   │   └── <span class="file">slide_editor.py</span>   <span class="comment"># Редактор слайдов</span><br>
│   └── <span class="directory">assets/</span><br>
│       └── <span class="file">corporate_template.pptx</span> <span class="comment"># Шаблон Росатома</span><br>
├── <span class="directory">data/</span><br>
│   ├── <span class="directory">uploaded/</span>             <span class="comment"># Временные файлы</span><br>
│   └── <span class="directory">chroma_db/</span>           <span class="comment"># Векторная БД</span><br>
├── <span class="directory">tests/</span><br>
│   ├── <span class="file">__init__.py</span><br>
│   ├── <span class="file">test_parsers.py</span><br>
│   └── <span class="file">test_services.py</span><br>
├── <span class="file">requirements.txt</span><br>
├── <span class="file">Dockerfile</span><br>
└── <span class="file">README.md</span>
            </div>
        </div>

        <div class="main-content">
            <div class="card">
                <h2>🎯 Использование</h2>
                
                <h3>Шаг 1: Загрузка документов</h3>
                <p>Загрузите PDF, DOCX, XLSX, PPTX файлы проекта через веб-интерфейс</p>
                
                <h3>Шаг 2: AI-анализ</h3>
                <p>Система автоматически извлекает ключевую информацию с помощью Qwen-1.7B</p>
                
                <h3>Шаг 3: Генерация</h3>
                <p>Создание презентации в корпоративном стиле Росатома</p>
                
                <h3>Шаг 4: Редактирование</h3>
                <p>Интерактивное редактирование контента перед скачиванием</p>

                <h3>Поддерживаемые форматы</h3>
                <div class="tech-stack">
                    <div class="tech-item">
                        <strong>Входные</strong><br>
                        PDF, DOCX, XLSX, PPTX
                    </div>
                    <div class="tech-item">
                        <strong>Выходные</strong><br>
                        PPTX (Росатом)
                    </div>
                </div>
            </div>

            <div class="card">
                <h2>⚙️ Конфигурация</h2>
                
                <h3>Переменные окружения</h3>
                <div class="code-block">
HUGGINGFACEHUB_API_TOKEN=your_token_here<br>
MODEL_NAME=Qwen/Qwen-1_8B-Chat<br>
CHROMA_DB_PATH=./data/chroma_db<br>
UPLOAD_DIR=./data/uploaded<br>
TEMPLATE_PATH=./frontend/assets/corporate_template.pptx
                </div>

                <h3>Промпты для Qwen-1.7B</h3>
                <div class="code-block">
"project_summary": "Извлеки ключевую информацию...",<br>
"financial_slide": "Создай текст для слайда 'Бюджет'...",<br>
"problem_statement": "Сформулируй проблему и решение..."
                </div>

                <h3>Пример запроса API</h3>
                <div class="code-block">
import requests<br><br>

response = requests.post(<br>
    "http://localhost:8000/generate",<br>
    json={<br>
        "file_paths": ["project.pdf", "financials.xlsx"],<br>
        "template": "corporate",<br>
        "audience": "investment_committee"<br>
    }<br>
)
                </div>
            </div>
        </div>

        <div class="footer">
            <h2>👥 Разработано с <span class="heart">❤️</span> для Росатома</h2>
            <p>В рамках хакатона АТОМИКХАК 3.0</p>
            <p>Команда: 2 Fullstack разработчика + 1 Дизайнер</p>
            <p>📧 Контакты: team@atom-assistant.ru</p>
            <p style="margin-top: 20px; font-size: 0.9em; color: #666;">
                Лицензия MIT • Ускоряем подготовку инвестиционных решений
            </p>
        </div>
    </div>

    <script>
        // Анимация для карточек при скролле
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Применяем анимацию ко всем карточкам и фичам
        document.querySelectorAll('.card, .feature').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(20px)';
            el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(el);
        });
    </script>
</body>
</html>