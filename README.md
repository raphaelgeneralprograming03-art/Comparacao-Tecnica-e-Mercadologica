
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Visão Geral & Matriz Comparativa: Sistema Autónomo vs Drones Padrão</title>
    <style>
        :root {
            --bg-color: #07090f;
            --panel-bg: #0d131f;
            --accent-green: #10b981;
            --accent-amber: #f59e0b;
            --accent-red: #ef4444;
            --accent-blue: #3b82f6;
            --text-main: #f3f4f6;
            --text-muted: #9ca3af;
            --border-color: #1e293b;
        }
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Courier New', Courier, monospace;
        }
        body {
            background-color: var(--bg-color);
            color: var(--text-main);
            display: flex;
            flex-direction: column;
            min-height: 100vh;
            padding: 15px;
        }
        header {
            background: var(--panel-bg);
            border: 1px solid var(--border-color);
            padding: 15px 20px;
            margin-bottom: 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-radius: 6px;
        }
        header h1 {
            font-size: 1.1rem;
            color: var(--accent-green);
            letter-spacing: 1px;
        }
        .author-badge {
            background: rgba(16, 185, 129, 0.12);
            color: var(--accent-green);
            border: 1px solid var(--accent-green);
            padding: 6px 12px;
            border-radius: 4px;
            font-size: 0.75rem;
            font-weight: bold;
        }
        .main-container {
            display: grid;
            grid-template-columns: 1.1fr 0.9fr;
            gap: 15px;
            flex: 1;
        }
        @media(max-width: 1100px) {
            .main-container {
                grid-template-columns: 1fr;
            }
        }
        .panel {
            background: var(--panel-bg);
            border: 1px solid var(--border-color);
            border-radius: 6px;
            padding: 15px;
            display: flex;
            flex-direction: column;
            gap: 12px;
        }
        .panel-title {
            font-size: 0.85rem;
            color: var(--accent-amber);
            border-bottom: 1px solid var(--border-color);
            padding-bottom: 8px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }
        /* Tabela de Matriz Comparativa */
        .comparison-table {
            width: 100%;
            border-collapse: collapse;
            font-size: 0.73rem;
            margin-bottom: 5px;
        }
        .comparison-table th, .comparison-table td {
            border: 1px solid var(--border-color);
            padding: 7px;
            text-align: left;
        }
        .comparison-table th {
            background: #111a2c;
            color: var(--text-main);
        }
        .col-standard {
            color: var(--accent-red);
            background: rgba(239, 68, 68, 0.04);
        }
        .col-proposed {
            color: var(--accent-green);
            background: rgba(16, 185, 129, 0.04);
            font-weight: bold;
        }
        /* Canvas de Simulação */
        .canvas-wrapper {
            position: relative;
            background: #020408;
            border: 1px solid var(--border-color);
            display: flex;
            justify-content: center;
            align-items: center;
            border-radius: 4px;
            flex: 1;
            min-height: 340px;
        }
        canvas {
            display: block;
            cursor: crosshair;
        }
        .controls-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 8px;
        }
        button {
            background: #1e293b;
            color: var(--text-main);
            border: 1px solid var(--border-color);
            padding: 9px 12px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 0.78rem;
            transition: all 0.2s;
        }
        button:hover {
            background: #334155;
            border-color: var(--accent-green);
            color: var(--accent-green);
        }
        button.active-mode {
            background: rgba(16, 185, 129, 0.2);
            border-color: var(--accent-green);
            color: var(--accent-green);
        }
        button.danger-mode {
            background: rgba(239, 68, 68, 0.2);
            border-color: var(--accent-red);
            color: var(--accent-red);
        }
        .telemetry-box {
            background: #04060a;
            border: 1px solid var(--border-color);
            padding: 10px;
            border-radius: 4px;
            font-size: 0.78rem;
            display: flex;
            flex-direction: column;
            gap: 5px;
        }
        .telemetry-row {
            display: flex;
            justify-content: space-between;
        }
        .serial-console {
            background: #020305;
            color: var(--accent-green);
            border: 1px solid var(--border-color);
            padding: 8px;
            border-radius: 4px;
            font-size: 0.7rem;
            height: 95px;
            overflow-y: auto;
            white-space: pre-wrap;
        }
        .overview-desc {
            font-size: 0.76rem;
            line-height: 1.35;
            color: var(--text-muted);
            background: #090d16;
            padding: 9px;
            border-radius: 4px;
            border-left: 3px solid var(--accent-blue);
        }
    </style>
