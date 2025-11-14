🚀 Desafio Técnico – Analista de BI (Allu)

Fala aí! Esse repositório é onde deixei toda a solução do Desafio Técnico de BI (Risco e Inadimplência) da Allu.
Aqui tem SQL, DAX, modelagem, dashboard, estrutura PBIP + PBIX, e tudo que realmente importa quando o assunto é análise de risco e comportamento de pagamento.

Eu quis montar de um jeito profissional, bem organizado, mas também com aquela pegada prática de quem realmente bota a mão na massa.

📦 Como organizei esse projeto

Nada de caos — deixei tudo organizado pra quem quiser abrir, revisar ou até rodar a solução por completo.

📦 allu-desafio-bi
│
├── 📂 pbip/                      → Projeto Power BI em formato PBIP (versionável)
│   ├── semanticModel/
│   ├── report/
│   └── model.bim
│
├── 📄 Allu_Desafio_BI.pbix       → Arquivo completo, fácil de abrir direto no Power BI
│
├── 📂 sql/
│   ├── modelagem_inadimplencia.sql
│   └── exploracao.sql
│
├── 📂 images/
│   └── dashboard_preview.png
│
└── README.md

🟨 Por que PBIP e PBIX?

Porque eu não brinco quando o assunto é versionamento e boas práticas:

PBIX → Pra abrir rápido e ver o dashboard funcionando

PBIP → Pra versionar igual gente grande (Git), ver diffs de DAX, revisar modelo e permitir colaboração futura

Se quiserem auditar, evoluir ou integrar com pipeline de BI, o PBIP já deixa o caminho pronto.

📊 Dashboard Online (Power BI)

👉 Acesse o relatório publicado aqui:
🔗 https://app.powerbi.com/…
 (coloque seu link aqui)

🧠 Como montei a solução (por partes)
1. Exploração e leitura do dataset

Dei aquela geral esperta no dataset:

Entendi cada status (paid, refunded, future, etc.)

Validei granularidade (1 linha = 1 parcela)

Identifiquei campos chave (idade, UF, recorrência)

Fiz checagens de nulos e coerência de datas

2. Construção da camada analítica (DAX + SQL)

Montei:

Taxa de inadimplência correta

Perfil do inadimplente por idade, estado e recorrência

Distribuição de valor da parcela

Classificações de faixa etária e bins de valor

Ordenações personalizadas (importantíssimo pra gráficos)

Métricas para todos os visuais do dashboard

Tudo dentro do PBIP pra ficar limpo, modular e versionado.

📈 O Dashboard (Power BI)

Montei um dashboard no estilo:

Clean

Direto

Pronto para tomada de decisão

Visuais entregues:

📉 Evolução da inadimplência mensal

🗺️ Mapa por Estado com % de risco

👥 Faixa Etária vs. Inadimplência

🔁 Comportamento ao longo da recorrência

💸 Distribuição de valor da parcela (histograma)

Cada visual amarra uma parte da história do comportamento do cliente.

🔍 Insights que tirei da base

A inadimplência cresce entre junho e julho (podendo indicar sazonalidade financeira).

Faixas extremas (<25 e >60) concentram o maior risco.

O risco aumenta principalmente até a 7ª parcela.

Ticket alto não necessariamente indica maior inadimplência.

Estados apresentam diferenças relevantes — comportamento regional importa.

Tudo escrito na Parte 3 do desafio, em PDF dentro da pasta insights (se você quiser que eu gere esse PDF aqui também, só falar!).

🛠️ Ferramentas que usei

Power BI (PBIX + PBIP)

DAX pra fazer a mágica

SQL pra análise exploratória

Git/GitHub pra versionar tudo

VS Code pra revisar estrutura PBIP

👨‍💻 Quem montou?

Gustavo Alexander Miranda
Especialista em Dados • Engenheiro de Dados • Analista de BI

Apaixonado por modelagem, risco, automação, pipelines e tudo que envolve transformar caos em informação útil.

<a href="https://www.linkedin.com/in/gustavoalexandermiranda" target="_blank"> <img src="https://img.shields.io/badge/LinkedIn-Gustavo-blue?style=flat&logo=linkedin"> </a>
