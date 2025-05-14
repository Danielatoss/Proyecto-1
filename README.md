
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>NeuroFinanzasMCD - Plataforma de Cursos Financieros</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background-color: #3366cc;
            color: white;
            text-align: center;
            padding: 1em 0;
        }
        nav {
            background-color: #2c5f9d;
            padding: 0.75em;
            text-align: center;
        }
        nav a, nav button {
            display: inline-block;
            color: white;
            margin: 0 1em;
            padding: 0.6em 1.4em;
            border-radius: 5px;
            background-color: #2c5f9d;
            text-decoration: none;
            transition: background-color 0.3s ease;
            cursor: pointer;
        }
        nav a:hover, nav button:hover {
            background-color: #1a3b6d;
        }
        .container {
            max-width: 1200px;
            margin: auto;
            padding: 2em;
        }
        .nivel-content, .curso-content {
            display: none;
        }
        .nivel-content.active, .curso-content.active {
            display: block;
        }
        .temario {
            margin-top: 1em;
        }
        .temario ul {
            list-style-type: decimal;
            padding-left: 1.5em;
        }
        .video-container, .audio-container {
            margin-top: 2em;
        }
        .exam-section {
            margin-top: 2em;
        }
        .exam-options button {
            margin-right: 1em;
            margin-top: 0.5em;
            background-color: #2c5f9d;
            color: white;
            border: none;
            padding: 0.5em 1em;
            border-radius: 5px;
            cursor: pointer;
        }
        .grades-section {
            margin-top: 2em;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 1em;
        }
        th, td {
            border: 1px solid #ccc;
            padding: 0.75em;
            text-align: center;
        }
        th {
            background-color: #e0e0e0;
        }
        footer {
            text-align: center;
            padding: 1em;
            background-color: #1a3b6d;
            color: white;
            margin-top: 2em;
        }
        .language-selector {
            position: fixed;
            top: 10px;
            right: 10px;
            background-color: #2c5f9d;
            color: white;
            padding: 0.5em;
            border-radius: 5px;
            cursor: pointer;
        }
        .language-dropdown {
            display: none;
            position: absolute;
            top: 40px;
            right: 10px;
            background-color: white;
            border: 1px solid #ccc;
            border-radius: 5px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .language-dropdown a {
            display: block;
            padding: 0.5em;
            text-decoration: none;
            color: black;
        }
        .language-dropdown a:hover {
            background-color: #f0f0f0;
        }
    </style>
</head>
<body>

<header>
    <h1 id="header-title">Bienvenido a NeuroFinanzasMCD</h1>
    <p id="header-description">Plataforma de Cursos Financieros Online</p>
</header>

<div class="language-selector" onclick="toggleLanguageDropdown()">Idioma ▼</div>
<div class="language-dropdown" id="language-dropdown">
    <a href="#" onclick="changeLanguage('es')">Español</a>
    <a href="#" onclick="changeLanguage('en')">Inglés</a>
    <a href="#" onclick="changeLanguage('fr')">Francés</a>
    <a href="#" onclick="changeLanguage('de')">Alemán</a>
    <a href="#" onclick="changeLanguage('pt')">Portugués</a>
</div>

<nav>
    <button onclick="mostrarNivel('basico')">Nivel Básico</button>
    <button onclick="mostrarNivel('intermedio')">Nivel Intermedio</button>
    <button onclick="mostrarNivel('avanzado')">Nivel Avanzado</button>
    <button onclick="mostrarNivel('experto')">Nivel Experto</button>
</nav>

<div class="container" id="niveles" style="display: block;">
    <!-- Nivel Básico -->
    <div id="basico" class="nivel-content active">
        <h2 id="basico-title">Nivel Básico</h2>
        <button onclick="volverInicio()" style="margin-bottom: 1em;">Volver a Página Principal</button>
        <div class="temario">
            <h3 id="basico-temario">Temario:</h3>
            <ul>
                <li><a onclick="mostrarCurso('basicoCurso1')">Curso 1: Introducción a los Mercados Financieros</a></li>
                <li><a onclick="mostrarCurso('basicoCurso2')">Curso 2: Conceptos básicos del Trading</a></li>
                <li><a onclick="mostrarCurso('basicoCurso3')">Curso 3: Análisis Técnico Inicial</a></li>
                <li><a onclick="mostrarCurso('basicoCurso4')">Curso 4: Análisis Fundamental para principiantes</a></li>
                <li><a onclick="mostrarCurso('basicoCurso5')">Curso 5: Psicología del Inversor, mentalidad correcta</a></li>
            </ul>
        </div>
    </div>

    <!-- Nivel Intermedio -->
    <div id="intermedio" class="nivel-content">
        <h2 id="intermedio-title">Nivel Intermedio</h2>
        <button onclick="volverInicio()" style="margin-bottom: 1em;">Volver a Página Principal</button>
        <div class="temario">
            <h3 id="intermedio-temario">Temario:</h3>
            <ul>
                <li><a onclick="mostrarCurso('intermedioCurso1')">Curso 1: Patrones gráficos y figuras técnicas</a></li>
                <li><a onclick="mostrarCurso('intermedioCurso2')">Curso 2: Gestión de riesgo y money management</a></li>
                <li><a onclick="mostrarCurso('intermedioCurso3')">Curso 3: Estrategia de Trading Intradía</a></li>
                <li><a onclick="mostrarCurso('intermedioCurso4')">Curso 4: Trading en tendencia y contratendencia</a></li>
                <li><a onclick="mostrarCurso('intermedioCurso5')">Curso 5: Uso de plataforma y Brokers profesionales</a></li>
            </ul>
        </div>
    </div>

    <!-- Nivel Avanzado -->
    <div id="avanzado" class="nivel-content">
        <h2 id="avanzado-title">Nivel Avanzado</h2>
        <button onclick="volverInicio()" style="margin-bottom: 1em;">Volver a Página Principal</button>
        <div class="temario">
            <h3 id="avanzado-temario">Temario:</h3>
            <ul>
                <li><a onclick="mostrarCurso('avanzadoCurso1')">Curso 1: Análisis Técnico avanzado y osciladores</a></li>
                <li><a onclick="mostrarCurso('avanzadoCurso2')">Curso 2: Estrategias Avanzadas de trading Forex y Criptoactivos</a></li>
                <li><a onclick="mostrarCurso('avanzadoCurso3')">Curso 3: Microestructura de los Mercados Financieros</a></li>
                <li><a onclick="mostrarCurso('avanzadoCurso4')">Curso 4: Trading Automatizado e introducción a Backtesting</a></li>
                <li><a onclick="mostrarCurso('avanzadoCurso5')">Curso 5: Gestión avanzada de portafolios de inversión</a></li>
            </ul>
        </div>
    </div>

    <!-- Nivel Experto -->
    <div id="experto" class="nivel-content">
        <h2 id="experto-title">Nivel Experto</h2>
        <button onclick="volverInicio()" style="margin-bottom: 1em;">Volver a Página Principal</button>
        <div class="temario">
            <h3 id="experto-temario">Temario:</h3>
            <ul>
                <li><a onclick="mostrarCurso('expertoCurso1')">Curso 1: Evaluación de proyectos Financieros, Van, TIR, PRI</a></li>
                <li><a onclick="mostrarCurso('expertoCurso2')">Curso 2: Optimización de portafolios. Teoría moderna y Frontera</a></li>
                <li><a onclick="mostrarCurso('expertoCurso3')">Curso 3: Análisis de Riesgos Financieros</a></li>
                <li><a onclick="mostrarCurso('expertoCurso4')">Curso 4: Herramientas de evaluación Cuantitativamente</a></li>
                <li><a onclick="mostrarCurso('expertoCurso5')">Curso 5: Análisis integral de Portafolios y reportes para inversores</a></li>
            </ul>
        </div>
    </div>

    <!-- Curso Contenido (Básico) -->
    <div id="basicoCurso1" class="curso-content">
        <h2>Introducción a los Mercados Financieros</h2>
        <button onclick="volverNivel('basico')" style="margin-bottom: 1em;">Volver al Nivel Básico</button>
        <div class="video-container">
            <h3>Video:</h3>
            <iframe src="https://www.youtube.com/embed/dummy-video-id " frameborder="0" allowfullscreen></iframe>
        </div>
        <div class="video-container">
            <h3>Streaming:</h3>
            <iframe src="https://www.twitch.tv/embed/dummy-stream-id " frameborder="0" allowfullscreen></iframe>
        </div>
        <div class="audio-container">
            <h3>Audio:</h3>
            <audio controls>
                <source src="dummy-audio.mp3" type="audio/mpeg">
                Tu navegador no soporta el elemento de audio.
            </audio>
        </div>
        <div class="exam-section">
            <h3>Examen del Curso</h3>
            <p>Elige la opción correcta para continuar:</p>
            <div class="exam-options">
                <button onclick="registrarCalificacion('Básico', 'Curso 1', 95)">Opción A</button>
                <button onclick="registrarCalificacion('Básico', 'Curso 1', 85)">Opción B</button>
                <button onclick="registrarCalificacion('Básico', 'Curso 1', 90)">Opción C</button>
            </div>
        </div>
    </div>

    <!-- Repetir bloques similares para todos los cursos de todos los niveles -->

</div>

<!-- Calificaciones -->
<div class="container" id="calificaciones" style="display: none;">
    <h2>Calificaciones</h2>
    <table>
        <thead>
            <tr>
                <th>Nivel</th>
                <th>Curso</th>
                <th>Calificación</th>
            </tr>
        </thead>
        <tbody id="tablaCalificaciones">
            <tr><td colspan="3">Sin calificaciones registradas aún.</td></tr>
        </tbody>
    </table>
</div>

<footer>
    &copy; 2025 NeuroFinanzasMCD - Todos los derechos reservados.
</footer>

<script>
    function mostrarNivel(nivelId) {
        document.querySelectorAll('.nivel-content').forEach(nivel => nivel.classList.remove('active'));
        document.getElementById(nivelId).classList.add('active');
    }

    function mostrarCurso(cursoId) {
        document.querySelectorAll('.curso-content').forEach(curso => curso.classList.remove('active'));
        document.getElementById(cursoId).classList.add('active');
    }

    function volverInicio() {
        document.querySelectorAll('.nivel-content').forEach(nivel => nivel.classList.remove('active'));
        document.getElementById('niveles').style.display = 'block';
    }

    function volverNivel(nivelId) {
        document.querySelectorAll('.curso-content').forEach(curso => curso.classList.remove('active'));
        document.getElementById(nivelId).classList.add('active');
    }

    function registrarCalificacion(nivel, curso, calificacion) {
        const tabla = document.getElementById("tablaCalificaciones");
        let fila = null;

        // Busca si ya existe una fila para ese nivel y curso
        for (let i = 0; i < tabla.rows.length; i++) {
            if (tabla.rows[i].cells[0].textContent === nivel && tabla.rows[i].cells[1].textContent === curso) {
                fila = tabla.rows[i];
                break;
            }
        }

        if (fila) {
            // Actualiza la calificación existente
            fila.cells[2].textContent = calificacion + "/100";
        } else {
            // Agrega nueva fila
            const newRow = tabla.insertRow();
            newRow.innerHTML = `
                <td>${nivel}</td>
                <td>${curso}</td>
                <td>${calificacion}/100</td>
            `;
        }
    }

    function toggleLanguageDropdown() {
        const dropdown = document.getElementById('language-dropdown');
        dropdown.style.display = dropdown.style.display === 'none' ? 'block' : 'none';
    }

    const translations = {
        es: {
            headerTitle: "Bienvenido a NeuroFinanzasMCD",
            headerDescription: "Plataforma de Cursos Financieros Online",
            basicoTitle: "Nivel Básico",
            intermedioTitle: "Nivel Intermedio",
            avanzadoTitle: "Nivel Avanzado",
            expertoTitle: "Nivel Experto",
            basicoTemario: "Temario:",
            intermedioTemario: "Temario:",
            avanzadoTemario: "Temario:",
            expertoTemario: "Temario:"
        },
        en: {
            headerTitle: "Welcome to NeuroFinanzasMCD",
            headerDescription: "Online Financial Courses Platform",
            basicoTitle: "Basic Level",
            intermedioTitle: "Intermediate Level",
            avanzadoTitle: "Advanced Level",
            expertoTitle: "Expert Level",
            basicoTemario: "Syllabus:",
            intermedioTemario: "Syllabus:",
            avanzadoTemario: "Syllabus:",
            expertoTemario: "Syllabus:"
        },
        fr: {
            headerTitle: "Bienvenue chez NeuroFinanzasMCD",
            headerDescription: "Plateforme de cours financiers en ligne",
            basicoTitle: "Niveau Basique",
            intermedioTitle: "Niveau Intermédiaire",
            avanzadoTitle: "Niveau Avancé",
            expertoTitle: "Niveau Expert",
            basicoTemario: "Programme:",
            intermedioTemario: "Programme:",
            avanzadoTemario: "Programme:",
            expertoTemario: "Programme:"
        },
        de: {
            headerTitle: "Willkommen bei NeuroFinanzasMCD",
            headerDescription: "Online-Finanzkurse-Plattform",
            basicoTitle: "Grundstufe",
            intermedioTitle: "Mittelstufe",
            avanzadoTitle: "Fortgeschrittenes Niveau",
            expertoTitle: "Expertenlevel",
            basicoTemario: "Lehrplan:",
            intermedioTemario: "Lehrplan:",
            avanzadoTemario: "Lehrplan:",
            expertoTemario: "Lehrplan:"
        },
        pt: {
            headerTitle: "Bem-vindo ao NeuroFinanzasMCD",
            headerDescription: "Plataforma de Cursos Financeiros Online",
            basicoTitle: "Nível Básico",
            intermedioTitle: "Nível Intermediário",
            avanzadoTitle: "Nível Avançado",
            expertoTitle: "Nível Especialista",
            basicoTemario: "Programa:",
            intermedioTemario: "Programa:",
            avanzadoTemario: "Programa:",
            expertoTemario: "Programa:"
        }
    };

    function changeLanguage(lang) {
        const t = translations[lang];
        document.getElementById('header-title').textContent = t.headerTitle;
        document.getElementById('header-description').textContent = t.headerDescription;
        document.getElementById('basico-title').textContent = t.basicoTitle;
        document.getElementById('intermedio-title').textContent = t.intermedioTitle;
        document.getElementById('avanzado-title').textContent = t.avanzadoTitle;
        document.getElementById('experto-title').textContent = t.expertoTitle;
        document.getElementById('basico-temario').textContent = t.basicoTemario;
        document.getElementById('intermedio-temario').textContent = t.intermedioTemario;
        document.getElementById('avanzado-temario').textContent = t.avanzadoTemario;
        document.getElementById('experto-temario').textContent = t.expertoTemario;
    }
</script>

</body>
</html>
