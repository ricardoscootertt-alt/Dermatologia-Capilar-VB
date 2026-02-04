<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vanessa Braga - Dermatologia Capilar</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&family=Playfair+Display:ital,wght@0,700;1,700&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Inter', sans-serif; background-color: #f1f5f9; }
        .serif { font-family: 'Playfair Display', serif; }
        .step-content { display: none; }
        .step-content.active { display: block; animation: fadeIn 0.4s ease-out; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
        .recommendation-paper { background: radial-gradient(#e2e8f0 1px, transparent 1px); background-size: 20px 20px; background-color: white; }
        @media print { .no-print { display: none; } body { background: white; } }
    </style>
</head>
<body class="text-slate-900">

    <div id="app" class="max-w-2xl mx-auto min-h-screen pb-12">
        <!-- Header Principal -->
        <nav class="p-6 flex justify-between items-center no-print">
            <div class="flex items-center gap-3">
                <div class="w-12 h-12 bg-slate-900 rounded-2xl flex items-center justify-center text-amber-500 shadow-xl">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10"/><circle cx="12" cy="11" r="3"/></svg>
                </div>
                <div>
                    <h1 class="serif text-xl font-bold leading-none tracking-tight">Vanessa Braga</h1>
                    <p class="text-[9px] tracking-[0.4em] text-slate-500 uppercase font-black">Dermatologia Capilar</p>
                </div>
            </div>
            <div class="flex gap-2">
                <div class="w-10 h-10 rounded-full border border-slate-200 flex items-center justify-center bg-white"><svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-slate-400"><path d="M19 21v-2a4 4 0 0 0-4-4H9a4 4 0 0 0-4 4v2"/><circle cx="12" cy="7" r="4"/></svg></div>
            </div>
        </nav>

        <!-- Container de Triagem -->
        <main class="px-4">
            
            <!-- STEP 1: Perfil do Paciente -->
            <div id="step-1" class="step-content active space-y-6">
                <div class="bg-slate-900 p-8 rounded-[2.5rem] text-white shadow-2xl overflow-hidden relative">
                    <div class="relative z-10">
                        <h2 class="text-2xl font-bold mb-2">Triagem Técnica</h2>
                        <p class="text-slate-400 text-sm">Inicie o protocolo de atendimento personalizado.</p>
                    </div>
                    <svg class="absolute right-[-20px] bottom-[-20px] opacity-10" width="200" height="200" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1"><path d="M14.5 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V7.5L14.5 2z"/><polyline points="14 2 14 8 20 8"/></svg>
                </div>

                <div class="bg-white p-8 rounded-[2rem] shadow-sm border border-slate-200 space-y-5">
                    <div>
                        <label class="text-[10px] font-black text-slate-400 uppercase ml-2 tracking-widest">Nome Completo</label>
                        <input type="text" id="p-name" placeholder="Nome do paciente" class="w-full p-4 bg-slate-50 border-none rounded-2xl mt-1 focus:ring-2 focus:ring-slate-900 outline-none">
                    </div>
                    <div class="grid grid-cols-2 gap-4">
                        <div>
                            <label class="text-[10px] font-black text-slate-400 uppercase ml-2 tracking-widest">Idade</label>
                            <input type="number" id="p-age" placeholder="Ex: 30" class="w-full p-4 bg-slate-50 border-none rounded-2xl mt-1 focus:ring-2 focus:ring-slate-900 outline-none">
                        </div>
                        <div>
                            <label class="text-[10px] font-black text-slate-400 uppercase ml-2 tracking-widest">Sexo</label>
                            <select id="p-gender" class="w-full p-4 bg-slate-50 border-none rounded-2xl mt-1 focus:ring-2 focus:ring-slate-900 outline-none">
                                <option value="Feminino">Feminino</option>
                                <option value="Masculino">Masculino</option>
                            </select>
                        </div>
                    </div>
                    <button onclick="goToStep(2)" class="w-full bg-slate-900 text-white py-5 rounded-2xl font-bold uppercase tracking-widest text-xs shadow-lg active:scale-95 transition-all">Iniciar Avaliação</button>
                </div>
            </div>

            <!-- STEP 2: Condições e Comorbidades -->
            <div id="step-2" class="step-content space-y-6">
                <div class="flex items-center gap-4 mb-4">
                    <button onclick="goToStep(1)" class="p-2 bg-white rounded-full shadow-sm"><svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m15 18-6-6 6-6"/></svg></button>
                    <h2 class="font-bold text-slate-800">Condições de Saúde</h2>
                </div>

                <div class="bg-white p-8 rounded-[2rem] shadow-sm space-y-3">
                    <p class="text-xs text-slate-400 font-bold uppercase mb-4 tracking-tighter">Assinale as condições pré-existentes:</p>
                    
                    <div class="grid grid-cols-1 gap-3" id="comorbidity-list">
                        <label class="flex items-center justify-between p-4 border rounded-2xl cursor-pointer hover:bg-slate-50 transition-colors">
                            <span class="font-medium text-slate-700">Diabetes Mellitus</span>
                            <input type="checkbox" value="Diabetes" class="comorb-check w-5 h-5 accent-slate-900">
                        </label>
                        <label class="flex items-center justify-between p-4 border rounded-2xl cursor-pointer hover:bg-slate-50 transition-colors">
                            <span class="font-medium text-slate-700">Hipertensão Arterial</span>
                            <input type="checkbox" value="Hipertensão" class="comorb-check w-5 h-5 accent-slate-900">
                        </label>
                        <label class="flex items-center justify-between p-4 border rounded-2xl cursor-pointer hover:bg-slate-50 transition-colors">
                            <span class="font-medium text-slate-700">Gestante ou Lactante</span>
                            <input type="checkbox" value="Gestante/Lactante" class="comorb-check w-5 h-5 accent-slate-900">
                        </label>
                        <label class="flex items-center justify-between p-4 border rounded-2xl cursor-pointer hover:bg-slate-50 transition-colors">
                            <span class="font-medium text-slate-700">Tireoide (Alterações)</span>
                            <input type="checkbox" value="Tireoide" class="comorb-check w-5 h-5 accent-slate-900">
                        </label>
                        <label class="flex items-center justify-between p-4 border rounded-2xl cursor-pointer hover:bg-slate-50 transition-colors">
                            <span class="font-medium text-slate-700">Alergia a Medicamentos</span>
                            <input type="checkbox" value="Alergia Medicamentosa" class="comorb-check w-5 h-5 accent-slate-900">
                        </label>
                    </div>

                    <button onclick="goToStep(3)" class="w-full bg-slate-900 text-white py-5 rounded-2xl font-bold uppercase tracking-widest text-xs mt-6">Continuar</button>
                </div>
            </div>

            <!-- STEP 3: Causa e Gatilho -->
            <div id="step-3" class="step-content space-y-6">
                <div class="flex items-center gap-4 mb-4">
                    <button onclick="goToStep(2)" class="p-2 bg-white rounded-full shadow-sm"><svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m15 18-6-6 6-6"/></svg></button>
                    <h2 class="font-bold text-slate-800">Etiologia (Causa)</h2>
                </div>

                <div class="space-y-4">
                    <p class="text-xs text-slate-400 font-bold uppercase px-2">O problema surgiu após:</p>
                    
                    <div onclick="setTrigger('Coloração/Tintura')" class="bg-white p-6 rounded-3xl border border-slate-100 flex items-center gap-5 cursor-pointer hover:border-amber-500 transition-all group shadow-sm">
                        <div class="p-4 bg-amber-50 text-amber-600 rounded-2xl group-hover:bg-amber-100"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m12 3-1.912 5.813a2 2 0 0 1-1.275 1.275L3 12l5.813 1.912a2 2 0 0 1 1.275 1.275L12 21l1.912-5.813a2 2 0 0 1 1.275-1.275L21 12l-5.813-1.912a2 2 0 0 1-1.275-1.275L12 3Z"/></svg></div>
                        <div class="flex-1">
                            <h4 class="font-bold text-slate-800">Coloração / Tintura</h4>
                            <p class="text-[10px] text-slate-400 uppercase font-black">Sensibilidade a corantes (PPD)</p>
                        </div>
                    </div>

                    <div onclick="setTrigger('Química Alisante (Progressiva/Botox)')" class="bg-white p-6 rounded-3xl border border-slate-100 flex items-center gap-5 cursor-pointer hover:border-amber-500 transition-all group shadow-sm">
                        <div class="p-4 bg-blue-50 text-blue-600 rounded-2xl group-hover:bg-blue-100"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 12a9 9 0 1 1-6.219-8.56"/><path d="M22 10 11 21"/><path d="m22 7-3 3"/></svg></div>
                        <div class="flex-1">
                            <h4 class="font-bold text-slate-800">Progressiva / Botox / Selagem</h4>
                            <p class="text-[10px] text-slate-400 uppercase font-black">Ácidos ou Formaldeído</p>
                        </div>
                    </div>

                    <div onclick="setTrigger('Quadro Espontâneo / Patológico')" class="bg-white p-6 rounded-3xl border border-slate-100 flex items-center gap-5 cursor-pointer hover:border-amber-500 transition-all group shadow-sm">
                        <div class="p-4 bg-emerald-50 text-emerald-600 rounded-2xl group-hover:bg-emerald-100"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 2v10"/><path d="m16 8-4 4-4-4"/><path d="M12 22v-7"/></svg></div>
                        <div class="flex-1">
                            <h4 class="font-bold text-slate-800">Causa Espontânea</h4>
                            <p class="text-[10px] text-slate-400 uppercase font-black">Dermatites, Queda ou Psoríase</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- STEP 4: Recomendação (Prescrição Digital) -->
            <div id="step-4" class="step-content space-y-6">
                <div class="flex justify-between items-center mb-4 no-print">
                    <button onclick="goToStep(1)" class="p-2 bg-white rounded-full shadow-sm"><svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M3 12a9 9 0 1 0 9-9 9.75 9.75 0 0 0-6.74 2.74L3 8"/><path d="M3 3v5h5"/></svg></button>
                    <h2 class="font-bold text-slate-800">Recomendação Digital</h2>
                    <button onclick="window.print()" class="p-2 bg-slate-900 text-white rounded-full shadow-lg"><svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M6 9V2h12v7"/><path d="M6 18H4a2 2 0 0 1-2-2v-5a2 2 0 0 1 2-2h16a2 2 0 0 1 2 2v5a2 2 0 0 1-2 2h-2"/><rect width="12" height="8" x="6" y="14"/></svg></button>
                </div>

                <div class="recommendation-paper rounded-[2.5rem] shadow-2xl border border-slate-100 overflow-hidden" id="printable-area">
                    <!-- Topo Clínico -->
                    <div class="bg-slate-900 p-10 text-white relative">
                        <div class="flex justify-between items-start mb-8">
                            <div>
                                <h3 class="serif text-3xl italic mb-1">Vanessa Braga</h3>
                                <p class="text-[10px] tracking-[0.4em] text-amber-500 uppercase font-black">Dermatologia Capilar Avançada</p>
                            </div>
                            <div class="text-right">
                                <span class="bg-amber-500 text-slate-900 px-3 py-1 rounded-full text-[9px] font-black uppercase tracking-widest">Recomendação Técnica</span>
                            </div>
                        </div>
                        <div class="grid grid-cols-2 gap-6 border-t border-white/10 pt-6">
                            <div>
                                <p class="text-[8px] uppercase font-bold text-slate-500 mb-1">Paciente</p>
                                <p id="res-name" class="text-sm font-bold"></p>
                            </div>
                            <div class="text-right">
                                <p class="text-[8px] uppercase font-bold text-slate-500 mb-1">Data / Idade</p>
                                <p id="res-meta" class="text-sm font-bold"></p>
                            </div>
                        </div>
                    </div>

                    <!-- Conteúdo Terapêutico -->
                    <div class="p-10 space-y-10">
                        <div>
                            <p class="text-[10px] font-black text-slate-400 uppercase tracking-widest mb-2">Análise de Caso e Etiologia</p>
                            <h4 id="res-trigger" class="text-xl font-bold text-slate-800"></h4>
                            <p id="res-comorb" class="text-[10px] text-red-500 font-bold uppercase mt-1"></p>
                        </div>

                        <!-- Protocolo MIP -->
                        <section>
                            <h5 class="text-[10px] font-black text-amber-600 uppercase tracking-widest mb-5 flex items-center gap-2">
                                <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m10.5 20.5 10-10a4.95 4.95 0 1 0-7-7l-10 10a4.95 4.95 0 1 0 7 7Z"/><path d="m8.5 8.5 7 7"/></svg>
                                Protocolo Farmacológico (MIP - Venda Livre)
                            </h5>
                            <div id="res-medicines" class="space-y-4">
                                <!-- JS Injection -->
                            </div>
                        </section>

                        <!-- Suplementação -->
                        <section>
                            <h5 class="text-[10px] font-black text-slate-400 uppercase tracking-widest mb-4 flex items-center gap-2">
                                <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><path d="M12 8v8"/><path d="M8 12h8"/></svg>
                                Suplementação e Nutracêuticos
                            </h5>
                            <div id="res-supplements" class="space-y-3 text-xs text-slate-600 font-medium">
                                <!-- JS Injection -->
                            </div>
                        </section>

                        <!-- Nota Acadêmica e Legal -->
                        <div class="pt-8 border-t border-dashed border-slate-200">
                            <div class="bg-slate-50 p-6 rounded-2xl border border-slate-100">
                                <h6 class="text-[9px] font-black text-slate-800 uppercase tracking-widest mb-3">Observações Acadêmico-Legais</h6>
                                <p class="text-[10px] text-slate-500 leading-relaxed italic text-justify">
                                    O presente documento consubstancia-se em uma <strong>Recomendação Terapêutica de Caráter Orientativo</strong>, não configurando, sob hipótese alguma, um ato de prescrição médica privativa. Esta orientação fundamenta-se na <strong>RDC nº 98/2016 da ANVISA</strong>, que regulamenta os Medicamentos Isentos de Prescrição (MIPs), selecionados aqui por seu alto índice de segurança farmacológica e baixa toxicidade. A abordagem visa a homeostase do ecossistema capilar e o reequilíbrio da barreira cutânea. Em caso de persistência da sintomatologia ou reações idiossincrásicas, a avaliação clínica presencial por médico dermatologista é imperativa.
                                </p>
                            </div>
                        </div>

                        <div class="text-center">
                            <p class="text-[9px] font-bold text-slate-300 uppercase tracking-[0.4em]">VB Clinic Digital Support</p>
                        </div>
                    </div>
                </div>
                
                <button onclick="location.reload()" class="w-full bg-slate-100 text-slate-500 py-4 rounded-2xl font-bold uppercase tracking-widest text-xs no-print">Novo Diagnóstico</button>
            </div>

        </main>
    </div>

    <script>
        let userData = {
            name: '',
            age: '',
            gender: '',
            comorbidities: [],
            trigger: ''
        };

        function goToStep(step) {
            if (step === 2) {
                userData.name = document.getElementById('p-name').value;
                userData.age = document.getElementById('p-age').value;
                userData.gender = document.getElementById('p-gender').value;
                if(!userData.name || !userData.age) {
                    alert('Por favor, preencha o perfil do paciente.');
                    return;
                }
            }
            if (step === 3) {
                userData.comorbidities = Array.from(document.querySelectorAll('.comorb-check:checked')).map(c => c.value);
            }
            
            document.querySelectorAll('.step-content').forEach(s => s.classList.remove('active'));
            document.getElementById(`step-${step}`).classList.add('active');
            window.scrollTo(0, 0);
        }

        function setTrigger(trigger) {
            userData.trigger = trigger;
            generateRecommendation();
            goToStep(4);
        }

        function generateRecommendation() {
            document.getElementById('res-name').innerText = userData.name;
            document.getElementById('res-meta').innerText = `${new Date().toLocaleDateString('pt-BR')} | ${userData.age} anos`;
            document.getElementById('res-trigger').innerText = `Etiologia: ${userData.trigger}`;
            
            const comorbBox = document.getElementById('res-comorb');
            if(userData.comorbidities.length > 0) {
                comorbBox.innerText = `Atenção: Paciente apresenta quadro de ${userData.comorbidities.join(', ')}`;
            } else {
                comorbBox.innerText = 'Sem comorbidades sistêmicas relatadas.';
            }

            const medContainer = document.getElementById('res-medicines');
            const supContainer = document.getElementById('res-supplements');
            medContainer.innerHTML = '';
            supContainer.innerHTML = '';

            let medicines = [];
            let supplements = [];

            // LÓGICA DE TRATAMENTO OTC (MIP)
            if (userData.trigger.includes('Coloração')) {
                // Foco em antialérgico leve e corticoide tópico de baixa potência
                medicines.push({ 
                    name: "Hidrocortisona 1% (Creme/Loção)", 
                    cat: "Corticoide Tópico de Baixa Potência", 
                    use: "Aplicar fina camada no couro cabeludo 2x ao dia, por no máximo 5 dias. Auxilia na redução do processo inflamatório local sem agressividade sistêmica." 
                });
                medicines.push({ 
                    name: "Loratadina 10mg", 
                    cat: "Anti-histamínico de 2ª Geração", 
                    use: "Tomar 1 comprimido ao dia. Indicado para o controle do prurido (coceira) e redução de edemas leves." 
                });
                supplements.push("Vitamina C (500mg): Agente antioxidante para suporte na regeneração tecidual.");
                supplements.push("Água Termal Gelada: Borrifar para alívio térmico imediato e estabilização de pH.");
            } 
            else if (userData.trigger.includes('Química')) {
                // Foco em regeneração e suavização (ácidos/queimadura leve)
                medicines.push({ 
                    name: "Dexpantenol (Solução)", 
                    cat: "Regenerador de Barreira Cutânea", 
                    use: "Aplicar no couro cabeludo 3x ao dia. Atua na síntese de coenzima A, essencial para a cicatrização e hidratação profunda." 
                });
                medicines.push({ 
                    name: "Shampoo Ultrasuave (PH 5.5)", 
                    cat: "Higiene Terapêutica", 
                    use: "Lavar delicadamente com água fria. Evitar tensoativos agressivos (Sulfatos)." 
                });
                supplements.push("Ômega 3: Auxilia no controle da resposta inflamatória sistêmica.");
                supplements.push("Aminoácidos da Queratina: Ingestão de L-Cistina para fortalecer a fibra enfraquecida.");
            }
            else {
                // Geral / Queda / Dermatite
                medicines.push({ 
                    name: "Cetoconazol 2% (Shampoo)", 
                    cat: "Antifúngico e Anti-inflamatório MIP", 
                    use: "Lavar 3x por semana, deixando agir por 5 minutos. Reduz a Malassezia e a descamação." 
                });
                supplements.push("Biotina 5mg + Zinco Quelato 29mg: Suporte metabólico para o ciclo de crescimento anágeno.");
            }

            // Regras Especiais
            if (userData.comorbidities.includes('Gestante/Lactante')) {
                medicines = [{ 
                    name: "Higiene com Shampoo Neutro e Soro Fisiológico", 
                    cat: "Protocolo de Segurança", 
                    use: "Para gestantes, recomenda-se apenas medidas paliativas. Evite corticoides ou tônicos sem anuência do obstetra." 
                }];
            }
            if (userData.comorbidities.includes('Diabetes')) {
                supplements.push("Atenção: Paciente diabético deve monitorar a microcirculação capilar e evitar qualquer atrito que gere feridas de difícil cicatrização.");
            }

            medContainer.innerHTML = medicines.map(m => `
                <div class="bg-slate-50 p-5 rounded-3xl border border-slate-100">
                    <p class="text-[9px] font-black text-amber-600 uppercase mb-1">${m.cat}</p>
                    <p class="text-sm font-bold text-slate-800">${m.name}</p>
                    <p class="text-[11px] text-slate-500 mt-2 leading-relaxed font-medium">${m.use}</p>
                </div>
            `).join('');

            supContainer.innerHTML = supplements.map(s => `
                <div class="flex gap-3 items-start">
                    <span class="text-amber-500 font-bold">•</span>
                    <span>${s}</span>
                </div>
            `).join('');
        }
    </script>
</body>
</html>
