<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SoloParaUsted - Frases Románticas Diarias</title>
    
    <!-- Meta tags SEO y Redes Sociales -->
    <meta name="description" content="Una frase romántica única cada día, creada para dedicar y compartir.">
    <meta name="theme-color" content="#fce4ec">
    <meta property="og:title" content="SoloParaUsted - Frases Románticas Diarias">
    <meta property="og:description" content="Una frase romántica única cada día, creada para dedicar y compartir.">
    <meta property="og:type" content="website">

    <!-- Tipografía Google Fonts: Playfair Display (Serif Elegante) + Plus Jakarta Sans (Sans-serif limpia) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,500;0,600;1,400&family=Plus+Jakarta+Sans:wght@400;500;600&display=swap" rel="stylesheet">

    <style>
        /* ==========================================================================
           1. VARIABLES Y DISEÑO DEL TEMA (PALETA DE ROSAS MINIMALISTA)
           ========================================================================== */
        :root {
            /* Paleta Principal de Colores */
            --bg-main: #fff5f7;              /* Fondo suave blanco-rosado */
            --bg-card: #ffffff;              /* Blanco puro para tarjetas */
            --bg-card-subtle: #fce4ec;       /* Rosa pastel claro */
            
            --text-primary: #5c1d30;         /* Vino profundo elegante */
            --text-secondary: #8c4a5c;       /* Rosa terroso / palo de rosa */
            --text-muted: #b07282;           /* Rosa suave apagado */
            
            --accent-pink: #f0829d;          /* Rosa romántico activo */
            --accent-soft: #f8bbd0;          /* Rosa empolvado */
            --accent-hover: #e06382;         /* Rosa acento al hacer hover */
            
            --border-pink: #f8d7e3;          /* Bordes finos rosados */
            --shadow-soft: 0 10px 30px -5px rgba(184, 82, 110, 0.08);
            --shadow-hover: 0 15px 35px -5px rgba(184, 82, 110, 0.15);

            /* Tipografía */
            --font-serif: 'Playfair Display', Georgia, serif;
            --font-sans: 'Plus Jakarta Sans', system-ui, -apple-system, sans-serif;
            
            /* Transiciones */
            --transition-smooth: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        /* Soporte para Modo Oscuro Romántico (Automático según preferencias del usuario) */
        @media (prefers-color-scheme: dark) {
            :root {
                --bg-main: #1a0c12;
                --bg-card: #28131d;
                --bg-card-subtle: #361a27;
                --text-primary: #fce4ec;
                --text-secondary: #f48fb1;
                --text-muted: #ce93d8;
                --border-pink: #4a2133;
                --shadow-soft: 0 10px 30px -5px rgba(0, 0, 0, 0.5);
            }
        }

        /* ==========================================================================
           2. RESETEO Y ESTILOS BASE
           ========================================================================== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            font-family: var(--font-sans);
            background-color: var(--bg-main);
            color: var(--text-primary);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            padding: 2rem 1.25rem;
            line-height: 1.6;
            overflow-x: hidden;
            transition: background-color 0.5s ease;
        }

        /* ==========================================================================
           3. ENCABEZADO Y LOGO (SoloParaUsted)
           ========================================================================== */
        .header {
            text-align: center;
            margin-top: 1rem;
            margin-bottom: 2.5rem;
            animation: fadeInDown 0.8s ease-out;
        }

        /* Contenedor del Logo con Formas de Corazón SVG */
        .logo-container {
            display: inline-flex;
            flex-direction: column;
            align-items: center;
            text-decoration: none;
            color: inherit;
        }

        .logo-icon {
            width: 48px;
            height: 48px;
            margin-bottom: 0.5rem;
            color: var(--accent-pink);
            transition: transform 0.4s ease;
        }

        .logo-container:hover .logo-icon {
            transform: scale(1.1) rotate(-5deg);
        }

        .logo-title {
            font-family: var(--font-serif);
            font-size: 2.8rem;
            font-weight: 600;
            letter-spacing: -0.02em;
            background: linear-gradient(135deg, var(--text-primary) 30%, var(--accent-pink) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            line-height: 1.1;
        }

        .logo-subtitle {
            font-family: var(--font-sans);
            font-size: 0.75rem;
            font-weight: 600;
            letter-spacing: 0.25em;
            text-transform: uppercase;
            color: var(--text-secondary);
            margin-top: 0.5rem;
            opacity: 0.9;
        }

        /* ==========================================================================
           4. TARJETA CENTRAL Y CONTENIDO DE LA FRASE
           ========================================================================== */
        .main-container {
            width: 100%;
            max-width: 680px;
            margin: 0 auto;
            flex-grow: 1;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .quote-card {
            background-color: var(--bg-card);
            border: 1px solid var(--border-pink);
            border-radius: 24px;
            padding: 3.5rem 2.5rem;
            width: 100%;
            text-align: center;
            box-shadow: var(--shadow-soft);
            position: relative;
            transition: var(--transition-smooth);
            animation: fadeInUp 0.9s ease-out;
        }

        .quote-card:hover {
            box-shadow: var(--shadow-hover);
        }

        /* Badge con Fecha */
        .date-badge {
            display: inline-block;
            font-size: 0.85rem;
            font-weight: 500;
            color: var(--text-secondary);
            background-color: var(--bg-card-subtle);
            padding: 0.4rem 1.2rem;
            border-radius: 50px;
            margin-bottom: 2.5rem;
            letter-spacing: 0.02em;
            text-transform: capitalize;
        }

        /* Texto de la Frase */
        .quote-text-container {
            min-height: 140px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 2.5rem;
            position: relative;
        }

        .quote-text {
            font-family: var(--font-serif);
            font-size: 1.85rem;
            font-weight: 500;
            line-height: 1.5;
            color: var(--text-primary);
            font-style: italic;
            transition: opacity 0.4s ease;
        }

        .quote-text::before {
            content: "“";
            color: var(--accent-soft);
            font-size: 3rem;
            line-height: 0;
            vertical-align: -0.4em;
            margin-right: 0.2rem;
        }

        .quote-text::after {
            content: "”";
            color: var(--accent-soft);
            font-size: 3rem;
            line-height: 0;
            vertical-align: -0.4em;
            margin-left: 0.2rem;
        }

        /* Spinner de Carga */
        .loading-spinner {
            display: none;
            width: 36px;
            height: 36px;
            border: 3px solid var(--bg-card-subtle);
            border-top: 3px solid var(--accent-pink);
            border-radius: 50%;
            animation: spin 1s linear infinite;
            margin: 0 auto;
        }

        /* ==========================================================================
           5. BOTONES E INTERACCIONES
           ========================================================================== */
        .actions-group {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            gap: 0.6rem;
            font-family: var(--font-sans);
            font-size: 0.95rem;
            font-weight: 600;
            padding: 0.85rem 1.6rem;
            border-radius: 50px;
            border: 1px solid var(--border-pink);
            background-color: var(--bg-card-subtle);
            color: var(--text-primary);
            cursor: pointer;
            transition: var(--transition-smooth);
            outline: none;
        }

        .btn:hover {
            background-color: var(--accent-pink);
            color: #ffffff;
            border-color: var(--accent-pink);
            transform: translateY(-2px);
        }

        .btn:active {
            transform: translateY(0);
        }

        .btn-icon {
            width: 18px;
            height: 18px;
            fill: none;
            stroke: currentColor;
            stroke-width: 2;
            stroke-linecap: round;
            stroke-linejoin: round;
        }

        /* ==========================================================================
           6. NOTIFICACIÓN TOAST (MENSAJE FLOTANTE AL COPIAR)
           ========================================================================== */
        .toast {
            position: fixed;
            bottom: 2rem;
            left: 50%;
            transform: translateX(-50%) translateY(100px);
            background-color: var(--text-primary);
            color: var(--bg-main);
            padding: 0.75rem 1.5rem;
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 500;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
            opacity: 0;
            transition: var(--transition-smooth);
            z-index: 100;
            pointer-events: none;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .toast.show {
            transform: translateX(-50%) translateY(0);
            opacity: 1;
        }

        /* ==========================================================================
           7. PIE DE PÁGINA (FOOTER)
           ========================================================================== */
        .footer {
            margin-top: 3rem;
            text-align: center;
            font-size: 0.85rem;
            color: var(--text-muted);
            animation: fadeIn 1s ease-out;
        }

        .footer p {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.3rem;
        }

        .footer-heart {
            color: var(--accent-pink);
            display: inline-block;
            animation: pulse 2s infinite;
        }

        /* ==========================================================================
           8. ANIMACIONES CSS
           ========================================================================== */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes fadeInDown {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.15); }
        }

        /* ==========================================================================
           9. ADAPTABILIDAD MOBILE-FIRST (MEDIA QUERIES)
           ========================================================================== */
        @media (max-width: 600px) {
            body {
                padding: 1.5rem 1rem;
            }

            .logo-title {
                font-size: 2.2rem;
            }

            .quote-card {
                padding: 2.5rem 1.5rem;
                border-radius: 20px;
            }

            .quote-text {
                font-size: 1.45rem;
            }

            .actions-group {
                width: 100%;
                flex-direction: column;
            }

            .btn {
                width: 100%;
                justify-content: center;
            }
        }
    </style>
</head>
<body>

    <!-- ENCABEZADO Y LOGO -->
    <header class="header">
        <a href="#" class="logo-container" aria-label="SoloParaUsted - Inicio">
            <!-- Icono de Corazón Elegante de Trazo Suave -->
            <svg class="logo-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round">
                <path d="M20.84 4.61a5.5 5.5 0 0 0-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 0 0-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 0 0 0-7.78z"></path>
            </svg>
            <h1 class="logo-title">SoloParaUsted</h1>
            <p class="logo-subtitle">Frases Románticas Diarias</p>
        </a>
    </header>

    <!-- CONTENIDO PRINCIPAL / TARJETA DE FRASE -->
    <main class="main-container">
        <article class="quote-card">
            <!-- Fecha Formateada -->
            <time id="current-date" class="date-badge" datetime="">Cargando fecha...</time>

            <!-- Contenedor del Texto de la Frase o Cargador -->
            <div class="quote-text-container">
                <div id="loading-spinner" class="loading-spinner" aria-label="Cargando frase del día..."></div>
                <blockquote id="quote-text" class="quote-text">
                    Eres mi primer pensamiento al despertar y el último antes de soñar. Eres mi hoy y todos mis mañanas.
                </blockquote>
            </div>

            <!-- Botones de Acción -->
            <div class="actions-group">
                <button id="btn-copy" class="btn" aria-label="Copiar frase al portapapeles">
                    <svg class="btn-icon" viewBox="0 0 24 24"><rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path></svg>
                    Copiar Frase
                </button>
                <button id="btn-share" class="btn" aria-label="Compartir frase">
                    <svg class="btn-icon" viewBox="0 0 24 24"><circle cx="18" cy="5" r="3"></circle><circle cx="6" cy="12" r="3"></circle><circle cx="18" cy="19" r="3"></circle><line x1="8.59" y1="13.51" x2="15.42" y2="17.49"></line><line x1="15.41" y1="6.51" x2="8.59" y2="10.49"></line></svg>
                    Compartir
                </button>
            </div>
        </article>
    </main>

    <!-- PIE DE PÁGINA -->
    <footer class="footer">
        <p>SoloParaUsted <span class="footer-heart">♥</span> Creado para inspirar amor cada día</p>
    </footer>

    <!-- NOTIFICACIÓN TOAST -->
    <div id="toast" class="toast" role="alert" aria-live="polite">
        <span>✓ Frase copiada al portapapeles</span>
    </div>

    <!-- LÓGICA JAVASCRIPT VANILLA -->
    <script>
        /**
         * CONFIGURACIÓN PRINCIPAL
         * Cuando publiquemos el Web App en Google Apps Script, pegaremos la URL aquí.
         */
        const API_URL = ""; // Ejemplo: "https://script.google.com/macros/s/AKfycbx.../exec"

        // Frase por defecto inicial mientras no haya backend conectado
        const DEFAULT_QUOTE = "Eres mi primer pensamiento al despertar y el último antes de soñar. Eres mi hoy y todos mis mañanas.";

        // Elementos del DOM
        const quoteTextEl = document.getElementById('quote-text');
        const currentDateEl = document.getElementById('current-date');
        const loadingSpinnerEl = document.getElementById('loading-spinner');
        const btnCopy = document.getElementById('btn-copy');
        const btnShare = document.getElementById('btn-share');
        const toastEl = document.getElementById('toast');

        /**
         * Formatea y muestra la fecha actual en español
         * Ejemplo: "lunes, 26 de octubre de 2026"
         */
        function displayCurrentDate() {
            const now = new Date();
            const options = { 
                weekday: 'long', 
                year: 'numeric', 
                month: 'long', 
                day: 'numeric' 
            };
            const formattedDate = now.toLocaleDateString('es-ES', options);
            currentDateEl.textContent = formattedDate;
            currentDateEl.setAttribute('datetime', now.toISOString().split('T')[0]);
        }

        /**
         * Consulta la API del backend en Google Apps Script o usa la frase por defecto
         */
        async function fetchDailyQuote() {
            // Si no hay URL configurada aún, usamos la frase por defecto
            if (!API_URL || API_URL.trim() === "") {
                setQuote(DEFAULT_QUOTE);
                return;
            }

            showLoading(true);

            try {
                const response = await fetch(API_URL);
                if (!response.ok) {
                    throw new Error(`Error HTTP status: ${response.status}`);
                }
                const data = await response.json();
                
                if (data && data.frase) {
                    setQuote(data.frase);
                } else {
                    setQuote(DEFAULT_QUOTE);
                }
            } catch (error) {
                console.warn('No se pudo conectar a la API de frases. Usando frase de respaldo:', error);
                setQuote(DEFAULT_QUOTE);
            } finally {
                showLoading(false);
            }
        }

        /**
         * Actualiza el texto de la frase con una animación suave
         */
        function setQuote(text) {
            quoteTextEl.style.opacity = '0';
            setTimeout(() => {
                quoteTextEl.textContent = text;
                quoteTextEl.style.opacity = '1';
            }, 200);
        }

        /**
         * Alterna el spinner de carga
         */
        function showLoading(isLoading) {
            if (isLoading) {
                quoteTextEl.style.display = 'none';
                loadingSpinnerEl.style.display = 'block';
            } else {
                loadingSpinnerEl.style.display = 'none';
                quoteTextEl.style.display = 'block';
            }
        }

        /**
         * Muestra una notificación Toast temporal
         */
        function showToast(message) {
            if (message) {
                toastEl.querySelector('span').textContent = message;
            }
            toastEl.classList.add('show');
            setTimeout(() => {
                toastEl.classList.remove('show');
            }, 3000);
        }

        /**
         * Copia la frase al portapapeles con fallback compatible
         */
        function copyToClipboard() {
            const textToCopy = `"${quoteTextEl.textContent.trim()}" — SoloParaUsted`;

            if (navigator.clipboard && window.isSecureContext) {
                navigator.clipboard.writeText(textToCopy)
                    .then(() => showToast('✓ Frase copiada al portapapeles'))
                    .catch(() => fallbackCopy(textToCopy));
            } else {
                fallbackCopy(textToCopy);
            }
        }

        /**
         * Método secundario para copiar en navegadores o entornos donde execCommand sea necesario
         */
        function fallbackCopy(text) {
            const textArea = document.createElement('textarea');
            textArea.value = text;
            textArea.style.position = 'fixed';
            textArea.style.left = '-999999px';
            document.body.appendChild(textArea);
            textArea.focus();
            textArea.select();

            try {
                document.execCommand('copy');
                showToast('✓ Frase copiada al portapapeles');
            } catch (err) {
                showToast('No se pudo copiar la frase.');
            } finally {
                document.body.removeChild(textArea);
            }
        }

        /**
         * Comparte la frase usando Web Share API o fallback a WhatsApp
         */
        function shareQuote() {
            const quote = quoteTextEl.textContent.trim();
            const shareData = {
                title: 'SoloParaUsted - Frase Romántica',
                text: `"${quote}" — Descubierto en SoloParaUsted:`,
                url: window.location.href
            };

            // Intentar Web Share API nativo (Móviles / Navegadores modernos)
            if (navigator.share) {
                navigator.share(shareData).catch((err) => {
                    if (err.name !== 'AbortError') {
                        fallbackShareWhatsApp(quote);
                    }
                });
            } else {
                fallbackShareWhatsApp(quote);
            }
        }

        /**
         * Fallback para compartir directamente por WhatsApp Web / App
         */
        function fallbackShareWhatsApp(quote) {
            const message = encodeURIComponent(`"${quote}"\n\nDescubre más frases en: ${window.location.href}`);
            const whatsappUrl = `https://api.whatsapp.com/send?text=${message}`;
            window.open(whatsappUrl, '_blank');
        }

        /* ==========================================================================
           INICIALIZACIÓN
           ========================================================================== */
        document.addEventListener('DOMContentLoaded', () => {
            displayCurrentDate();
            fetchDailyQuote();

            // Event Listeners
            btnCopy.addEventListener('click', copyToClipboard);
            btnShare.addEventListener('click', shareQuote);
        });
    </script>
</body>
</html>
