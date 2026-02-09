<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vanessa Braga - Dermatologia Capilar Avançada</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&family=Playfair+Display:ital,wght@0,700;1,700&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Inter', sans-serif; background-color: #f8fafc; }
        .serif { font-family: 'Playfair Display', serif; }
        .step { display: none; }
        .step.active { display: block; animation: fadeIn 0.5s ease-out; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
        .glass { background: rgba(255, 255, 255, 0.8); backdrop-filter: blur(12px); border: 1px solid rgba(255, 255, 255, 0.3); }
        .gradient-bg { background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%); }
    </style>
</head>
<body class="text-slate-900 pb-12">

    <div id="app" class="max-w-2xl mx-auto min-h-screen p-4 md:p-8">
        <!-- Header Branding -->
        <header class="flex justify-between items-center mb-8">
            <div class="flex items-center gap-3">
                <div class="w-12 h-12 bg-slate-900 rounded-2xl flex items-center justify-center text-amber-500 shadow-xl border border-slate-700">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10"/><circle cx="12" cy="12" r="3"/></svg>
                </div>
                <div>
                    <h1 class="serif text-xl font-bold leading-none tracking-tight">Vanessa Braga</h1>
                    <p class="text-[9px] tracking-[0.3em] text-slate-500 uppercase font-black">Dermatologia Capilar</p>
                </div>
            </div>
            <div class="hidden md:block text-right">
                <p class="text-[10px] font-bold text-slate-400 uppercase tracking-widest">Portal de Triagem v2.0</p>
            </div>
        </header>

        <!-- STEP 1: Identificação do Paciente -->
        <section id="step-1" class="step active space-y-6">
            <div class="gradient-bg p-8 rounded-[2.5rem] text-white shadow-2xl relative overflow-hidden">
                <h2 class="text-2xl font-bold mb-2">Identificação</h2>
                <p class="text-slate-400 text-sm">Dados básicos para personalização do atendimento.</p>
                <div class="absolute right-[-20px] bottom-[-20px] opacity-10">
                    <svg width="180" height="180" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1"><path d="M19 21v-2a4 4 0 0 0-4-4H9a4 4 0 0 0-4 4v2"/><circle cx="12" cy="7" r="4"/></svg>
                </div>
            </div>

            <div class="bg-white p-8 rounded-[2rem] shadow-sm space-y-5 border border-slate-200">
                <div class="space-y-4">
                    <div>
                        <label class="text-[10px] font-black text-slate-400 uppercase ml-2 mb-1 block">Nome Completo</label>
                        <input type="text" id="p-name" placeholder="Nome do paciente" class="w-full p-4 bg-slate-50 border-none rounded-2xl focus:ring-2 focus:ring-amber-500 outline-none transition-all">
                    </div>
                    <div class="grid grid-cols-2 gap-4">
                        <div>
                            <label class="text-[10px] font-black text-slate-400 uppercase ml-2 mb-1 block">Idade</label>
                            <input type="number" id="p-age" placeholder="Ex: 28" class="w-full p-4 bg-slate-50 border-none rounded-2xl focus:ring-2 focus:ring-amber-500 outline-none">
                        </div>
                        <div>
                            <label class="text-[10px] font-black text-slate-400 uppercase ml-2 mb-1 block">Gênero</label>
                            <select id="p-gender" class="w-full p-4 bg-slate-50 border-none rounded-2xl focus:ring-2 focus:ring-amber-500 outline-none">
                                <option value="Feminino">Feminino</option>
                                <option value="Masculino">Masculino</option>
                                <option value="Outro">Outro</option>
                            </select>
                        </div>
                    </div>
                    <div>
                        <label class="text-[10px] font-black text-slate-400 uppercase ml-2 mb-2 block">Condições de Saúde</label>
                        <div class="grid grid-cols-2 gap-2">
                            <label class="flex items-center gap-2 p-3 bg-slate-50 rounded-xl cursor-pointer text-xs font-medium border border-transparent hover:border-slate-200">
                                <input type="checkbox" class="comorb" value="Diabetes"> Diabetes
                            </label>
                            <label class="flex items-center gap-2 p-3 bg-slate-50 rounded-xl cursor-pointer text-xs font-medium border border-transparent hover:border-slate-200">
                                <input type="checkbox" class="comorb" value="Hipertensão"> Hipertensão
                            </label>
                            <label class="flex items-center gap-2 p-3 bg-slate-50 rounded-xl cursor-pointer text-xs font-medium border border-transparent hover:border-slate-200">
                                <input type="checkbox" class="comorb" value="Sensibilidade"> Pele Sensível
                            </label>
                            <label class="flex items-center gap-2 p-3 bg-slate-50 rounded-xl cursor-pointer text-xs font-medium border border-transparent hover:border-slate-200">
                                <input type="checkbox" class="comorb" value="Alergia"> Alergia a Medicamentos
                            </label>
                        </div>
                    </div>
                </div>
                <button onclick="goToStep(2)" class="w-full bg-slate-900 text-white py-4 rounded-2xl font-bold uppercase tracking-widest text-sm shadow-xl active:scale-95 transition-all">Próximo: Causa do Problema</button>
            </div>
        </section>

        <!-- STEP 2: Causa Principal -->
        <section id="step-2" class="step space-y-6">
            <div class="flex items-center gap-3 mb-4">
                <button onclick="goToStep(1)" class="p-2 bg-white rounded-full shadow-sm"><svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m15 18-6-6 6-6"/></svg></button>
                <h2 class="text-xl font-bold text-slate-800">O que causou o desconforto?</h2>
            </div>

            <div class="grid grid-cols-1 gap-4">
                <div onclick="selectTrigger('Coloração')" class="bg-white p-6 rounded-3xl border border-slate-200 shadow-sm flex items-center gap-4 cursor-pointer hover:border-amber-500 hover:shadow-lg transition-all group">
                    <div class="w-14 h-14 bg-amber-50 text-amber-600 rounded-2xl flex items-center justify-center group-hover:bg-amber-500 group-hover:text-white transition-colors">
                        <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 2.69l5.66 5.66a8 8 0 1 1-11.31 0z"/></svg>
                    </div>
                    <div>
                        <h3 class="font-bold text-lg leading-tight">Coloração / Tintura</h3>
                        <p class="text-xs text-slate-400">Reação a pigmentos ou amônia.</p>
                    </div>
                </div>

                <div onclick="selectTrigger('Química')" class="bg-white p-6 rounded-3xl border border-slate-200 shadow-sm flex items-center gap-4 cursor-pointer hover:border-amber-500 hover:shadow-lg transition-all group">
                    <div class="w-14 h-14 bg-blue-50 text-blue-600 rounded-2xl flex items-center justify-center group-hover:bg-blue-500 group-hover:text-white transition-colors">
                        <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"/></svg>
                    </div>
                    <div>
                        <h3 class="font-bold text-lg leading-tight">Progressiva, Selagem ou Botox</h3>
                        <p class="text-xs text-slate-400">Alisamentos químicos e ácidos.</p>
                    </div>
                </div>

                <div onclick="selectTrigger('Pos-Cancer')" class="bg-white p-6 rounded-3xl border border-slate-200 shadow-sm flex items-center gap-4 cursor-pointer hover:border-pink-500 hover:shadow-lg transition-all group">
                    <div class="w-14 h-14 bg-pink-50 text-pink-600 rounded-2xl flex items-center justify-center group-hover:bg-pink-500 group-hover:text-white transition-colors">
                        <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M19 14c1.49-1.46 3-3.21 3-5.5A5.5 5.5 0 0 0 16.5 3c-1.76 0-3 .5-4.5 2-1.5-1.5-2.74-2-4.5-2A5.5 5.5 0 0 0 2 8.5c0 2.3 1.5 4.05 3 5.5l7 7Z"/></svg>
                    </div>
                    <div>
                        <h3 class="font-bold text-lg leading-tight">Pós-Quimioterapia / Câncer</h3>
                        <p class="text-xs text-slate-400">Queda, quebra e sensibilidade extrema.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- STEP 3: Sintomas Dinâmicos -->
        <section id="step-3" class="step space-y-6">
            <div class="flex items-center justify-between mb-4">
                <button onclick="goToStep(2)" class="p-2 bg-white rounded-full shadow-sm"><svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m15 18-6-6 6-6"/></svg></button>
                <div id="trigger-badge" class="px-4 py-1.5 bg-slate-900 text-white text-[10px] font-black rounded-full uppercase tracking-widest"></div>
            </div>

            <div class="bg-white p-8 rounded-[2.5rem] shadow-sm border border-slate-200">
                <h3 class="text-lg font-bold text-slate-800 mb-6 text-center">Selecione os sintomas presentes:</h3>
                <div id="symptom-container" class="space-y-3">
                    <!-- JS INJECTION -->
                </div>
                <button onclick="generateRecommendation()" class="w-full bg-slate-900 text-white py-4 rounded-2xl font-bold uppercase tracking-widest text-sm mt-8 shadow-xl transition-all active:scale-95">Gerar Recomendação de Cuidados</button>
            </div>
        </section>

        <!-- STEP FINAL: Recomendação -->
        <section id="step-result" class="step space-y-6">
            <div class="flex justify-between items-center px-2">
                <button onclick="location.reload()" class="p-2 bg-white rounded-full shadow-sm"><svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M3 12a9 9 0 1 0 9-9 9.75 9.75 0 0 0-6.74 2.74L3 8"/><path d="M3 3v5h5"/></svg></button>
                <button onclick="window.print()" class="bg-slate-900 text-white px-5 py-2 rounded-full text-xs font-bold uppercase flex items-center gap-2"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M6 9V2h12v7"/><path d="M6 18H4a2 2 0 0 1-2-2v-5a2 2 0 0 1 2-2h16a2 2 0 0 1 2 2v5a2 2 0 0 1-2 2h-2"/><rect width="12" height="8" x="6" y="14"/></svg> Imprimir Guia</button>
            </div>

            <div id="print-area" class="bg-white rounded-[3rem] shadow-2xl overflow-hidden border border-slate-100">
                <!-- Cabeçalho Clínico -->
                <div class="gradient-bg p-10 text-white text-center relative">
                    <h2 class="serif text-3xl font-bold italic mb-1">Vanessa Braga</h2>
                    <p class="text-[9px] tracking-[0.4em] text-amber-500 uppercase font-black">Dermatologia Capilar Avançada</p>
                    
                    <div class="mt-8 pt-6 border-t border-white/10 flex justify-between text-left">
                        <div class="space-y-1">
                            <p class="text-[8px] uppercase font-bold text-slate-400">Paciente</p>
                            <p id="res-name" class="font-bold text-sm"></p>
                        </div>
                        <div class="text-right space-y-1">
                            <p class="text-[8px] uppercase font-bold text-slate-400">Data de Emissão</p>
                            <p id="res-date" class="font-bold text-sm"></p>
                        </div>
                    </div>
                </div>

                <!-- Corpo da Recomendação -->
                <div class="p-10 space-y-8">
                    <div id="res-tags" class="flex flex-wrap gap-2"></div>

                    <!-- Seção Medicamentos OTC -->
                    <section>
                        <h3 class="text-[10px] font-black text-amber-600 uppercase tracking-widest mb-4 flex items-center gap-2">
                            <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="m10.5 20.5 10-10a4.95 4.95 0 1 0-7-7l-10 10a4.95 4.95 0 1 0 7 7Z"/><path d="m8.5 8.5 7 7"/></svg>
                            Recomendação de Cuidados e OTC (Venda Livre)
                        </h3>
                        <div id="med-list" class="space-y-4"></div>
                    </section>

                    <!-- Seção Suplementação -->
                    <section class="bg-slate-50 p-6 rounded-3xl border border-slate-100">
                        <h3 class="text-[10px] font-black text-slate-400 uppercase tracking-widest mb-3">Suplementação Auxiliar</h3>
                        <ul id="sup-list" class="space-y-2 text-xs font-medium text-slate-600"></ul>
                    </section>

                    <!-- Disclaimer Legal -->
                    <div class="pt-8 border-t border-dashed border-slate-200">
                        <div class="bg-amber-50 p-5 rounded-2xl text-[10px] text-amber-900 leading-relaxed border border-amber-100">
                            <p class="mb-2 font-black uppercase underline">Aviso de Isenção e Fundamentação Legal:</p>
                            <strong>ESTE DOCUMENTO NÃO É UMA PRESCRIÇÃO MÉDICA.</strong> Trata-se de uma Orientação de Cuidados Domiciliares (Home-Care) baseada em Medicamentos Isentos de Prescrição (MIPs) e Suplementos Alimentares. 
                            <br><br>
                            <strong>Fundamentação:</strong> Conforme a Resolução <strong>RDC ANVISA nº 98/2016</strong>, que estabelece os critérios para enquadramento de medicamentos isentos de prescrição, e a <strong>Lei Federal nº 5.991/1973</strong>. Os ativos aqui sugeridos (como Hidrocortisona 1%) são de baixa potência e seguros para venda livre. Em caso de persistência, procure um médico.
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <script>
        const state = {
            name: '', age: '', gender: '', comorbidities: [], trigger: '', symptoms: []
        };

        const SYMPTOMS_MAP = {
            'Coloração': [
                { id: 'edema', label: 'Inchaço facial ou nas pálpebras' },
                { id: 'coceira', label: 'Coceira intensa imediata' },
                { id: 'vermelhidão', label: 'Vermelhidão (Couro cabeludo "em brasa")' },
                { id: 'secreção', label: 'Pequenas bolhas ou saída de líquido' }
            ],
            'Química': [
                { id: 'ardor', label: 'Ardor ou queimação durante a lavagem' },
                { id: 'descamação', label: 'Descamação em placas (Parece caspa grossa)' },
                { id: 'sensibilidade', label: 'Dor ao pentear ou tocar o couro' },
                { id: 'quebra', label: 'Fios "elásticos" ou quebra imediata' }
            ],
            'Pos-Cancer': [
                { id: 'fragilidade', label: 'Fios extremamente finos e transparentes' },
                { id: 'falhas', label: 'Crescimento irregular (Clareiras)' },
                { id: 'ressecamento', label: 'Ressecamento extremo da haste' },
                { id: 'inflamação', label: 'Couro cabeludo sensível pós-radiação/quimio' }
            ]
        };

        function goToStep(s) {
            document.querySelectorAll('.step').forEach(el => el.classList.remove('active'));
            document.getElementById(`step-${s}`).classList.add('active');
            window.scrollTo(0,0);
        }

        function selectTrigger(t) {
            state.trigger = t;
            document.getElementById('trigger-badge').innerText = t;
            const container = document.getElementById('symptom-container');
            container.innerHTML = SYMPTOMS_MAP[t].map(s => `
                <label class="flex items-center gap-4 p-5 border rounded-2xl cursor-pointer hover:bg-slate-50 transition-all">
                    <input type="checkbox" class="symp-check w-5 h-5 accent-slate-900" value="${s.id}">
                    <span class="font-medium text-slate-700 text-sm">${s.label}</span>
                </label>
            `).join('');
            goToStep(3);
        }

        function generateRecommendation() {
            state.name = document.getElementById('p-name').value || 'Paciente Anônimo';
            state.age = document.getElementById('p-age').value || '--';
            state.gender = document.getElementById('p-gender').value;
            state.comorbidities = Array.from(document.querySelectorAll('.comorb:checked')).map(c => c.value);
            state.symptoms = Array.from(document.querySelectorAll('.symp-check:checked')).map(c => c.value);

            // Injetar Textos
            document.getElementById('res-name').innerText = state.name;
            document.getElementById('res-date').innerText = new Date().toLocaleDateString('pt-br');
            
            // Tags
            const tagContainer = document.getElementById('res-tags');
            tagContainer.innerHTML = `
                <span class="px-3 py-1 bg-slate-900 text-white text-[9px] font-black rounded-lg uppercase tracking-widest">${state.trigger}</span>
                <span class="px-3 py-1 bg-slate-100 text-slate-500 text-[9px] font-black rounded-lg uppercase">${state.age} Anos</span>
                <span class="px-3 py-1 bg-slate-100 text-slate-500 text-[9px] font-black rounded-lg uppercase">${state.gender}</span>
                ${state.comorbidities.map(c => `<span class="px-3 py-1 bg-red-100 text-red-600 text-[9px] font-black rounded-lg uppercase">${c}</span>`).join('')}
            `;

            const medList = document.getElementById('med-list');
            const supList = document.getElementById('sup-list');
            let meds = [];
            let sups = [];

            // LÓGICA DE RECOMENDAÇÃO BASEADA NO GATILHO
            if (state.trigger === 'Coloração') {
                meds.push({ name: "Hidrocortisona 1% (Creme/Loção)", info: "Corticoide de Baixa Potência (OTC)", usage: "Aplicar fina camada no couro 2x ao dia por até 5 dias. Não causa efeito rebote se usado conforme indicado." });
                meds.push({ name: "Loratadina 10mg", info: "Antihistamínico de Venda Livre", usage: "1 comprimido ao dia para redução de edema e prurido." });
                sups.push("Vitamina C 500mg: Potencializa a recuperação da barreira cutânea.");
            } else if (state.trigger === 'Química') {
                meds.push({ name: "Água Termal (Borrificar Gelada)", info: "Cuidado Calmante", usage: "Borrifar no couro a cada 3h para resfriamento e alívio do ardor." });
                meds.push({ name: "Dexpantenol (Bepantol Derma)", info: "Regenerador Epitelial", usage: "Aplicar no couro limpo para auxiliar na cicatrização das placas." });
                sups.push("Zinco Quelato 29mg: Essencial para a reparação de tecidos agredidos.");
            } else if (state.trigger === 'Pos-Cancer') {
                meds.push({ name: "Óleo de Rosa Mosqueta Puro", info: "Nutrição Celular", usage: "Massagear levemente o couro 1x ao dia para melhorar a elasticidade." });
                meds.push({ name: "Shampoo de pH Fisiológico (Infantil)", info: "Limpeza Ultra Suave", usage: "Lavar delicadamente para não remover a proteção natural fragilizada." });
                sups.push("Biotina 5mg: Estímulo para a síntese de queratina no fio nascente.");
                sups.push("Pantotenato de Cálcio (Vit B5): Melhora a resistência à quebra.");
            }

            // Suplementos Padrão
            sups.push("L-Cistina: Aminoácido fundamental para a estrutura capilar.");

            medList.innerHTML = meds.map(m => `
                <div class="flex gap-4 p-5 bg-white border border-slate-100 rounded-3xl shadow-sm">
                    <div class="w-2 h-2 bg-amber-500 rounded-full mt-2 shrink-0"></div>
                    <div>
                        <p class="text-[9px] font-black text-amber-600 uppercase mb-0.5">${m.info}</p>
                        <p class="text-sm font-bold text-slate-800">${m.name}</p>
                        <p class="text-[11px] text-slate-500 mt-2 italic leading-relaxed font-medium">${m.usage}</p>
                    </div>
                </div>
            `).join('');

            supList.innerHTML = sups.map(s => `<li class="flex items-center gap-2"><div class="w-1 h-1 bg-slate-300 rounded-full"></div> ${s}</li>`).join('');

            goToStep('result');
        }
    </script>
</body>
</html>

