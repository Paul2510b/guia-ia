<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Guía Definitiva IA Google - Jean Paul Bernal Rodriguez</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    
    <!-- Chosen Palette: Warm Neutrals & Tech Blue. Fondo Stone-50, acentos Blue-600 y Slate-900. Una paleta que transmite calma, claridad y autoridad profesional. -->
    
    <!-- Application Structure Plan: Diseño de "Learning Hub" (Hub de Aprendizaje). La arquitectura de información se aleja de la lectura lineal de un PDF para ofrecer una exploración por módulos. El Dashboard inicial presenta el ROI (Retorno de Inversión) de tiempo, y las secciones internas utilizan Tabs (pestañas) y Cards para organizar tutoriales y prompts maestros de forma que no saturen visualmente al usuario. -->
    
    <!-- Visualization & Content Choices: 
    1. Gráfico de Barras (Chart.js): Comparativa visual de minutos ahorrados por tarea. 
    2. Sistema de Pestañas Dinámicas (JS): Para navegar entre herramientas de Workspace (Docs, Gmail, etc.). 
    3. Bloques de Código Interactivos: Con botones de copiado rápido para Prompts R.T.F.C. 
    4. Diagrama de Flujo Conceptual (HTML/CSS): Representación visual de la lógica de automatización. 
    Librerías: Chart.js para visualización. Tailwind para UI. NO SVG, NO Mermaid. -->
    
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->

    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        
        body {
            font-family: 'Inter', sans-serif;
            background-color: #fafaf9; /* stone-50 */
            color: #1c1917; /* stone-900 */
        }

        .chart-container {
            position: relative;
            width: 100%;
            max-width: 800px;
            margin: 0 auto;
            height: 350px;
            max-height: 400px;
        }

        .tab-active {
            border-bottom: 3px solid #2563eb;
            color: #2563eb;
            font-weight: 700;
        }

        .fade-in {
            animation: fadeIn 0.4s ease-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .hide-scroll {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }
        .hide-scroll::-webkit-scrollbar {
            display: none;
        }
    </style>
</head>
<body class="antialiased flex flex-col min-h-screen">

    <!-- Navegación -->
    <nav class="sticky top-0 z-50 bg-white/80 backdrop-blur-lg border-b border-stone-200">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row justify-between items-center h-auto md:h-16 py-3">
                <div class="flex items-center space-x-2 mb-3 md:mb-0">
                    <span class="text-xl">🤖</span>
                    <span class="font-bold text-slate-800 tracking-tighter text-lg uppercase">Hub IA Google</span>
                </div>
                <div class="flex items-center space-x-1 md:space-x-2 overflow-x-auto w-full md:w-auto hide-scroll justify-center">
                    <button onclick="navigate('home')" id="nav-home" class="px-4 py-2 rounded-lg text-xs font-bold uppercase tracking-widest bg-blue-50 text-blue-700 transition-all">Inicio</button>
                    <button onclick="navigate('mod1')" id="nav-mod1" class="px-4 py-2 rounded-lg text-xs font-bold uppercase tracking-widest text-slate-500 hover:bg-stone-100 transition-all">Módulo 1</button>
                    <button onclick="navigate('mod2')" id="nav-mod2" class="px-4 py-2 rounded-lg text-xs font-bold uppercase tracking-widest text-slate-500 hover:bg-stone-100 transition-all">Módulo 2</button>
                    <button onclick="navigate('mod3')" id="nav-mod3" class="px-4 py-2 rounded-lg text-xs font-bold uppercase tracking-widest text-slate-500 hover:bg-stone-100 transition-all">Módulo 3</button>
                </div>
            </div>
        </div>
    </nav>

    <main class="flex-grow max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-10">

        <!-- SECCIÓN: INICIO (HOME) -->
        <section id="sec-home" class="fade-in block">
            <div class="text-center mb-16">
                <h1 class="text-5xl md:text-7xl font-black text-slate-900 mb-4 tracking-tighter">Guía Definitiva IA Google</h1>
                <p class="text-xl md:text-2xl text-blue-600 font-medium tracking-tight mb-8">Jean Paul Bernal Rodriguez</p>
                <div class="w-20 h-1.5 bg-blue-600 mx-auto rounded-full mb-12"></div>
                
                <div class="grid grid-cols-1 md:grid-cols-3 gap-6 max-w-5xl mx-auto">
                    <div onclick="navigate('mod1')" class="bg-white p-8 rounded-3xl border border-stone-200 shadow-sm hover:shadow-xl hover:-translate-y-1 transition-all cursor-pointer group">
                        <div class="text-4xl mb-4 group-hover:scale-110 transition-transform">🧠</div>
                        <h3 class="font-bold text-slate-800 text-lg">Dominio Gemini</h3>
                        <p class="text-sm text-slate-500 mt-2">Fundamentos, R.T.F.C. y Privacidad.</p>
                    </div>
                    <div onclick="navigate('mod2')" class="bg-white p-8 rounded-3xl border border-stone-200 shadow-sm hover:shadow-xl hover:-translate-y-1 transition-all cursor-pointer group">
                        <div class="text-4xl mb-4 group-hover:scale-110 transition-transform">⚡</div>
                        <h3 class="font-bold text-slate-800 text-lg">Workspace</h3>
                        <p class="text-sm text-slate-500 mt-2">IA en Docs, Sheets, Gmail y Slides.</p>
                    </div>
                    <div onclick="navigate('mod3')" class="bg-white p-8 rounded-3xl border border-stone-200 shadow-sm hover:shadow-xl hover:-translate-y-1 transition-all cursor-pointer group">
                        <div class="text-4xl mb-4 group-hover:scale-110 transition-transform">⚙️</div>
                        <h3 class="font-bold text-slate-800 text-lg">Automatización</h3>
                        <p class="text-sm text-slate-500 mt-2">Sistemas autónomos y Apps Script.</p>
                    </div>
                </div>
            </div>

            <div class="bg-white rounded-[2.5rem] shadow-sm border border-stone-200 p-8 md:p-12 mb-10">
                <div class="flex flex-col md:flex-row justify-between items-end mb-10">
                    <div>
                        <h2 class="text-3xl font-bold text-slate-900 tracking-tight">Impacto en la Productividad</h2>
                        <p class="text-slate-500 mt-1">Comparativa de tiempo manual vs. optimizado con IA.</p>
                    </div>
                    <div class="text-[10px] text-slate-400 font-mono tracking-widest mt-4 md:mt-0 uppercase">Data by Jean Paul Bernal Rodriguez</div>
                </div>
                <div class="chart-container">
                    <canvas id="timeChart"></canvas>
                </div>
            </div>
        </section>

        <!-- SECCIÓN: MÓDULO 1 -->
        <section id="sec-mod1" class="fade-in hidden">
            <div class="max-w-4xl mx-auto">
                <div class="mb-12">
                    <h2 class="text-4xl font-bold text-slate-900 tracking-tight">Módulo 1: El Nuevo Estándar Base</h2>
                    <p class="text-slate-600 mt-3 text-lg">Dominar la interfaz y la ingeniería de prompts es el primer paso para convertir la IA en un activo estratégico.</p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-12">
                    <div class="bg-white p-8 rounded-3xl border border-stone-200 shadow-sm">
                        <h3 class="font-bold text-xl mb-6 text-slate-800 border-b border-stone-100 pb-4">🔒 Privacidad y Entorno</h3>
                        <ul class="space-y-4">
                            <li class="flex items-start">
                                <span class="text-blue-600 mr-3 font-bold">01.</span>
                                <p class="text-sm text-slate-700"><strong>Desactiva la Actividad:</strong> Evita que tus datos se usen para entrenar modelos públicos.</p>
                            </li>
                            <li class="flex items-start">
                                <span class="text-blue-600 mr-3 font-bold">02.</span>
                                <p class="text-sm text-slate-700"><strong>Hilos Específicos:</strong> Crea chats por proyecto para evitar "alucinaciones" cruzadas.</p>
                            </li>
                            <li class="flex items-start">
                                <span class="text-blue-600 mr-3 font-bold">03.</span>
                                <p class="text-sm text-slate-700"><strong>Gemini Advanced:</strong> Utilízalo para procesar archivos de más de 500 páginas.</p>
                            </li>
                        </ul>
                    </div>

                    <div class="bg-slate-900 p-8 rounded-3xl text-white shadow-xl">
                        <h3 class="font-bold text-xl mb-6 text-blue-400">Ingeniería R.T.F.C.</h3>
                        <div class="grid grid-cols-2 gap-3 mb-8">
                            <div class="bg-slate-800 p-3 rounded-xl border border-slate-700 text-center">
                                <span class="block text-xl font-black text-blue-400">R</span>
                                <span class="text-[10px] uppercase font-bold tracking-tighter">Rol</span>
                            </div>
                            <div class="bg-slate-800 p-3 rounded-xl border border-slate-700 text-center">
                                <span class="block text-xl font-black text-blue-400">T</span>
                                <span class="text-[10px] uppercase font-bold tracking-tighter">Tarea</span>
                            </div>
                            <div class="bg-slate-800 p-3 rounded-xl border border-slate-700 text-center">
                                <span class="block text-xl font-black text-blue-400">F</span>
                                <span class="text-[10px] uppercase font-bold tracking-tighter">Formato</span>
                            </div>
                            <div class="bg-slate-800 p-3 rounded-xl border border-slate-700 text-center">
                                <span class="block text-xl font-black text-blue-400">C</span>
                                <span class="text-[10px] uppercase font-bold tracking-tighter">Contexto</span>
                            </div>
                        </div>
                        <button onclick="copyText('prompt1')" class="w-full bg-blue-600 text-white py-4 rounded-2xl font-bold hover:bg-blue-700 transition-colors shadow-lg">Copiar Prompt Maestro (Crisis)</button>
                        <textarea id="prompt1" class="hidden">[ROL]: Director de Comunicaciones Corporativas. [TAREA]: Redactar comunicado de caída de servicio. [FORMATO]: Email de 3 párrafos. [CONTEXTO]: Servidores AWS caídos 4h. Resuelto. Datos a salvo.</textarea>
                    </div>
                </div>
            </div>
        </section>

        <!-- SECCIÓN: MÓDULO 2 -->
        <section id="sec-mod2" class="fade-in hidden">
            <div class="mb-10">
                <h2 class="text-4xl font-bold text-slate-900 tracking-tight">Módulo 2: Workspace Inyectado</h2>
                <p class="text-slate-600 mt-2 text-lg">La IA integrada permite ejecutar tareas directamente en el flujo de trabajo.</p>
            </div>

            <div class="bg-white rounded-3xl border border-stone-200 overflow-hidden shadow-sm">
                <div class="flex border-b border-stone-200 bg-stone-50 overflow-x-auto hide-scroll">
                    <button onclick="switchTab('docs')" id="tab-docs" class="ws-tab tab-active flex-1 py-5 px-6 text-sm font-black uppercase tracking-widest">Docs</button>
                    <button onclick="switchTab('gmail')" id="tab-gmail" class="ws-tab flex-1 py-5 px-6 text-sm font-black uppercase tracking-widest text-stone-400">Gmail</button>
                    <button onclick="switchTab('sheets')" id="tab-sheets" class="ws-tab flex-1 py-5 px-6 text-sm font-black uppercase tracking-widest text-stone-400">Sheets</button>
                    <button onclick="switchTab('slides')" id="tab-slides" class="ws-tab flex-1 py-5 px-6 text-sm font-black uppercase tracking-widest text-stone-400">Slides</button>
                </div>
                <div class="p-8 md:p-12">
                    <div id="content-docs" class="ws-content block fade-in">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
                            <div>
                                <h4 class="text-2xl font-bold text-slate-800 mb-4">Invocación Directa</h4>
                                <p class="text-slate-600 text-sm leading-relaxed mb-6">Usa el botón flotante <strong>"Ayúdame a escribir"</strong> para generar borradores desde cero o el <strong>Panel Lateral</strong> para cruzar datos con archivos de Drive.</p>
                                <div class="bg-blue-50 p-4 rounded-2xl border border-blue-100 text-blue-800 text-xs italic">"Optimización de clics diseñada por Jean Paul Bernal Rodriguez."</div>
                            </div>
                            <div class="bg-stone-900 p-6 rounded-3xl">
                                <div class="flex justify-between items-center mb-4">
                                    <span class="text-[10px] font-bold text-stone-500 uppercase tracking-widest">Prompt Sugerido</span>
                                    <button onclick="copyText('p-docs')" class="text-xs bg-stone-800 text-white px-3 py-1 rounded-full border border-stone-700">Copiar</button>
                                </div>
                                <textarea id="p-docs" class="hidden">Actúa como Ejecutivo B2B. Redacta propuesta ERP con: resumen, problema cliente, solución y cronograma de 3 meses.</textarea>
                                <p class="text-green-400 font-mono text-xs leading-relaxed">Actúa como Ejecutivo B2B. Redacta propuesta ERP con: resumen, problema cliente, solución y cronograma de 3 meses.</p>
                            </div>
                        </div>
                    </div>
                    <div id="content-gmail" class="ws-content hidden fade-in">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
                            <div>
                                <h4 class="text-2xl font-bold text-slate-800 mb-4">Gestión de Bandeja</h4>
                                <p class="text-slate-600 text-sm leading-relaxed mb-6">Resumen de hilos interminables con un clic y redacción inteligente para gestión de crisis y reembolsos.</p>
                                <div class="bg-stone-50 p-4 rounded-2xl border border-stone-200 text-slate-600 text-xs">Usa "Refinar -> Sentirme con suerte" para tonos más naturales.</div>
                            </div>
                            <div class="bg-stone-900 p-6 rounded-3xl">
                                <button onclick="copyText('p-gmail')" class="w-full bg-blue-600 text-white py-3 rounded-xl text-xs font-bold mb-4">Copiar Respuesta a Crisis</button>
                                <textarea id="p-gmail" class="hidden">Redacta respuesta empática. Cliente molesto por retraso. Ofrece disculpas y crédito de $50 USD. Máximo 2 párrafos.</textarea>
                                <p class="text-stone-400 font-mono text-[10px]">Redacta respuesta empática. Cliente molesto por retraso. Ofrece disculpas y crédito de $50 USD. Máximo 2 párrafos.</p>
                            </div>
                        </div>
                    </div>
                    <div id="content-sheets" class="ws-content hidden fade-in">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
                            <div>
                                <h4 class="text-2xl font-bold text-slate-800 mb-4">Estructuras y Fórmulas</h4>
                                <p class="text-slate-600 text-sm leading-relaxed mb-6">Genera tablas inteligentes con "Ayúdame a organizar" o pide fórmulas complejas de VLOOKUP directamente en el chat lateral.</p>
                            </div>
                            <div class="bg-stone-900 p-6 rounded-3xl text-green-400 font-mono text-xs">
                                <span>=IFERROR(VLOOKUP(A2, Nómina!A:B, 2, FALSE), "")</span>
                                <button onclick="copyText('p-sheets')" class="block w-full mt-4 bg-stone-800 text-white py-2 rounded-lg text-[10px] font-bold">Copiar Prompt de Fórmula</button>
                                <textarea id="p-sheets" class="hidden">Dame una fórmula de VLOOKUP para cruzar el ID de la columna A con la hoja de 'Nómina' y traer el salario. Si falla, dejar vacío.</textarea>
                            </div>
                        </div>
                    </div>
                    <div id="content-slides" class="ws-content hidden fade-in">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
                            <div>
                                <h4 class="text-2xl font-bold text-slate-800 mb-4">Diseño Narrativo</h4>
                                <p class="text-slate-600 text-sm leading-relaxed mb-6">Crea esquemas de 6-8 diapositivas y genera imágenes fotorrealistas con Imagen 3 para evitar bancos de stock genéricos.</p>
                            </div>
                            <div class="bg-stone-900 p-6 rounded-3xl flex items-center justify-center text-stone-600 border border-stone-800 border-dashed">
                                <span class="text-[10px] uppercase font-bold tracking-widest text-center">Inyecta Prompts de Imagen aquí</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- SECCIÓN: MÓDULO 3 -->
        <section id="sec-mod3" class="fade-in hidden">
            <div class="mb-10">
                <h2 class="text-4xl font-bold text-slate-900 tracking-tight">Módulo 3: Automatización</h2>
                <div class="h-1.5 w-20 bg-blue-600 mt-4 rounded-full"></div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-12">
                <div class="bg-white p-10 rounded-[2.5rem] border border-stone-200 shadow-sm">
                    <h3 class="font-bold text-2xl text-slate-800 mb-6">Apps Script No-Code</h3>
                    <p class="text-slate-600 text-sm mb-8 leading-relaxed">No necesitas ser programador. Describe el flujo a Gemini y pega el resultado en el editor de Google Sheets.</p>
                    <div class="space-y-4">
                        <div class="flex items-center space-x-4 p-4 bg-stone-50 rounded-2xl border border-stone-100">
                            <div class="bg-blue-600 text-white w-8 h-8 rounded-full flex items-center justify-center font-bold text-xs">1</div>
                            <span class="text-xs font-medium text-slate-700">Extensiones > Apps Script</span>
                        </div>
                        <div class="flex items-center space-x-4 p-4 bg-stone-50 rounded-2xl border border-stone-100">
                            <div class="bg-blue-600 text-white w-8 h-8 rounded-full flex items-center justify-center font-bold text-xs">2</div>
                            <span class="text-xs font-medium text-slate-700">Pega el código generado por IA</span>
                        </div>
                        <div class="flex items-center space-x-4 p-4 bg-stone-50 rounded-2xl border border-stone-100">
                            <div class="bg-blue-600 text-white w-8 h-8 rounded-full flex items-center justify-center font-bold text-xs">3</div>
                            <span class="text-xs font-medium text-slate-700">Activa el Trigger "Al Editarse"</span>
                        </div>
                    </div>
                </div>

                <div class="bg-slate-900 p-10 rounded-[2.5rem] text-white shadow-2xl relative overflow-hidden">
                    <div class="relative z-10">
                        <h3 class="font-bold text-2xl mb-8">Arquitectura de Sistema</h3>
                        <p class="text-slate-400 text-xs mb-10 italic">"Sistemas diseñados por Jean Paul Bernal Rodriguez."</p>
                        
                        <div class="flex flex-col space-y-6">
                            <div class="flex items-center space-x-4 border-l-2 border-slate-700 pl-6 py-2">
                                <span class="text-2xl">📥</span>
                                <div>
                                    <div class="text-[10px] font-bold text-blue-400 uppercase tracking-widest">Entrada</div>
                                    <div class="text-sm font-medium">Nuevo Lead vía Make/Zapier</div>
                                </div>
                            </div>
                            <div class="flex items-center space-x-4 border-l-2 border-blue-600 pl-6 py-2 bg-blue-900/20 rounded-r-xl">
                                <span class="text-2xl">🧠</span>
                                <div>
                                    <div class="text-[10px] font-bold text-blue-400 uppercase tracking-widest">Procesamiento</div>
                                    <div class="text-sm font-medium">Gemini analiza y clasifica</div>
                                </div>
                            </div>
                            <div class="flex items-center space-x-4 border-l-2 border-slate-700 pl-6 py-2">
                                <span class="text-2xl">⚡</span>
                                <div>
                                    <div class="text-[10px] font-bold text-blue-400 uppercase tracking-widest">Salida</div>
                                    <div class="text-sm font-medium">Auto-Registro y Borrador de Email</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="bg-white border-t border-stone-200 pt-20 pb-10">
        <div class="max-w-7xl mx-auto px-4 text-center">
            <h5 class="text-3xl font-black text-slate-900 tracking-tighter mb-2">Jean Paul Bernal Rodriguez</h5>
            <p class="text-slate-400 text-[10px] uppercase tracking-[0.5em] font-bold mb-10">Guía Definitiva IA Google • 2026</p>
            <div class="w-16 h-1 bg-stone-100 mx-auto rounded-full mb-10"></div>
            <p class="text-stone-300 text-[10px] leading-relaxed max-w-sm mx-auto">Esta aplicación interactiva es un activo de formación técnica. Diseñada para la optimización masiva de procesos mediante Inteligencia Artificial.</p>
        </div>
    </footer>

    <!-- Notificaciones Toast -->
    <div id="toast" class="fixed bottom-10 right-10 bg-slate-900 text-white px-8 py-5 rounded-3xl shadow-2xl transform translate-y-40 opacity-0 transition-all duration-500 flex items-center font-bold text-sm">
        <span class="mr-4 text-xl">📋</span> Texto copiado al portapapeles
    </div>

    <script>
        // --- NAVEGACIÓN ---
        const sections = ['home', 'mod1', 'mod2', 'mod3'];
        function navigate(id) {
            sections.forEach(s => {
                document.getElementById('sec-' + s).classList.add('hidden');
                document.getElementById('nav-' + s).classList.remove('bg-blue-50', 'text-blue-700');
                document.getElementById('nav-' + s).classList.add('text-slate-500');
            });
            document.getElementById('sec-' + id).classList.remove('hidden');
            document.getElementById('nav-' + id).classList.add('bg-blue-50', 'text-blue-700');
            document.getElementById('nav-' + id).classList.remove('text-slate-500');
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // --- TABS MOD 2 ---
        function switchTab(id) {
            ['docs', 'gmail', 'sheets', 'slides'].forEach(t => {
                document.getElementById('tab-' + t).classList.remove('tab-active');
                document.getElementById('tab-' + t).classList.add('text-stone-400');
                document.getElementById('content-' + t).classList.add('hidden');
            });
            const active = document.getElementById('tab-' + id);
            active.classList.add('tab-active');
            active.classList.remove('text-stone-400');
            document.getElementById('content-' + id).classList.remove('hidden');
        }

        // --- UTILIDADES ---
        function copyText(id) {
            const el = document.getElementById(id);
            el.style.display = 'block';
            el.select();
            document.execCommand('copy');
            el.style.display = 'none';
            
            const toast = document.getElementById('toast');
            toast.classList.remove('translate-y-40', 'opacity-0');
            setTimeout(() => toast.classList.add('translate-y-40', 'opacity-0'), 3000);
        }

        // --- GRÁFICOS ---
        document.addEventListener("DOMContentLoaded", function() {
            const ctx = document.getElementById('timeChart').getContext('2d');
            new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: ['Reporte 40p', 'Hilo Email', 'CRM Base', 'Fórmula', 'Slides'],
                    datasets: [
                        { 
                            label: 'Manual (minutos)', 
                            data: [90, 45, 20, 15, 10], 
                            backgroundColor: '#e7e5e4', 
                            borderRadius: 12 
                        },
                        { 
                            label: 'IA by Jean Paul Bernal Rodriguez (minutos)', 
                            data: [2, 1, 1, 1, 1], 
                            backgroundColor: '#2563eb', 
                            borderRadius: 12 
                        }
                    ]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: { 
                        legend: { 
                            position: 'bottom', 
                            labels: { 
                                font: { family: 'Inter', weight: '700', size: 11 },
                                boxWidth: 10,
                                padding: 20
                            } 
                        } 
                    },
                    scales: { 
                        y: { beginAtZero: true, grid: { display: false }, ticks: { font: { size: 10 } } }, 
                        x: { grid: { display: false }, ticks: { font: { size: 10 } } } 
                    }
                }
            });
        });
    </script>
</body>
</html>
