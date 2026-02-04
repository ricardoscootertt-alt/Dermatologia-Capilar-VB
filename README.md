<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vanessa Braga - Recomendação Capilar Inteligente</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&family=Playfair+Display:ital,wght@0,700;1,700&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Inter', sans-serif; background-color: #f1f5f9; }
        .serif { font-family: 'Playfair Display', serif; }
        .step { display: none; }
        .step.active { display: block; animation: fadeIn 0.4s ease-out; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
        .premium-shadow { box-shadow: 0 25px 50px -12px rgba(15, 23, 42, 0.15); }
        .bg-vanessa { background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%); }
    </style>
</head>
<body class="text-slate-900 pb-12">

    <div id="app" class="max-w-2xl mx-auto min-h-screen">
        <!-- Header -->
        <header class="p-8 flex justify-between items-center">
            <div class="flex items-center gap-3">
                <div class="w-12 h-12 bg-slate-900 rounded-2xl flex items-center justify-center text-amber-500 shadow-lg">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10"/><circle cx="12" cy="12" r="3"/></svg>
                </div>
                <div>
                    <h1 class="serif text-xl font-bold leading-none tracking-tight">Vanessa Braga</h1>
                    <p class="text-[9px] tracking-[0.3em] text-slate-500 uppercase font-black">Saúde Capilar Avançada</p>
                </div>
            </div>
        </header>

        <main class="px-4">
            <!-- PASSO 1: Identificação -->
            <section id="step-1" class="step active space-y-6">
                <div class="bg-vanessa p-8 rounded-[2.5rem] text-white premium-shadow relative overflow-hidden">
                    <div class="relative z-10">
                        <h2 class="text-2xl font-bold mb-2">Novo Perfil</h2>
                        <p class="text-slate-400 text-sm">Inicie preenchendo os dados básicos do paciente.</p>
                    </div>
                    <svg class="absolute right-[-20px] bottom-[-20px] opacity-10 text-white" width="180" height="180" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1"><path d="M19 21v-2a4 4 0 0 0-4-4H9a4 4 0 0 0-4 4v2"/><circle cx="12" cy="7" r="4"/></svg>
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
                                </select>
                            </div>
                        </div>
                        <div>
                            <label class="text-[10px] font-black text-slate-400 uppercase ml-2 mb-2 block">Condições Pré-existentes</label>
                            <div class="grid grid-cols-2 gap-2">
                                <label class="flex items-center gap-2 p-3 bg-slate-50 rounded-xl cursor-pointer text-xs font-medium border border-transparent hover:border-slate-200">
                                    <input type="checkbox" class="comorb" value="Diabetes"> Diabetes
                                </label>
                                <label class="flex items-center gap-2 p-3 bg-slate-50 rounded-xl cursor-pointer text-xs font-medium border border-transparent hover:border-slate-200">
                                    <input type="checkbox" class="comorb" value="Pele Atópica"> Pele Sensível
                                </label>
                                <label class="flex items-center gap-2 p-3 bg-slate-50 rounded-xl cursor-pointer text-xs font-medium border border-transparent hover:border-slate-200">
                                    <input type="checkbox" class="comorb" value="Gestante/Lactante"> Gestante
                                </label>
                                <label class="flex items-center gap-2 p-3 bg-slate-50 rounded-xl cursor-pointer text-xs font-medium border border-transparent hover:border-slate-200">
                                    <input type="checkbox" class="comorb" value="Hipertensão"> Hipertensão
                                </label>
                            </div>
                        </div>
                    </div>
                    <button onclick="goToStep(2)" class="w-full bg-slate-900 text-white py-4 rounded-2xl font-bold uppercase tracking-widest text-sm shadow-xl active:scale-95 transition-all">Continuar para Causa</button>
                </div>
            </section>

            <!-- PASSO 2: Causa -->
            <section id="step-2" class="step space-y-6">
                <button onclick="goToStep(1)" class="flex items-center gap-2 text-slate-400 font-bold text-xs uppercase mb-4"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m15 18-6-6 6-6"/></svg> Voltar</button>
                <h2 class="text-2xl font-bold text-slate-800 tracking-tight">O que causou o problema?</h2>
                
                <div class="grid grid-cols-1 gap-4">
                    <div onclick="selectTrigger('Coloração')" class="bg-white p-6 rounded-3xl border border-slate-200 shadow-sm flex items-center gap-4 cursor-pointer hover:border-amber-500 transition-all group">
                        <div class="w-14 h-14 bg-amber-50 text-amber-600 rounded-2xl flex items-center justify-center group-hover:bg-amber-500 group-hover:text-white transition-colors">
                            <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="m12 3-1.912 5.813a2 2 0 0 1-1.275 1.275L3 12l5.813 1.912a2 2 0 0 1 1.275 1.275L12 21l1.912-5.813a2 2 0 0 1 1.275-1.275L21 12l-5.813-1.912a2 2 0 0 1-1.275-1.275L12 3Z"/></svg>
                        </div>
                        <div>
                            <h3 class="font-bold text-lg">Coloração / Tintura</h3>
                            <p class="text-xs text-slate-400 font-medium">Reações alérgicas a corantes e PPD</p>
                        </div>
                    </div>

                    <div onclick="selectTrigger('Química')" class="bg-white p-6 rounded-3xl border border-slate-200 shadow-sm flex items-center gap-4 cursor-pointer hover:border-amber-500 transition-all group">
                        <div class="w-14 h-14 bg-blue-50 text-blue-600 rounded-2xl flex items-center justify-center group-hover:bg-blue-500 group-hover:text-white transition-colors">
                            <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"/></svg>
                        </div>
                        <div>
                            <h3 class="font-bold text-lg">Progressiva, Selagem ou Botox</h3>
                            <p class="text-xs text-slate-400 font-medium">Sensibilidade a ácidos ou formol</p>
                        </div>
                    </div>
                </div>
            </section>

            <!-- PASSO 3: Sintomas Específicos -->
            <section id="step-3" class="step space-y-6">
                <button onclick="goToStep(2)" class="flex items-center gap-2 text-slate-400 font-bold text-xs uppercase mb-4"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m15 18-6-6 6-6"/></svg> Voltar</button>
                <div class="flex items-end justify-between">
                    <h2 class="text-2xl font-bold text-slate-800 tracking-tight">Sinais e Sintomas</h2>
                    <span id="trigger-badge" class="px-3 py-1 bg-amber-100 text-amber-700 text-[10px] font-black rounded-full uppercase mb-1"></span>
                </div>

                <div class="bg-white p-8 rounded-[2.5rem] shadow-sm border border-slate-200">
                    <p class="text-xs text-slate-400 font-bold uppercase mb-6 tracking-widest text-center">Marque o que está observando:</p>
                    <div id="symptom-container" class="space-y-3">
                        <!-- Gerado via JS -->
                    </div>
                    <button onclick="processResult()" class="w-full bg-slate-900 text-white py-4 rounded-2xl font-bold uppercase tracking-widest text-sm mt-8 shadow-xl transition-all active:scale-95">Gerar Recomendação</button>
                </div>
            </section>

            <!-- PASSO FINAL: Recomendação -->
            <section id="step-result" class="step space-y-6">
                <div class="flex justify-between items-center px-4">
                    <button onclick="location.reload()" class="p-2 bg-white rounded-full shadow-sm"><svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M3 12a9 9 0 1 0 9-9 9.75 9.75 0 0 0-6.74 2.74L3 8"/><path d="M3 3v5h5"/></svg></button>
                    <button onclick="window.print()" class="text-slate-400 flex items-center gap-2 font-bold text-xs uppercase"><svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M6 9V2h12v7"/><path d="M6 18H4a2 2 0 0 1-2-2v-5a2 2 0 0 1 2-2h16a2 2 0 0 1 2 2v5a2 2 0 0 1-2 2h-2"/><rect width="12" height="8" x="6" y="14"/></svg> Imprimir</button>
                </div>

                <div id="printable-area" class="bg-white rounded-[3rem] shadow-2xl overflow-hidden border border-slate-100">
                    <!-- Header Recomendação -->
                    <div class="bg-vanessa p-10 text-white text-center relative">
                        <div class="absolute inset-0 flex items-center justify-center opacity-5 pointer-events-none">
                            <span class="text-[120px] font-black">VB</span>
                        </div>
                        <h2 class="serif text-3xl font-bold mb-1 italic">Vanessa Braga</h2>
                        <p class="text-[9px] tracking-[0.4em] text-amber-500 uppercase font-black">Hair Health & Wellness</p>
                        <div class="mt-8 pt-6 border-t border-white/10 flex justify-between text-left">
                            <div>
                                <p class="text-[8px] uppercase font-bold text-slate-400">Paciente</p>
                                <p id="res-name" class="font-bold text-sm"></p>
                            </div>
                            <div class="text-right">
                                <p class="text-[8px] uppercase font-bold text-slate-400">Data do Guia</p>
                                <p id="res-date" class="font-bold text-sm"></p>
                            </div>
                        </div>
                    </div>

                    <!-- Conteúdo Clínico -->
                    <div class="p-10 space-y-10">
                        <div class="flex flex-wrap gap-2" id="res-tags">
                            <!-- Tags Automáticas -->
                        </div>

                        <!-- O que usar -->
                        <section>
                            <h3 class="text-[10px] font-black text-amber-600 uppercase tracking-[0.2em] mb-4 flex items-center gap-2">
                                <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M11 15h2m-1-5v3M12 21a9 9 0 1 0 0-18 9 9 0 0 0 0 18Z"/></svg>
                                Itens de Cuidado Home-Care (Venda Livre)
                            </h3>
                            <div id="med-list" class="space-y-4">
                                <!-- JS -->
                            </div>
                        </section>

                        <!-- Suplementos -->
                        <section class="bg-slate-50 p-6 rounded-3xl border border-slate-100">
                            <h3 class="text-[10px] font-black text-slate-400 uppercase tracking-[0.2em] mb-3">Sugestão de Suplementação</h3>
                            <ul id="sup-list" class="space-y-2 text-xs font-medium text-slate-600">
                                <!-- JS -->
                            </ul>
                        </section>

                        <!-- Jurídico / Disclaimer -->
                        <div class="pt-8 border-t border-dashed border-slate-200">
                            <div class="bg-slate-100 p-4 rounded-xl text-[10px] text-slate-500 leading-relaxed text-justify">
                                <p class="mb-2 uppercase font-black text-slate-400">Aviso Legal e Fundamentação:</p>
                                <strong>ESTE DOCUMENTO NÃO É UMA PRESCRIÇÃO MÉDICA.</strong> Trata-se de uma Recomendação de Cuidados Domiciliares (Home-Care) focada em Medicamentos Isentos de Prescrição (MIPs) e suplementos alimentares. 
                                <br><br>
                                Fundamentação: Resolução <strong>RDC ANVISA nº 98/2016</strong>, que dispõe sobre os critérios para enquadramento de medicamentos como isentos de prescrição, e a <strong>Lei nº 5.991/1973</strong> que disciplina o comércio de drogas e medicamentos. Em caso de agravamento dos sintomas, procure auxílio médico especializado ou pronto-socorro.
                            </div>
                        </div>

                        <div class="text-center pt-4">
                            <p class="text-[8px] font-black text-slate-300 uppercase tracking-widest">Protocolo Digital validado - Espaço Vanessa Braga</p>
                        </div>
                    </div>
                </div>
            </section>
        </main>
    </div>

    <script>
        const state = {
            patient: { name: '', age: '', gender: '', comorbidities: [] },
            trigger: '',
            symptoms: []
        };

        const SYMPTOMS_DATA = {
            'Coloração': [
                { id: 'edema', label: 'Inchaço (Edema) no rosto ou pálpebras' },
                { id: 'prurido', label: 'Coceira intensa e persistente' },
                { id: 'eritema', label: 'Vermelhidão (Couro "pegando fogo")' },
                { id: 'vesiculas', label: 'Pequenas bolhas ou secreção' }
            ],
            'Química': [
                { id: 'queimadura', label: 'Ardor ou sensação de queimadura' },
                { id: 'feridas', label: 'Feridas vivas ou crostas' },
                { id: 'descamacao', label: 'Descamação excessiva (Pele soltando)' },
                { id: 'alopecia', label: 'Queda de fios na hora ou quebra' }
            ]
        };

        function goToStep(s) {
            document.querySelectorAll('.step').forEach(el => el.classList.remove('active'));
            document.getElementById(`step-${s === 'result' ? 'result' : s}`).classList.add('active');
            window.scrollTo(0,0);
        }

        function selectTrigger(t) {
            state.trigger = t;
            const container = document.getElementById('symptom-container');
            const badge = document.getElementById('trigger-badge');
            badge.innerText = t;
            
            container.innerHTML = SYMPTOMS_DATA[t].map(s => `
                <label class="flex items-center gap-4 p-5 border rounded-2xl cursor-pointer hover:bg-slate-50 transition-all">
                    <input type="checkbox" class="symp-check w-5 h-5 accent-slate-900" value="${s.id}">
                    <span class="font-medium text-slate-700 text-sm">${s.label}</span>
                </label>
            `).join('');
            
            goToStep(3);
        }

        function processResult() {
            // Coletar Dados do Passo 1
            state.patient.name = document.getElementById('p-name').value || 'Paciente Visitante';
            state.patient.age = document.getElementById('p-age').value;
            state.patient.gender = document.getElementById('p-gender').value;
            state.patient.comorbidities = Array.from(document.querySelectorAll('.comorb:checked')).map(c => c.value);
            state.symptoms = Array.from(document.querySelectorAll('.symp-check:checked')).map(c => c.value);

            // Renderizar na Prescrição
            document.getElementById('res-name').innerText = state.patient.name;
            document.getElementById('res-date').innerText = new Date().toLocaleDateString('pt-br');
            
            const tags = document.getElementById('res-tags');
            tags.innerHTML = `
                <span class="px-2 py-1 bg-slate-900 text-white text-[8px] font-black rounded uppercase">${state.trigger}</span>
                <span class="px-2 py-1 bg-slate-100 text-slate-500 text-[8px] font-black rounded uppercase">${state.patient.age} Anos</span>
                ${state.patient.comorbidities.map(c => `<span class="px-2 py-1 bg-red-100 text-red-600 text-[8px] font-black rounded uppercase">${c}</span>`).join('')}
            `;

            const medList = document.getElementById('med-list');
            const supList = document.getElementById('sup-list');
            let meds = [];
            let sups = [];

            // Lógica de Recomendação (Foco em MIPs e Corticoides Leves)
            if (state.trigger === 'Coloração') {
                meds.push({ name: "Hidrocortisona 1% (Creme/Loção)", type: "Corticoide Tópico Leve", usage: "Aplicar nas áreas de coceira e vermelhidão 2x ao dia por até 5 dias. Corticoide suave para evitar efeitos sistêmicos." });
                meds.push({ name: "Loratadina 10mg", type: "Anti-histamínico (Venda Livre)", usage: "1 comprimido ao dia para controle do inchaço e prurido." });
                meds.push({ name: "Compressas de Soro Fisiológico Gelado", type: "Cuidado Local", usage: "Fazer compressas nas áreas com calor local por 15 minutos." });
                sups.push("Vitamina C 500mg: Auxilia na resposta antioxidante da pele.");
            } else {
                meds.push({ name: "Água Termal (La Roche ou Avène)", type: "Dermocosmético", usage: "Borrife várias vezes ao dia. Ajuda a restaurar o pH e acalmar o ardor." });
                meds.push({ name: "Bepantol Derma Solução", type: "Regenerador de Barreira", usage: "Aplicar no couro cabeludo limpo para acelerar a cicatrização das feridas e crostas." });
                meds.push({ name: "Shampoo sem Sulfatos (Infantil ou Pós-Química)", type: "Limpeza Suave", usage: "Lavar delicadamente apenas para remover sujidade sem agredir a pele exposta." });
                sups.push("Zinco Quelato 29mg: Mineral vital para cicatrização e saúde do folículo.");
            }

            // Suplementos base
            sups.push("Biotina 5mg: Vitamina que auxilia na reconstrução da fibra capilar danificada.");

            // Ajuste por Comorbidade (Segurança)
            if (state.patient.comorbidities.includes('Diabetes')) {
                meds.push({ name: "Aviso de Cicatrização", type: "Monitoramento", usage: "Devido à condição de Diabetes, evite remover crostas manualmente para prevenir infecções." });
            }

            medList.innerHTML = meds.map(m => `
                <div class="flex gap-4 p-4 bg-slate-50 rounded-2xl border border-slate-100">
                    <div class="mt-1"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="#d97706" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><path d="m9 12 2 2 4-4"/></svg></div>
                    <div>
                        <p class="text-[9px] font-black text-amber-600 uppercase mb-0.5">${m.type}</p>
                        <p class="text-sm font-bold text-slate-800 leading-none">${m.name}</p>
                        <p class="text-[11px] text-slate-500 mt-2 italic leading-relaxed">${m.usage}</p>
                    </div>
                </div>
            `).join('');

            supList.innerHTML = sups.map(s => `<li>• ${s}</li>`).join('');

            goToStep('result');
        }
    </script>
</body>
</html>

