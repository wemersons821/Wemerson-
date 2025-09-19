<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Guia Completo: Como Crescer na Academia</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        .chapter-content {
            display: none;
        }
        .chapter-content.active {
            display: block;
        }
        .progress-bar {
            transition: width 0.3s ease;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .fade-in {
            animation: fadeIn 0.5s ease-out;
        }
    </style>
</head>
<body class="bg-gradient-to-br from-blue-900 via-purple-900 to-indigo-900 min-h-screen text-white">
    <!-- Header -->
    <header class="bg-black/30 backdrop-blur-sm border-b border-white/10 sticky top-0 z-50">
        <div class="container mx-auto px-6 py-4">
            <div class="flex items-center justify-between">
                <h1 class="text-2xl font-bold bg-gradient-to-r from-blue-400 to-purple-400 bg-clip-text text-transparent">
                    💪 Guia Completo: Como Crescer na Academia
                </h1>
                <div class="flex flex-col sm:flex-row items-center gap-4">
                    <button onclick="downloadEbook()" class="bg-green-600 hover:bg-green-500 px-6 py-3 rounded-lg text-base font-bold transition-colors flex items-center space-x-2 shadow-lg hover:shadow-xl transform hover:scale-105 w-full sm:w-auto justify-center">
                        <span class="text-xl">📥</span>
                        <span>BAIXAR E-BOOK</span>
                    </button>
                    <div class="flex items-center space-x-3">
                        <div class="text-sm text-gray-300">
                            Progresso: <span id="progress-text">0%</span>
                        </div>
                        <div class="w-24 sm:w-32 h-2 bg-gray-700 rounded-full overflow-hidden">
                            <div id="progress-bar" class="progress-bar h-full bg-gradient-to-r from-blue-500 to-purple-500 w-0"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <div class="container mx-auto px-4 sm:px-6 py-8 flex flex-col lg:flex-row gap-6 lg:gap-8">
        <!-- Sidebar Navigation -->
        <nav class="w-full lg:w-80 bg-black/20 backdrop-blur-sm rounded-2xl p-4 sm:p-6 h-fit lg:sticky lg:top-24">
            <h2 class="text-xl font-bold mb-6 text-center">📚 Índice</h2>
            <ul class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-1 gap-2 lg:gap-3">
                <li><button onclick="showChapter('intro')" class="nav-btn w-full text-left p-3 rounded-lg hover:bg-white/10 transition-colors active text-sm sm:text-base">Introdução</button></li>
                <li><button onclick="showChapter('fundamentos')" class="nav-btn w-full text-left p-3 rounded-lg hover:bg-white/10 transition-colors text-sm sm:text-base">1. Fundamentos</button></li>
                <li><button onclick="showChapter('treino')" class="nav-btn w-full text-left p-3 rounded-lg hover:bg-white/10 transition-colors text-sm sm:text-base">2. Treino</button></li>
                <li><button onclick="showChapter('nutricao')" class="nav-btn w-full text-left p-3 rounded-lg hover:bg-white/10 transition-colors text-sm sm:text-base">3. Nutrição</button></li>
                <li><button onclick="showChapter('descanso')" class="nav-btn w-full text-left p-3 rounded-lg hover:bg-white/10 transition-colors text-sm sm:text-base">4. Descanso</button></li>
                <li><button onclick="showChapter('suplementos')" class="nav-btn w-full text-left p-3 rounded-lg hover:bg-white/10 transition-colors text-sm sm:text-base">5. Suplementos</button></li>
                <li><button onclick="showChapter('motivacao')" class="nav-btn w-full text-left p-3 rounded-lg hover:bg-white/10 transition-colors text-sm sm:text-base">6. Motivação</button></li>
                <li><button onclick="showChapter('erros')" class="nav-btn w-full text-left p-3 rounded-lg hover:bg-white/10 transition-colors text-sm sm:text-base">7. Erros Comuns</button></li>
                <li><button onclick="showChapter('conclusao')" class="nav-btn w-full text-left p-3 rounded-lg hover:bg-white/10 transition-colors text-sm sm:text-base">Conclusão</button></li>
            </ul>
        </nav>

        <!-- Main Content -->
        <main class="flex-1 bg-black/20 backdrop-blur-sm rounded-2xl p-4 sm:p-6 lg:p-8">
            <!-- Introdução -->
            <div id="intro" class="chapter-content active fade-in">
                <h2 class="text-4xl font-bold mb-6 bg-gradient-to-r from-blue-400 to-purple-400 bg-clip-text text-transparent">
                    🚀 Introdução
                </h2>
                <div class="prose prose-invert max-w-none">
                    <p class="text-lg mb-6 leading-relaxed">
                        Bem-vindo ao guia definitivo para crescer na academia! Este e-book foi criado para te ajudar a maximizar seus resultados, seja você iniciante ou já tenha experiência com musculação.
                    </p>
                    <div class="bg-gradient-to-r from-blue-600/20 to-purple-600/20 p-6 rounded-xl border border-blue-500/30 mb-6">
                        <h3 class="text-xl font-semibold mb-3">🎯 O que você vai aprender:</h3>
                        <ul class="space-y-2">
                            <li>✅ Princípios científicos do crescimento muscular</li>
                            <li>✅ Como estruturar treinos eficientes</li>
                            <li>✅ Estratégias nutricionais comprovadas</li>
                            <li>✅ A importância do descanso</li>
                            <li>✅ Suplementação inteligente</li>
                            <li>✅ Como manter a motivação</li>
                        </ul>
                    </div>
                    <p class="text-gray-300">
                        Crescer na academia não é apenas sobre levantar pesos pesados. É sobre entender como seu corpo funciona, criar hábitos sustentáveis e ser consistente ao longo do tempo. Vamos começar essa jornada juntos!
                    </p>
                </div>
            </div>

            <!-- Capítulo 1: Fundamentos -->
            <div id="fundamentos" class="chapter-content">
                <h2 class="text-4xl font-bold mb-6 bg-gradient-to-r from-blue-400 to-purple-400 bg-clip-text text-transparent">
                    🧬 Capítulo 1: Fundamentos do Crescimento
                </h2>
                <div class="prose prose-invert max-w-none">
                    <h3 class="text-2xl font-semibold mb-4">Como os Músculos Crescem</h3>
                    <p class="mb-6">
                        O crescimento muscular (hipertrofia) acontece quando você cria micro-lesões nas fibras musculares através do treino, e seu corpo as repara tornando-as maiores e mais fortes.
                    </p>
                    
                    <div class="grid md:grid-cols-2 gap-6 mb-8">
                        <div class="bg-green-600/20 p-6 rounded-xl border border-green-500/30">
                            <h4 class="text-lg font-semibold mb-3">🔬 Processo de Hipertrofia</h4>
                            <ol class="space-y-2 text-sm">
                                <li>1. Estímulo (treino de força)</li>
                                <li>2. Micro-lesões nas fibras</li>
                                <li>3. Resposta inflamatória</li>
                                <li>4. Síntese proteica</li>
                                <li>5. Crescimento muscular</li>
                            </ol>
                        </div>
                        <div class="bg-blue-600/20 p-6 rounded-xl border border-blue-500/30">
                            <h4 class="text-lg font-semibold mb-3">⚡ Fatores Essenciais</h4>
                            <ul class="space-y-2 text-sm">
                                <li>• Sobrecarga progressiva</li>
                                <li>• Volume adequado</li>
                                <li>• Frequência de treino</li>
                                <li>• Tempo sob tensão</li>
                                <li>• Recuperação adequada</li>
                            </ul>
                        </div>
                    </div>

                    <h3 class="text-2xl font-semibold mb-4">Princípio da Sobrecarga Progressiva</h3>
                    <p class="mb-4">
                        Este é o princípio mais importante para o crescimento. Você deve constantemente desafiar seus músculos aumentando:
                    </p>
                    <ul class="list-disc list-inside space-y-2 mb-6 text-gray-300">
                        <li>Peso (carga)</li>
                        <li>Repetições</li>
                        <li>Séries</li>
                        <li>Frequência</li>
                        <li>Densidade (menos descanso)</li>
                    </ul>
                </div>
            </div>

            <!-- Capítulo 2: Treino -->
            <div id="treino" class="chapter-content">
                <h2 class="text-4xl font-bold mb-6 bg-gradient-to-r from-blue-400 to-purple-400 bg-clip-text text-transparent">
                    🏋️ Capítulo 2: Treino Eficiente
                </h2>
                <div class="prose prose-invert max-w-none">
                    <h3 class="text-2xl font-semibold mb-4">Estrutura do Treino Ideal</h3>
                    
                    <div class="bg-yellow-600/20 p-6 rounded-xl border border-yellow-500/30 mb-6">
                        <h4 class="text-lg font-semibold mb-3">📋 Parâmetros Recomendados</h4>
                        <div class="grid md:grid-cols-2 gap-4 text-sm">
                            <div>
                                <strong>Frequência:</strong> 3-6x por semana<br>
                                <strong>Séries por músculo:</strong> 10-20 por semana<br>
                                <strong>Repetições:</strong> 6-20 (hipertrofia)
                            </div>
                            <div>
                                <strong>Descanso entre séries:</strong> 2-3 min<br>
                                <strong>Tempo de treino:</strong> 45-90 min<br>
                                <strong>Intensidade:</strong> 65-85% 1RM
                            </div>
                        </div>
                    </div>

                    <h3 class="text-2xl font-semibold mb-4">Exercícios Fundamentais</h3>
                    
                    <div class="grid md:grid-cols-2 gap-6 mb-8">
                        <div class="bg-red-600/20 p-6 rounded-xl border border-red-500/30">
                            <h4 class="text-lg font-semibold mb-3">🔥 Exercícios Compostos</h4>
                            <ul class="space-y-2 text-sm">
                                <li>• Agachamento</li>
                                <li>• Levantamento terra</li>
                                <li>• Supino</li>
                                <li>• Remada</li>
                                <li>• Desenvolvimento</li>
                                <li>• Barra fixa</li>
                            </ul>
                        </div>
                        <div class="bg-purple-600/20 p-6 rounded-xl border border-purple-500/30">
                            <h4 class="text-lg font-semibold mb-3">🎯 Exercícios Isolados</h4>
                            <ul class="space-y-2 text-sm">
                                <li>• Rosca bíceps</li>
                                <li>• Tríceps pulley</li>
                                <li>• Elevação lateral</li>
                                <li>• Leg curl</li>
                                <li>• Panturrilha</li>
                                <li>• Abdominal</li>
                            </ul>
                        </div>
                    </div>

                    <h3 class="text-2xl font-semibold mb-4">Divisão de Treino</h3>
                    <p class="mb-4">Exemplo de divisão ABC (3x por semana):</p>
                    
                    <div class="space-y-4">
                        <div class="bg-gray-800/50 p-4 rounded-lg">
                            <strong class="text-blue-400">Treino A - Peito, Ombro, Tríceps</strong>
                            <p class="text-sm text-gray-300 mt-2">Supino, desenvolvimento, crucifixo, elevação lateral, tríceps</p>
                        </div>
                        <div class="bg-gray-800/50 p-4 rounded-lg">
                            <strong class="text-green-400">Treino B - Costas, Bíceps</strong>
                            <p class="text-sm text-gray-300 mt-2">Remada, pulldown, barra fixa, rosca bíceps</p>
                        </div>
                        <div class="bg-gray-800/50 p-4 rounded-lg">
                            <strong class="text-red-400">Treino C - Pernas, Abdômen</strong>
                            <p class="text-sm text-gray-300 mt-2">Agachamento, leg press, stiff, panturrilha, abdominais</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Capítulo 3: Nutrição -->
            <div id="nutricao" class="chapter-content">
                <h2 class="text-4xl font-bold mb-6 bg-gradient-to-r from-blue-400 to-purple-400 bg-clip-text text-transparent">