</head>
<body>

    <header>
        <div>
            <h1>VISÃO GERAL DO APLICATIVO & MATRIZ DE COMPARAÇÃO</h1>
            <p style="font-size: 0.7rem; color: var(--text-muted);">Simulador Tático de Guiagem Autônoma vs. Arquitetura Comercial Vulnerável</p>
        </div>
        <div class="author-badge">SISTEMA: RAFAEL SILVA (DSMAC / ATR)</div>
    </header>

    <div class="main-container">
        <!-- Coluna Esquerda: Matriz de Comparação & Visão Geral -->
        <div class="panel">
            <div class="panel-title">Visão Geral do Aplicativo & Memorial Descritivo</div>
            <div class="overview-desc">
                Esta aplicação simula a arquitetura de alta confiabilidade desenvolvida por Rafael Silva, contrapondo-se aos drones comerciais convencionais. O sistema elimina vulnerabilidades críticas de guerra eletrônica, satélites e nuvem, operando em silêncio de rádio absoluto com IA de borda local e barramento blindado.
            </div>

            <div class="panel-title" style="margin-top: 5px;">Matriz de Comparação Técnica e Mercadológica</div>
            <table class="comparison-table">
                <thead>
                    <tr>
                        <th>Recurso Técnico</th>
                        <th>Drones Comerciais Padrão</th>
                        <th>Sistema Autônomo Proposto (Rafael Silva)</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td><strong>Dependência de GPS / Satélite</strong></td>
                        <td class="col-standard">Contínua (Vulnerável a Spoofing)</td>
                        <td class="col-proposed">Apenas Inicial (Redundância em Background)</td>
                    </tr>
                    <tr>
                        <td><strong>Emissão Eletromagnética</strong></td>
                        <td class="col-standard">Alta (Rastreável por Guerra Eletrônica)</td>
                        <td class="col-proposed">Zero Emissão Local (Silêncio de Rádio Total)</td>
                    </tr>
                    <tr>
                        <td><strong>Mecanismo de Perseguição</strong></td>
                        <td class="col-standard">Cálculo de Vetores Remotos / Nuvem</td>
                        <td class="col-proposed">Algoritmo ATR Local por Assinatura Digital</td>
                    </tr>
                    <tr>
                        <td><strong>Comunicação Mestre-Escravo</strong></td>
                        <td class="col-standard">Protocolos Proprietários s/ Criptografia</td>
                        <td class="col-proposed">Hardware Dedicado com Barramento Blindado</td>
                    </tr>
                </tbody>
            </table>

            <div class="panel-title" style="margin-top: 5px;">Controles do Cenário de Simulação</div>
            <div class="controls-grid">
                <button id="btnToggleSystem" class="active-mode">Modo: Sistema Rafael Silva</button>
                <button id="btnSpoofing" class="danger-mode">Disparar Ataque de Spoofing GPS</button>
                <button id="btnReset" style="grid-column: span 2;">Reiniciar Posição dos Vetores</button>
            </div>
            <p style="font-size: 0.68rem; color: var(--text-muted);">* Clique no botão de Spoofing para injetar interferência eletromagnética na área de operação.</p>
        </div>

        <!-- Coluna Direita: Canvas de Simulação & Telemetria -->
        <div class="panel">
            <div class="panel-title">Simulador Gráfico em Tempo Real (Canvas 2D)</div>
            <div class="canvas-wrapper">
                <canvas id="simCanvas" width="560" height="310"></canvas>
            </div>

            <div class="panel-title">Telemetria de Campo & Emissão RF</div>
            <div class="telemetry-box">
                <div class="telemetry-row"><span>Modo de Operação Ativo:</span> <span id="valMode" style="color:var(--accent-green)">Sistema Autônomo (Rafael Silva)</span></div>
                <div class="telemetry-row"><span>Estado do GPS / Satélite:</span> <span id="valGps" style="color:var(--accent-green)">Redundância Inicial / Travado</span></div>
                <div class="telemetry-row"><span>Assinatura RF (Emissão Eletromagnética):</span> <span id="valRf" style="color:var(--accent-green)">0 dBm [Silêncio Absoluto]</span></div>
                <div class="telemetry-row"><span>Algoritmo de Perseguição:</span> <span id="valAlgo" style="color:var(--accent-amber)">ATR Local (OpenCV CSRT + Arduino)</span></div>
            </div>

            <div class="panel-title">Log do Sistema Local</div>
            <div class="serial-console" id="serialConsole">[INIT] Aplicativo inicializado com sucesso.
