# 🚀 Desafio Técnico – Analista de BI (Allu)

Fala aí! 👋  
Esse repositório é onde deixei toda a solução do **Desafio Técnico de BI (Risco e Inadimplência)** da **Allu**.  
Aqui tem SQL, DAX, modelagem, dashboard em Power BI e estrutura PBIX + PBIP organizada do jeito certo pra BI profissional.

---

## 📦 Estrutura do Projeto

📦 allu-desafio-bi
│
├── 📂 pbip/                      → Projeto Power BI em formato PBIP (versionável)
│   ├── semanticModel/
│   ├── report/
│   └── model.bim
│
├── 📄 Allu_Desafio_BI.pbix       → Arquivo completo para abrir direto no Power BI
│
├── 📂 sql/
│   ├── modelagem_inadimplencia.sql
│   └── exploracao.sql
│
├── 📂 images/
│   └── dashboard_preview.png
│
└── README.md


### 🟨 Por que PBIX *e* PBIP?

- **PBIX** → abrir rápido, ver o dashboard funcionando em 2 cliques.  
- **PBIP** → versionar DAX, modelo e layout de forma limpa no Git (sem arquivo gigante).  

A ideia foi unir o melhor dos dois mundos:  
👉 fácil de visualizar **e** pronto pra ser mantido como projeto de BI de verdade.

---

## 📊 Dashboard Online

👉 **Link do relatório no Power BI:**  
https://app.powerbi.com/view?r=eyJrIjoiOTUzNzNjYjctYjNlMy00YzM5LThlMDgtNjI5NGM3ZTliOTIwIiwidCI6IjVlYzZhYTJhLWVmYzctNGIyNS1iZTIxLTNhYzhmZmM2MzAxYyJ9&navContentPaneEnabled=false&actionBarEnabled=false

_(Substitua pelo link público publicado.)_

---

## 🧠 Como montei a solução

### 1️⃣ Exploração do dataset

Cada linha = uma parcela do cliente.  
Validei campos chave:

- idade  
- estado  
- valor_parcela  
- parcela_recorrencia  
- status_pagamento  
- datas de vencimento x pagamento  

E tratei as regras de negócio:

- `future` não entra no denominador  
- `refunded` = considerado pago  
- `failed` e `chargedback` = inadimplência real  
- agrupamento por mês/ano de vencimento  

---

### 2️⃣ Modelagem Analítica (SQL + DAX)

Usei SQL para exploração e DAX para consolidar a camada semântica.

Principais entregas:

- **Taxa de inadimplência mensal**  
- **Perfil do inadimplente por idade, estado e recorrência**  
- **Distribuição por valor da parcela** (faixas/bins)  
- **Comportamento por ciclo (parcela_recorrencia)**  
- **Colunas auxiliares:** faixa etária, bins de valores, ordenações personalizadas  

Toda a lógica está separada dentro do projeto PBIP para facilitar revisão e versionamento.

---

### 3️⃣ Construção do Dashboard (Power BI)

Dashboard focado em clareza e tomada de decisão:

- 📈 Evolução da inadimplência mês a mês  
- 🗺️ Mapa por Estado com % de risco  
- 👥 Faixa Etária x Inadimplência  
- 🔁 Comportamento por Número da Parcela  
- 💸 Distribuição por Valor da Parcela (histograma)  

Usei dark mode e ênfase nos KPIs principais.

---

## 🔍 Insights Principais

- A inadimplência cresce entre os meses analisados → possível sazonalidade financeira.  
- Faixas etárias extremas (`<25` e `>60`) concentram os maiores riscos.  
- O risco aumenta até a 7ª parcela, sugerindo perda de capacidade ao longo do ciclo.  
- Valor da parcela sozinho **não** determina inadimplência.  
- Estados apresentam comportamentos diferentes → influência regional importante.

---

## 🛠️ Stack Utilizada

- **Power BI** (PBIX + PBIP)  
- **DAX** (medidas, classificações e cálculos de risco)  
- **SQL** (exploração e modelagem inicial)  
- **Git/GitHub** (versionamento completo)  

---

## 👨‍💻 Sobre mim

Sou o **Gustavo**, Especialista/Engenheiro de Dados.  
Curto:

- arquitetura simples e eficiente  
- dashboards que contam a história certa  
- automações que evitam retrabalho  
- usar BI + engenharia para transformar dados em decisões  

Conecta comigo:

<a href="https://www.linkedin.com/in/gustavoalexandermiranda" target="_blank">
  <img src="https://img.shields.io/badge/LinkedIn-Gustavo-blue?style=flat&logo=linkedin">
</a>
