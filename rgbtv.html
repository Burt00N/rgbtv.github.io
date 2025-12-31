<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>TV Channel Broadcast</title>
    
    <!-- Шрифты -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;800&display=swap" rel="stylesheet">
    
    <!-- Стили плеера Plyr -->
    <link rel="stylesheet" href="https://cdn.plyr.io/3.7.8/plyr.css" />

    <style>
        /* === ЦВЕТОВАЯ СХЕМА: Deep Blue & Snow White === */
        :root {
            --bg-color: #020408;       /* Почти черный, глубокий синий */
            --surface-color: #0a1120;  /* Темно-синяя подложка */
            --primary-color: #00d2ff;  /* Ледяной голубой (акцент) */
            --secondary-color: #005bea;/* Глубокий королевский синий */
            --text-primary: #ffffff;   /* Белоснежный текст */
            --text-secondary: #b0c4de; /* Светло-стальной для описания */
            --radius: 6px;
            
            /* Свечение для фокуса (Smart TV) */
            --focus-glow: 0 0 20px rgba(0, 210, 255, 0.5);
            
            /* Настройки плеера (переопределение Plyr) */
            --plyr-color-main: #00d2ff;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            outline: none;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-primary);
            font-family: 'Montserrat', sans-serif;
            overflow-x: hidden;
            -webkit-font-smoothing: antialiased;
            min-height: 100vh;
        }

        /* Фоновая текстура (легкий шум) */
        body::before {
            content: "";
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.8' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)' opacity='0.04'/%3E%3C/svg%3E");
            pointer-events: none;
            z-index: -1;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* === HEADER === */
        header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 25px 0;
            border-bottom: 1px solid rgba(0, 210, 255, 0.1); /* Тонкая ледяная линия */
            margin-bottom: 30px;
        }

        /* Контейнер для Логотипа */
        .logo-container {
            display: block;
            height: 60px; /* Высота логотипа */
            width: auto;
        }

        /* Сам Логотип (IMG) */
        .channel-logo-img {
            height: 100%;
            width: auto;
            display: block;
            object-fit: contain;
            /* Фильтр для придания логотипу "холодного" оттенка, если нужно. 
               Если ваш лого уже цветной - удалите строку ниже */
            filter: drop-shadow(0 0 5px rgba(255,255,255,0.2)); 
        }

        /* Индикатор LIVE */
        .live-badge {
            display: flex;
            align-items: center;
            gap: 8px;
            background: rgba(0, 91, 234, 0.15);
            padding: 6px 14px;
            border-radius: 4px;
            border: 1px solid var(--secondary-color);
            color: var(--primary-color);
            font-weight: 700;
            font-size: 0.85rem;
            letter-spacing: 1px;
            text-transform: uppercase;
        }

        .live-dot {
            width: 8px;
            height: 8px;
            background-color: var(--primary-color);
            border-radius: 50%;
            box-shadow: 0 0 10px var(--primary-color);
            animation: pulse 2s infinite;
        }

        /* === PLAYER === */
        .player-wrapper {
            width: 100%;
            background: #000;
            border-radius: var(--radius);
            overflow: hidden;
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.6);
            border: 1px solid rgba(255, 255, 255, 0.1);
            margin-bottom: 40px;
            aspect-ratio: 16/9;
        }

        /* Перекраска элементов Plyr под стиль сайта */
        .plyr--full-ui input[type=range] {
            color: var(--primary-color);
        }
        .plyr__control--overlaid {
            background: var(--secondary-color);
        }
        .plyr--video .plyr__control.plyr__tab-focus,
        .plyr--video .plyr__control:hover,
        .plyr--video .plyr__control[aria-expanded=true] {
            background: var(--secondary-color);
        }

        /* === CONTENT INFO === */
        .content-grid {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 30px;
            margin-bottom: 60px;
        }

        .info-card {
            background: var(--surface-color);
            padding: 30px;
            border-radius: var(--radius);
            border: 1px solid rgba(255, 255, 255, 0.05);
            position: relative;
            overflow: hidden;
        }

        /* Ледяной блик сверху карточек */
        .info-card::after {
            content: '';
            position: absolute;
            top: 0; left: 0; width: 100%; height: 2px;
            background: linear-gradient(90deg, transparent, var(--secondary-color), transparent);
        }

        h2 {
            font-size: 1.1rem;
            margin-bottom: 20px;
            color: var(--text-primary);
            text-transform: uppercase;
            letter-spacing: 2px;
            display: flex;
            align-items: center;
            gap: 12px;
            border-bottom: 1px solid rgba(255,255,255,0.1);
            padding-bottom: 10px;
        }

        h2 svg {
            color: var(--primary-color);
        }

        .description {
            line-height: 1.7;
            color: var(--text-secondary);
            font-size: 0.95rem;
        }

        /* Тэги */
        .tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 25px;
        }

        .tag {
            padding: 4px 10px;
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--primary-color);
            font-size: 0.75rem;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            border-radius: 2px;
        }

        /* === SCHEDULE LIST === */
        .schedule-list {
            list-style: none;
        }

        .schedule-item {
            display: flex;
            gap: 15px;
            padding: 15px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
            transition: background 0.2s;
        }

        .schedule-item:last-child { border-bottom: none; }

        .time {
            font-weight: 700;
            color: var(--primary-color);
            font-size: 0.9rem;
            min-width: 50px;
            text-shadow: 0 0 10px rgba(0, 210, 255, 0.3);
        }

        .program strong {
            display: block;
            color: var(--text-primary);
            font-weight: 600;
            margin-bottom: 4px;
            font-size: 0.95rem;
        }
        
        .program span {
            font-size: 0.85rem;
            color: var(--text-secondary);
        }

        /* === FOOTER === */
        footer {
            text-align: center;
            padding: 40px 0;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            color: #556677;
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* === DECORATION LINES === */
        .winter-line {
            height: 3px;
            width: 100%;
            background: linear-gradient(90deg, var(--bg-color) 0%, var(--primary-color) 50%, var(--bg-color) 100%);
            position: fixed;
            top: 0; left: 0; z-index: 100;
            box-shadow: 0 0 15px var(--primary-color);
        }

        /* === SVG ICONS === */
        .icon {
            width: 20px;
            height: 20px;
            fill: currentColor;
        }

        /* === SMART TV FOCUS === */
        :focus-visible {
            outline: none;
            box-shadow: 0 0 0 3px var(--secondary-color), 0 0 20px var(--primary-color);
            border-color: var(--primary-color);
            z-index: 10;
        }
        
        .focusable:focus {
            background-color: rgba(255, 255, 255, 0.05);
        }

        @keyframes pulse {
            0% { opacity: 1; transform: scale(1); }
            50% { opacity: 0.5; transform: scale(0.9); }
            100% { opacity: 1; transform: scale(1); }
        }

        @media (max-width: 768px) {
            .content-grid { grid-template-columns: 1fr; }
            header { padding: 15px 0; }
            .logo-container { height: 45px; }
        }
    </style>
</head>
<body>

    <!-- Декоративная линия сверху -->
    <div class="winter-line"></div>

    <div class="container">
        <!-- HEADER -->
        <header>
            <div class="logo-container">
                <!-- ======================================================= -->
                <!-- СЮДА ВСТАВИТЬ ССЫЛКУ НА PNG (вместо placeholder) -->
                <!-- ======================================================= -->
                <img src="https://s2.radikal.cloud/2025/12/31/1f21eba0a5827f1b712c.png"
                     alt="Channel Logo" 
                     class="channel-logo-img">
            </div>
            
            <div class="live-badge focusable" tabindex="0">
                <div class="live-dot"></div>
                Live Stream
            </div>
        </header>

        <!-- PLAYER -->
        <main>
            <div class="player-wrapper">
                <!-- Плеер Plyr -->
                <video id="player" class="plyr-video" playsinline controls crossorigin>
                    <!-- Источник подгружается JS-ом -->
                </video>
            </div>

            <!-- INFO -->
            <div class="content-grid">
                <!-- Описание -->
                <section class="info-card focusable" tabindex="0">
                    <h2>
                        <svg class="icon" viewBox="0 0 24 24"><path d="M20 2H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V4c0-1.1-.9-2-2-2zm0 14H4V4h16v12zM4 20h16v2H4z"/></svg>
                        Channel Info
                    </h2>
                    <p class="description">
                        Праздничный эфир в формате высокой четкости. Лучшие музыкальные клипы, 
                        документальные фильмы и познавательные программы. Наслаждайтесь 
                        атмосферой зимних праздников вместе с нами. Эфир работает 24/7.
                    </p>
                    <div class="tags">
                        <span class="tag">HD Broadcast</span>
                        <span class="tag">Music</span>
                        <span class="tag">Travel</span>
                        <span class="tag">Science</span>
                    </div>
                </section>

                <!-- Программа -->
                <section class="info-card focusable" tabindex="0">
                    <h2>
                        <svg class="icon" viewBox="0 0 24 24"><path d="M11.99 2C6.47 2 2 6.48 2 12s4.47 10 9.99 10C17.52 22 22 17.52 22 12S17.52 2 11.99 2zM12 20c-4.42 0-8-3.58-8-8s3.58-8 8-8 8 3.58 8 8-3.58 8-8 8zm.5-13H11v6l5.25 3.15.75-1.23-4.5-2.67z"/></svg>
                        Timeline
                    </h2>
                    <ul class="schedule-list">
                        <li class="schedule-item">
                            <span class="time">ON AIR</span>
                            <div class="program">
                                <strong>Winter Holidays Mix</strong>
                                <span>Music & Entertainment</span>
                            </div>
                        </li>
                        <li class="schedule-item">
                            <span class="time">15:00</span>
                            <div class="program">
                                <strong>Discovery: Frozen Planet</strong>
                                <span>Documentary</span>
                            </div>
                        </li>
                        <li class="schedule-item">
                            <span class="time">17:45</span>
                            <div class="program">
                                <strong>HBO Special</strong>
                                <span>Concert Series</span>
                            </div>
                        </li>
                    </ul>
                </section>
            </div>
        </main>

        <!-- FOOTER -->
        <footer>
            <p>BROADCAST SIGNAL © 2025. SECURE CONNECTION.</p>
        </footer>
    </div>

    <!-- Библиотеки -->
    <script src="https://cdn.jsdelivr.net/npm/hls.js@latest"></script>
    <script src="https://cdn.plyr.io/3.7.8/plyr.js"></script>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const video = document.getElementById('player');
            const source = 'http://194.87.214.51/hls/rgbtv.m3u8';
            
            // Настройки плеера
            const defaultOptions = {
                controls: ['play-large', 'play', 'mute', 'volume', 'settings', 'pip', 'fullscreen'],
                ratio: '16:9',
                autoplay: true, // Попытка автозапуска
                muted: true     // Автозапуск обычно требует мута
            };

            if (Hls.isSupported()) {
                const hls = new Hls({ debug: false });
                hls.loadSource(source);
                hls.attachMedia(video);
                
                hls.on(Hls.Events.MEDIA_ATTACHED, function () {
                    window.player = new Plyr(video, defaultOptions);
                    // Попытка запуска
                    video.play().catch(() => {
                        // Если браузер блокирует автоплей
                        window.player.muted = true;
                        window.player.play();
                    });
                });
                
                // Обработка ошибок
                hls.on(Hls.Events.ERROR, function (event, data) {
                    if (data.fatal) {
                        switch (data.type) {
                            case Hls.ErrorTypes.NETWORK_ERROR:
                                hls.startLoad();
                                break;
                            case Hls.ErrorTypes.MEDIA_ERROR:
                                hls.recoverMediaError();
                                break;
                            default:
                                hls.destroy();
                                break;
                        }
                    }
                });
            } else if (video.canPlayType('application/vnd.apple.mpegurl')) {
                video.src = source;
                window.player = new Plyr(video, defaultOptions);
                video.play();
            }
        });

        // Улучшение навигации для TV пульта
        window.addEventListener('keydown', (e) => {
            if (['ArrowUp', 'ArrowDown', 'ArrowLeft', 'ArrowRight'].includes(e.key)) {
                document.body.classList.add('user-is-tabbing');
            }
        });
    </script>
</body>
</html>