[SYSTEM] Arquitetura de Guiagem DSMAC/ATR carregada.
[STATUS] Silêncio de rádio ativo. Barramento blindado operacional.</div>
        </div>
    </div>

    <script>
        const canvas = document.getElementById('simCanvas');
        const ctx = canvas.getContext('2d');

        // Estados do Sistema
        let useProposedSystem = true; // true = Rafael Silva, false = Drone Comercial Padrão
        let spoofingActive = false;

        // Alvo e Drone
        let target = { x: 420, y: 155, vx: 1.2, radius: 10 };
        let drone = { x: 120, y: 155, angle: 0 };
        let commercialDrone = { x: 120, y: 155, errX: 0, errY: 0 };

        // Elementos UI
        const btnToggleSystem = document.getElementById('btnToggleSystem');
        const btnSpoofing = document.getElementById('btnSpoofing');
        const btnReset = document.getElementById('btnReset');
        const valMode = document.getElementById('valMode');
        const valGps = document.getElementById('valGps');
        const valRf = document.getElementById('valRf');
        const valAlgo = document.getElementById('valAlgo');
        const serialConsole = document.getElementById('serialConsole');

        function logMsg(msg) {
            serialConsole.textContent += "\n" + msg;
            serialConsole.scrollTop = serialConsole.scrollHeight;
        }

        btnToggleSystem.addEventListener('click', () => {
            useProposedSystem = !useProposedSystem;
            if (useProposedSystem) {
                btnToggleSystem.textContent = "Modo: Sistema Rafael Silva";
                btnToggleSystem.className = "active-mode";
                valMode.textContent = "Sistema Autônomo (Rafael Silva)";
                valMode.style.color = "var(--accent-green)";
                valGps.textContent = "Redundância Inicial / Travado";
                valGps.style.color = "var(--accent-green)";
                valRf.textContent = "0 dBm [Silêncio Absoluto]";
                valRf.style.color = "var(--accent-green)";
                valAlgo.textContent = "ATR Local (OpenCV CSRT + Arduino)";
                logMsg("[SWITCH] Sistema alterado para: Sistema Autônomo Proposto (Zero emissão, ATR Local).");
            } else {
                btnToggleSystem.textContent = "Modo: Drone Comercial Padrão";
                btnToggleSystem.className = "danger-mode";
                valMode.textContent = "Drone Comercial Padrão";
                valMode.style.color = "var(--accent-red)";
                valGps.textContent = "Dependência Contínua de GPS";
                valGps.style.color = "var(--accent-red)";
                valRf.textContent = "Alta Emissão (Rastreável por EW)";
                valRf.style.color = "var(--accent-red)";
                valAlgo.textContent = "Cálculo de Vetores em Nuvem / Remoto";
                logMsg("[SWITCH] Alerta: Alterado para Drone Comercial Padrão (Vulnerável a Spoofing e EW).");
            }
        });

        btnSpoofing.addEventListener('click', () => {
            spoofingActive = !spoofingActive;
            if (spoofingActive) {
                btnSpoofing.textContent = "Desativar Ataque de Spoofing";
                logMsg("[GUERRA ELETRÔNICA] ATENÇÃO: Sinal de Spoofing GPS / Interferência injetado no ambiente!");
                if (!useProposedSystem) {
                    logMsg("[DRONE COMERCIAL] ERRO CRÍTICO: Perda de controle por satélite falso! Desvio de rota iniciado.");
                } else {
                    logMsg("[SISTEMA RAFAEL SILVA] Imune: Sistema operando com ATR local e redundância em background. Rota inalterada.");
                }
            } else {
                btnSpoofing.textContent = "Disparar Ataque de Spoofing GPS";
                logMsg("[GUERRA ELETRÔNICA] Interferência GPS encerrada.");
            }
        });

        btnReset.addEventListener('click', () => {
            target.x = 380 + Math.random() * 100;
            target.y = 80 + Math.random() * 150;
            drone.x = 120; drone.y = 155;
            commercialDrone.x = 120; commercialDrone.y = 155;
            commercialDrone.errX = 0; commercialDrone.errY = 0;
            logMsg("[SYSTEM] Posições iniciais restauradas.");
        });

        function update() {
            // Movimentação do alvo
            target.y += target.vx;
            if (target.y < 50 || target.y > canvas.height - 50) target.vx *= -1;

            if (useProposedSystem) {
                // Sistema Proposto: Persegue o alvo com ATR local, ignorando spoofing (sem cloud/GPS contínuo)
                drone.x += (target.x - drone.x) * 0.035;
                drone.y += (target.y - drone.y) * 0.035;
            } else {
                // Drone Comercial Padrão: Depende de nuvem/GPS. Se spoofing ativo, desvia erraticamente
                if (spoofingActive) {
                    commercialDrone.errX += (Math.random() - 0.5) * 8;
                    commercialDrone.errY += (Math.random() - 0.5) * 8;
                } else {
                    commercialDrone.errX += (0 - commercialDrone.errX) * 0.1;
                    commercialDrone.errY += (0 - commercialDrone.errY) * 0.1;
                }
                commercialDrone.x += (target.x - commercialDrone.x) * 0.02 + (Math.random() - 0.5) * 2;
                commercialDrone.y += (target.y - commercialDrone.y) * 0.02 + commercialDrone.errY * 0.1;
            }
        }

        function draw() {
            ctx.fillStyle = '#020408';
            ctx.fillRect(0, 0, canvas.width, canvas.height);

            // Grade de radar tática
            ctx.strokeStyle = '#101826';
            ctx.lineWidth = 1;
            for (let x = 0; x < canvas.width; x += 40) {
                ctx.beginPath(); ctx.moveTo(x, 0); ctx.lineTo(x, canvas.height); ctx.stroke();
            }
            for (let y = 0; y < canvas.height; y += 40) {
                ctx.beginPath(); ctx.moveTo(0, y); ctx.lineTo(canvas.width, y); ctx.stroke();
            }

            // Desenhar Alvo
            ctx.fillStyle = '#f59e0b';
            ctx.beginPath();
            ctx.arc(target.x, target.y, target.radius, 0, Math.PI * 2);
            ctx.fill();
            ctx.fillStyle = '#ffffff';
            ctx.font = '9px Courier New';
            ctx.fillText("ALVO MÓVEL", target.x - 30, target.y - 15);

            if (useProposedSystem) {
                // Desenhar Sistema Rafael Silva
                // Ondas de silêncio (ou ausência de radar inimigo detectando)
                ctx.strokeStyle = 'rgba(16, 185, 129, 0.3)';
                ctx.lineWidth = 1;
                ctx.beginPath(); ctx.arc(drone.x, drone.y, 25, 0, Math.PI * 2); ctx.stroke();

                // Ícone do Drone Proposto
                ctx.fillStyle = '#10b981';
                ctx.beginPath();
                ctx.arc(drone.x, drone.y, 8, 0, Math.PI * 2);
                ctx.fill();

                // Linha de mira ATR (Assinatura Digital)
                ctx.strokeStyle = '#10b981';
                ctx.setLineDash([4, 4]);
                ctx.beginPath();
                ctx.moveTo(drone.x, drone.y);
                ctx.lineTo(target.x, target.y);
                ctx.stroke();
                ctx.setLineDash([]);

                ctx.fillStyle = '#10b981';
                ctx.fillText("SISTEMA RAFAEL SILVA [ATR LOC]", drone.x - 45, drone.y + 22);

                if (spoofingActive) {
                    ctx.fillStyle = '#10b981';
                    ctx.fillText("STATUS: IMUNE A SPOOFING (GPS ISOLADO)", 15, 20);
                }
            } else {
                // Desenhar Drone Comercial Padrão
                // Emissão eletromagnética alta visível ao radar inimigo
                if (Math.floor(Date.now() / 200) % 2 === 0) {
                    ctx.strokeStyle = 'rgba(239, 68, 68, 0.6)';
                    ctx.lineWidth = 2;
                    ctx.beginPath(); ctx.arc(commercialDrone.x, commercialDrone.y, 35, 0, Math.PI * 2); ctx.stroke();
                }

                ctx.fillStyle = '#ef4444';
                ctx.beginPath();
                ctx.arc(commercialDrone.x, commercialDrone.y, 8, 0, Math.PI * 2);
                ctx.fill();

                // Linha de comunicação nuvem vulnerável
                ctx.strokeStyle = '#ef4444';
                ctx.setLineDash([2, 2]);
                ctx.beginPath();
                ctx.moveTo(commercialDrone.x, commercialDrone.y);
                ctx.lineTo(target.x, target.y);
                ctx.stroke();
                ctx.setLineDash([]);

                ctx.fillStyle = '#ef4444';
                ctx.fillText("DRONE COMERCIAL [CLOUD/GPS]", commercialDrone.x - 45, commercialDrone.y + 22);

                if (spoofingActive) {
                    ctx.fillStyle = '#ef4444';
                    ctx.fillText("STATUS: VULNERÁVEL - PERDIDO EM ROTA FALSA", 15, 20);
                }
            }
        }

        function loop() {
            update();
            draw();
            requestAnimationFrame(loop);
        }

        requestAnimationFrame(loop);
    </script>
</body>
</html>
