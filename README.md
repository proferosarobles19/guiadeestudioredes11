<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Guía de Estudios: Redes de Computadoras 11° - Colegio Ingeniero Tomás Guardia</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        body { font-family: 'Inter', sans-serif; scroll-behavior: smooth; }
        
        .global-network-bg {
            background: radial-gradient(circle at center, #1e293b 0%, #0f172a 100%);
            position: relative;
            overflow: hidden;
        }
        
        .global-network-bg::before {
            content: "";
            position: absolute;
            top: 0; left: 0; right: 0; bottom: 0;
            background-image: 
                linear-gradient(rgba(30, 58, 138, 0.2) 1px, transparent 1px),
                linear-gradient(90deg, rgba(30, 58, 138, 0.2) 1px, transparent 1px);
            background-size: 40px 40px;
            mask-image: radial-gradient(ellipse at center, black, transparent 80%);
        }

        .pulse-node {
            animation: pulse 4s cubic-bezier(0.4, 0, 0.6, 1) infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 0.3; transform: scale(1); }
            50% { opacity: 0.7; transform: scale(1.1); }
        }

        .card-hover:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1), 0 8px 10px -6px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }
        
        .timeline-line {
            width: 2px;
            background: #e2e8f0;
            position: absolute;
            left: 20px;
            top: 0;
            bottom: 0;
        }

        .feedback-box {
            border: 2px dashed #cbd5e1;
            transition: all 0.3s ease;
        }

        .feedback-box:hover {
            border-color: #3b82f6;
            background-color: #eff6ff;
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-900">

    <header class="global-network-bg text-white py-16 px-6 relative">
        <div class="max-w-6xl mx-auto text-center relative z-10">
            <div class="inline-block bg-blue-600 text-xs font-bold px-3 py-1 rounded-full mb-4 tracking-widest uppercase">
                Bachiller en Informática
            </div>
            <h1 class="text-4xl md:text-6xl font-extrabold mb-4 tracking-tight">
                Guía de Estudios: <span class="text-blue-400">Redes de Computadoras</span>
            </h1>
            <p class="text-xl text-slate-300 font-light mb-8 max-w-2xl mx-auto">
                11° Grado - Colegio Ingeniero Tomás Guardia
            </p>
            
            <div class="flex flex-wrap justify-center gap-4 text-sm mb-10">
                <div class="bg-white/10 backdrop-blur-md px-4 py-2 rounded-lg border border-white/20">
                    <i class="fas fa-school mr-2 text-blue-400"></i> Colegio Ing. Tomás Guardia
                </div>
                <div class="bg-white/10 backdrop-blur-md px-4 py-2 rounded-lg border border-white/20">
                    <i class="fas fa-chalkboard-teacher mr-2 text-blue-400"></i> Profa. Rosa Robles Pino
                </div>
            </div>

            <nav class="flex flex-wrap justify-center gap-2 md:gap-4 overflow-x-auto py-2">
                <a href="#concepto" class="px-4 py-2 bg-white/5 hover:bg-white/20 rounded-full transition text-sm">Concepto</a>
                <a href="#historia" class="px-4 py-2 bg-white/5 hover:bg-white/20 rounded-full transition text-sm">Historia</a>
                <a href="#componentes" class="px-4 py-2 bg-white/5 hover:bg-white/20 rounded-full transition text-sm">Componentes</a>
                <a href="#tipos" class="px-4 py-2 bg-white/5 hover:bg-white/20 rounded-full transition text-sm">Tipos</a>
                <a href="#topologias" class="px-4 py-2 bg-white/5 hover:bg-white/20 rounded-full transition text-sm">Topologías</a>
                <a href="#panama" class="px-4 py-2 bg-white/5 hover:bg-white/20 rounded-full transition text-sm">Panamá</a>
                <a href="#vocabulario" class="px-4 py-2 bg-white/5 hover:bg-white/20 rounded-full transition text-sm">Vocabulario</a>
            </nav>
        </div>
        
        <div class="absolute top-20 left-1/4 w-2 h-2 bg-blue-500 rounded-full pulse-node"></div>
        <div class="absolute bottom-40 right-1/4 w-3 h-3 bg-blue-400 rounded-full pulse-node" style="animation-delay: 1s"></div>
    </header>

    <main class="max-w-6xl mx-auto px-6 py-12 space-y-24">

        <!-- Sección 01: Concepto con Retroalimentación -->
        <section id="concepto" class="scroll-mt-28">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-start">
                <div>
                    <h2 class="text-3xl font-bold text-slate-900 mb-6 flex items-center">
                        <span class="w-10 h-10 bg-blue-600 text-white rounded-lg flex items-center justify-center mr-4 text-sm font-bold">01</span>
                        Concepto de Red
                    </h2>
                    <p class="text-lg text-slate-600 leading-relaxed mb-6">
                        Una <span class="font-bold text-blue-700">Red de Computadoras</span> es un conjunto de equipos y software conectados entre sí por medio de dispositivos físicos que envían y reciben impulsos eléctricos, ondas electromagnéticas o cualquier otro medio para el transporte de datos, con la finalidad de compartir información, recursos y ofrecer servicios.
                    </p>
                    <div class="bg-blue-50 border-l-4 border-blue-600 p-6 rounded-r-xl">
                        <p class="text-blue-800 italic font-medium">
                            <i class="fas fa-quote-left mr-2"></i>Las redes eliminan la barrera de la distancia física en el procesamiento de datos.
                        </p>
                    </div>
                </div>
                
                <div class="bg-white p-8 rounded-3xl shadow-sm border border-slate-200 feedback-box">
                    <h3 class="text-blue-600 font-bold mb-4 flex items-center">
                        <i class="fas fa-comment-dots mr-2"></i> Retroalimentación de Concepto
                    </h3>
                    <p class="text-sm text-slate-600 mb-4">Analiza y responde en tu cuaderno:</p>
                    <ul class="space-y-3 text-sm text-slate-700">
                        <li class="flex gap-3">
                            <i class="fas fa-question-circle text-blue-400 mt-1"></i>
                            <span>¿Cuál es la diferencia principal entre una "computadora aislada" y un "nodo de red"?</span>
                        </li>
                        <li class="flex gap-3">
                            <i class="fas fa-question-circle text-blue-400 mt-1"></i>
                            <span>Menciona tres recursos que compartes diariamente en la red del Colegio.</span>
                        </li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Sección 02: Historia Interactiva -->
        <section id="historia" class="scroll-mt-28">
            <div class="flex flex-col lg:flex-row gap-12">
                <div class="flex-1">
                    <h2 class="text-3xl font-bold text-slate-900 mb-10 flex items-center">
                        <span class="w-10 h-10 bg-blue-600 text-white rounded-lg flex items-center justify-center mr-4 text-sm font-bold">02</span>
                        Evolución Histórica
                    </h2>
                    
                    <div class="relative space-y-8 pl-12">
                        <div class="timeline-line"></div>
                        
                        <div class="relative">
                            <div class="absolute -left-[52px] top-0 w-10 h-10 bg-blue-600 rounded-full flex items-center justify-center text-white z-10"><i class="fas fa-rocket text-xs"></i></div>
                            <h4 class="font-bold text-blue-700">1969: ARPANET</h4>
                            <p class="text-slate-600 text-xs">Surgimiento de la primera red de conmutación de paquetes.</p>
                        </div>

                        <div class="relative">
                            <div class="absolute -left-[52px] top-0 w-10 h-10 bg-slate-800 rounded-full flex items-center justify-center text-white z-10"><i class="fas fa-globe text-xs"></i></div>
                            <h4 class="font-bold text-slate-800">1983: Protocolo TCP/IP</h4>
                            <p class="text-slate-600 text-xs">Estandarización que permitió que redes distintas hablaran el mismo idioma.</p>
                        </div>

                        <div class="relative">
                            <div class="absolute -left-[52px] top-0 w-10 h-10 bg-blue-500 rounded-full flex items-center justify-center text-white z-10"><i class="fab fa-google text-xs"></i></div>
                            <h4 class="font-bold text-blue-600">1998: Google y la Indexación Global</h4>
                            <p class="text-slate-600 text-xs">La red se vuelve accesible y organizada para el usuario común.</p>
                        </div>

                        <div class="relative">
                            <div class="absolute -left-[52px] top-0 w-10 h-10 bg-indigo-600 rounded-full flex items-center justify-center text-white z-10"><i class="fas fa-wifi text-xs"></i></div>
                            <h4 class="font-bold text-indigo-700">2000-2005: El Salto Inalámbrico</h4>
                            <p class="text-slate-600 text-xs">Popularización del Wi-Fi y dispositivos móviles conectados.</p>
                        </div>

                        <div class="relative">
                            <div class="absolute -left-[52px] top-0 w-10 h-10 bg-emerald-600 rounded-full flex items-center justify-center text-white z-10"><i class="fas fa-brain text-xs"></i></div>
                            <h4 class="font-bold text-emerald-700">2026: Redes Autónomas</h4>
                            <p class="text-slate-600 text-xs">Integración de IA para la auto-reparación y optimización de redes.</p>
                        </div>
                    </div>
                </div>

                <div class="lg:w-1/3 space-y-6">
                    <div class="bg-indigo-900 text-white p-8 rounded-3xl shadow-xl">
                        <h3 class="font-bold text-xl mb-4 flex items-center italic">
                            <i class="fas fa-history mr-3"></i> Taller de Memoria
                        </h3>
                        <p class="text-sm text-indigo-200 mb-6 underline">Completa los espacios en blanco (Retroalimentación):</p>
                        <div class="space-y-4 text-sm">
                            <p>1. El antecesor directo de Internet se llamó ________.</p>
                            <p>2. En 1983, el cambio al protocolo ________ marcó el inicio de la era moderna.</p>
                            <p>3. El auge del IoT (Internet de las Cosas) ocurrió principalmente después del año ________.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Sección 03: Componentes -->
        <section id="componentes" class="scroll-mt-28">
            <h2 class="text-3xl font-bold text-slate-900 mb-10">Hardware y Dispositivos de Red</h2>
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6 mb-12">
                <div class="bg-white p-6 rounded-3xl border border-slate-200 shadow-sm card-hover">
                    <div class="w-14 h-14 bg-blue-100 text-blue-600 rounded-2xl flex items-center justify-center mb-4 text-2xl"><i class="fas fa-exchange-alt"></i></div>
                    <h3 class="font-bold text-lg mb-2">Switch</h3>
                    <p class="text-xs text-slate-600">Distribuye datos de forma inteligente basándose en la dirección MAC del destino.</p>
                </div>
                <div class="bg-white p-6 rounded-3xl border border-slate-200 shadow-sm card-hover">
                    <div class="w-14 h-14 bg-indigo-100 text-indigo-600 rounded-2xl flex items-center justify-center mb-4 text-2xl"><i class="fas fa-route"></i></div>
                    <h3 class="font-bold text-lg mb-2">Router</h3>
                    <p class="text-xs text-slate-600">El "director de tráfico" que conecta tu red local con el mundo exterior (Internet).</p>
                </div>
                <div class="bg-white p-6 rounded-3xl border border-slate-200 shadow-sm card-hover">
                    <div class="w-14 h-14 bg-slate-100 text-slate-800 rounded-2xl flex items-center justify-center mb-4 text-2xl"><i class="fas fa-server"></i></div>
                    <h3 class="font-bold text-lg mb-2">Servidor</h3>
                    <p class="text-xs text-slate-600">Provee servicios centralizados como bases de datos, correo o almacenamiento web.</p>
                </div>
                <div class="bg-white p-6 rounded-3xl border border-slate-200 shadow-sm card-hover">
                    <div class="w-14 h-14 bg-orange-100 text-orange-600 rounded-2xl flex items-center justify-center mb-4 text-2xl"><i class="fas fa-broadcast-tower"></i></div>
                    <h3 class="font-bold text-lg mb-2">Hub</h3>
                    <p class="text-xs text-slate-600">Repetidor multipuerto que envía la información a todos los equipos, causando colisiones.</p>
                </div>
            </div>

            <div class="bg-slate-100 p-8 rounded-[40px] flex flex-col md:flex-row gap-8 items-center border border-slate-200">
                <div class="text-3xl text-slate-400"><i class="fas fa-tools fa-2x"></i></div>
                <div>
                    <h4 class="font-bold text-slate-800 mb-2">Práctica de Laboratorio: Identificación</h4>
                    <p class="text-sm text-slate-600 leading-relaxed">
                        Dirígete al rack de comunicaciones del Colegio. Identifica cuál de los dispositivos tiene más cables conectados y verifica si es un <span class="font-bold">Switch</span> o un <span class="font-bold">Patch Panel</span>. Anota las marcas de los Routers que encuentres.
                    </p>
                </div>
            </div>
        </section>

        <!-- Sección 04: Tipos de Redes y Ventajas -->
        <section id="tipos" class="scroll-mt-28">
            <h2 class="text-3xl font-bold text-slate-900 mb-10">Análisis Comparativo de Redes</h2>
            <div class="overflow-x-auto bg-white border border-slate-200 rounded-3xl shadow-sm mb-8">
                <table class="w-full text-left border-collapse">
                    <thead class="bg-slate-900 text-white">
                        <tr>
                            <th class="p-4 font-semibold text-xs uppercase tracking-wider">Tipo</th>
                            <th class="p-4 font-semibold text-xs uppercase tracking-wider">Ventaja Principal</th>
                            <th class="p-4 font-semibold text-xs uppercase tracking-wider">Desventaja</th>
                            <th class="p-4 font-semibold text-xs uppercase tracking-wider">Uso Diario</th>
                        </tr>
                    </thead>
                    <tbody class="text-sm divide-y divide-slate-100">
                        <tr>
                            <td class="p-4 font-bold text-blue-600">PAN</td>
                            <td class="p-4">Seguridad personal y bajo costo.</td>
                            <td class="p-4">Radio de acción mínimo (1-10m).</td>
                            <td class="p-4">Auriculares inalámbricos.</td>
                        </tr>
                        <tr>
                            <td class="p-4 font-bold text-blue-600">LAN</td>
                            <td class="p-4">Transferencia de archivos instantánea.</td>
                            <td class="p-4">Requiere cableado o puntos Wi-Fi cercanos.</td>
                            <td class="p-4">Laboratorio de Informática.</td>
                        </tr>
                        <tr>
                            <td class="p-4 font-bold text-blue-600">CAN</td>
                            <td class="p-4">Interconexión de edificios cercanos.</td>
                            <td class="p-4">Costo de fibra óptica entre edificios.</td>
                            <td class="p-4">Campus universitario o escolar.</td>
                        </tr>
                        <tr>
                            <td class="p-4 font-bold text-blue-600">WMAN</td>
                            <td class="p-4">Conectividad inalámbrica ciudadana.</td>
                            <td class="p-4">Saturación por interferencias climáticas.</td>
                            <td class="p-4">Wi-Fi gratuito en parques públicos.</td>
                        </tr>
                        <tr>
                            <td class="p-4 font-bold text-blue-600">WAN</td>
                            <td class="p-4">Acceso a bases de datos mundiales.</td>
                            <td class="p-4">Vulnerable a ciberataques externos.</td>
                            <td class="p-4">Acceso a redes sociales y banca.</td>
                        </tr>
                    </tbody>
                </table>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div class="p-6 bg-emerald-50 rounded-3xl border border-emerald-100">
                    <h4 class="font-bold text-emerald-800 mb-3 flex items-center">
                        <i class="fas fa-check-double mr-2"></i> Retroalimentación Práctica
                    </h4>
                    <p class="text-sm text-emerald-700 leading-relaxed">
                        ¿Qué tipo de red utilizarías para conectar una sucursal del Colegio en Chorrera con la sede central? Justifica tu respuesta basándote en la distancia y los costos mencionados en clase.
                    </p>
                </div>
                <div class="p-6 bg-orange-50 rounded-3xl border border-orange-100">
                    <h4 class="font-bold text-orange-800 mb-3 flex items-center">
                        <i class="fas fa-exclamation-triangle mr-2"></i> Caso de Fallo
                    </h4>
                    <p class="text-sm text-orange-700 leading-relaxed">
                        Si el router principal de una red WAN falla, ¿los equipos de la red LAN interna podrán seguir compartiendo archivos entre sí? Explica por qué.
                    </p>
                </div>
            </div>
        </section>

        <!-- Sección 05: Panamá (Tabla de Datos) -->
        <section id="panama" class="scroll-mt-28">
            <h2 class="text-3xl font-bold text-slate-900 mb-8 flex items-center">
                <i class="fas fa-map-marker-alt text-red-500 mr-4"></i>
                Panorama de Redes en Panamá
            </h2>
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                <div class="lg:col-span-2 overflow-x-auto">
                    <table class="w-full text-sm bg-white border border-slate-200 rounded-3xl overflow-hidden shadow-sm">
                        <thead class="bg-blue-600 text-white">
                            <tr>
                                <th class="p-4 text-left">Infraestructura</th>
                                <th class="p-4 text-left">Situación en Panamá</th>
                                <th class="p-4 text-left">Importancia</th>
                            </tr>
                        </thead>
                        <tbody class="divide-y divide-slate-100">
                            <tr>
                                <td class="p-4 font-bold">Cables Submarinos</td>
                                <td class="p-4">Somos punto de llegada de 7 cables transoceánicos.</td>
                                <td class="p-4">Hub digital de las Américas.</td>
                            </tr>
                            <tr>
                                <td class="p-4 font-bold">Red Fibra Óptica</td>
                                <td class="p-4">Expansión masiva en Panamá Centro y Oeste.</td>
                                <td class="p-4">Teletrabajo y educación 4.0.</td>
                            </tr>
                            <tr>
                                <td class="p-4 font-bold">5G / LTE</td>
                                <td class="p-4">Despliegue inicial de bandas 5G en 2024-25.</td>
                                <td class="p-4">Velocidad móvil ultra-rápida.</td>
                            </tr>
                            <tr>
                                <td class="p-4 font-bold">IXP Panamá</td>
                                <td class="p-4">Punto de Intercambio de Tráfico Local.</td>
                                <td class="p-4">Mantiene los datos locales dentro del país.</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
                <div class="bg-blue-900 text-white p-8 rounded-3xl flex flex-col justify-center text-center">
                    <i class="fas fa-satellite-dish fa-3x mb-4 text-blue-400"></i>
                    <h4 class="font-bold mb-4">Pregunta de Examen</h4>
                    <p class="text-sm text-blue-200 italic">
                        "¿Por qué se dice que Panamá es un Hub de Telecomunicaciones?"
                    </p>
                    <div class="mt-6 p-4 bg-white/10 rounded-xl text-xs text-left">
                        <span class="font-bold text-blue-300">Tip:</span> Investiga la ubicación geográfica de los cables Maya-1 y Pan-Am.
                    </div>
                </div>
            </div>
        </section>

        <!-- Sección 06: Topologías (Definiciones) -->
        <section id="topologias" class="scroll-mt-28">
            <h2 class="text-3xl font-bold text-slate-900 mb-10">Definición de Topologías</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="p-6 bg-white border border-slate-200 rounded-3xl card-hover">
                    <h4 class="font-bold text-blue-600 mb-2 flex justify-between">
                        Estrella <i class="fas fa-star"></i>
                    </h4>
                    <p class="text-xs text-slate-600 leading-relaxed">
                        Todos los nodos se conectan a un concentrador central. <span class="font-semibold">Ventaja:</span> Si falla un cable, los demás siguen funcionando.
                    </p>
                </div>
                <div class="p-6 bg-white border border-slate-200 rounded-3xl card-hover">
                    <h4 class="font-bold text-blue-600 mb-2 flex justify-between">
                        Malla <i class="fas fa-network-wired"></i>
                    </h4>
                    <p class="text-xs text-slate-600 leading-relaxed">
                        Cada nodo está conectado a todos los demás. <span class="font-semibold">Ventaja:</span> Máxima redundancia; nunca se cae la red completa.
                    </p>
                </div>
                <div class="p-6 bg-white border border-slate-200 rounded-3xl card-hover">
                    <h4 class="font-bold text-blue-600 mb-2 flex justify-between">
                        Arbol <i class="fas fa-sitemap"></i>
                    </h4>
                    <p class="text-xs text-slate-600 leading-relaxed">
                        Conexión jerárquica similar a una estrella de estrellas. <span class="font-semibold">Uso:</span> Ideal para separar departamentos en una escuela.
                    </p>
                </div>
                <div class="p-6 bg-white border border-slate-200 rounded-3xl card-hover">
                    <h4 class="font-bold text-blue-600 mb-2 flex justify-between">
                        Mixta <i class="fas fa-layer-group"></i>
                    </h4>
                    <p class="text-xs text-slate-600 leading-relaxed">
                        Combina bus, estrella o anillo según la necesidad física del área. Es la más flexible del mundo real.
                    </p>
                </div>
                <div class="p-6 bg-white border border-slate-200 rounded-3xl card-hover">
                    <h4 class="font-bold text-blue-600 mb-2 flex justify-between">
                        Anillo <i class="fas fa-sync"></i>
                    </h4>
                    <p class="text-xs text-slate-600 leading-relaxed">
                        Los datos viajan en una sola dirección de nodo a nodo. <span class="font-semibold">Desventaja:</span> Difícil de diagnosticar ante fallos.
                    </p>
                </div>
                <div class="p-6 bg-white border border-slate-200 rounded-3xl card-hover">
                    <h4 class="font-bold text-blue-600 mb-2 flex justify-between">
                        Bus <i class="fas fa-minus"></i>
                    </h4>
                    <p class="text-xs text-slate-600 leading-relaxed">
                        Un solo canal de comunicación (troncal). Es económica pero poco fiable para redes modernas con mucho tráfico.
                    </p>
                </div>
            </div>
        </section>

        <!-- Sección 07: Vocabulario -->
        <section id="vocabulario" class="scroll-mt-28">
            <div class="bg-slate-900 text-white p-10 rounded-[40px]">
                <h2 class="text-3xl font-bold mb-8 flex items-center">
                    <i class="fas fa-spell-check mr-4 text-blue-400"></i>
                    Glosario Técnico de Redes
                </h2>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6 text-sm">
                    <div class="border-b border-white/10 pb-4">
                        <span class="text-blue-400 font-bold block mb-1">NIC (Network Interface Card):</span>
                        Hardware que permite a un equipo conectarse físicamente a la red.
                    </div>
                    <div class="border-b border-white/10 pb-4">
                        <span class="text-blue-400 font-bold block mb-1">Nodo:</span>
                        Cualquier punto de conexión (PC, impresora, router) en la red.
                    </div>
                    <div class="border-b border-white/10 pb-4">
                        <span class="text-blue-400 font-bold block mb-1">Cable UTP:</span>
                        Cable de par trenzado no blindado, el estándar para redes LAN.
                    </div>
                    <div class="border-b border-white/10 pb-4">
                        <span class="text-blue-400 font-bold block mb-1">Internet:</span>
                        Infraestructura global que interconecta redes privadas, públicas y académicas.
                    </div>
                    <div class="border-b border-white/10 pb-4">
                        <span class="text-blue-400 font-bold block mb-1">Tarjeta de Red:</span>
                        Sinónimo de NIC, puede ser Ethernet (cable) o Wi-Fi (aire).
                    </div>
                    <div class="border-b border-white/10 pb-4">
                        <span class="text-blue-400 font-bold block mb-1">Red Malla:</span>
                        Topología donde no existe un servidor central, todos colaboran.
                    </div>
                </div>
                
                <div class="mt-10 p-6 bg-white/5 rounded-2xl border border-white/10">
                    <h5 class="font-bold text-blue-400 mb-2">Desafío Final:</h5>
                    <p class="text-xs text-slate-400">Utiliza al menos 4 palabras del glosario anterior para describir cómo te conectas desde tu celular al Wi-Fi de tu casa.</p>
                </div>
            </div>
        </section>

    </main>

    <footer class="bg-slate-900 text-white py-12 px-6 border-t border-white/10">
        <div class="max-w-6xl mx-auto flex flex-col md:flex-row justify-between items-center gap-8">
            <div class="text-center md:text-left">
                <p class="font-bold text-xl mb-2">Colegio Ingeniero Tomás Guardia</p>
                <p class="text-slate-400 text-sm">Departamento de Informática - 11° Bachiller</p>
                <p class="text-slate-600 text-xs mt-4 italic">"La tecnología es el puente hacia el futuro"</p>
            </div>
            <div class="text-center md:text-right">
                <p class="text-xs text-slate-500 uppercase tracking-widest font-bold">Guía de Estudios 2026</p>
                <p class="text-blue-400 font-bold text-sm">Profa. Rosa Robles Pino</p>
            </div>
        </div>
    </footer>

</body>
</html>
