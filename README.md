# Portfólio · Projetos do Curso de Ciência de Dados (EBAC)

Este repositório reúne **projetos independentes** desenvolvidos ao longo do curso de **Ciência de Dados** da **EBAC**.  
Cada pasta corresponde a um **módulo/atividade**, com seu próprio objetivo, dados e entregáveis. A ideia é mostrar, de forma organizada, a evolução de habilidades como **limpeza e preparação de dados**, **análise exploratória (EDA)**, **visualização** e **raciocínio analítico**.

> **Como navegar:** entre em cada pasta de módulo e abra o notebook (`.ipynb`) correspondente.  
> **Ferramentas usadas:** Jupyter Notebook, `pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`, `scipy`, `statsmodels` (varia por projeto).

---

## Estrutura & Organização

- Os projetos estão organizados por **capítulos/módulos** (ex.: `Atividade_Cap10`, `Atividade_Cap12`, …).  
- Cada pasta contém o **notebook** do módulo e, quando aplicável, **arquivos de dados** usados na análise.  
- Os projetos são **independentes entre si**, mas refletem a progressão natural do curso (do básico ao avançado).  
  *Ex.: atividades de churn de telecom são evoluídas de um módulo ao seguinte, aprofundando técnicas e interpretações.*

---

## Projetos por Módulo

> Abaixo, um resumo **curto e objetivo** de cada módulo. Consulte o notebook de cada pasta para detalhes, gráficos e conclusões.

### 🔹 Atividade_Cap10 — Fundamentos & EDA inicial
Foco em **primeiros passos com pandas/numpy**, leitura de dados, inspeção de colunas, **estatística descritiva** e **visualizações básicas** para entender o comportamento dos dados e possíveis problemas de qualidade.  
(*Organização de dados, `describe()`, `info()`, contagens e gráficos simples.*) :contentReference[oaicite:0]{index=0}

### 🔹 Atividade_Cap12 — Prática na criação de gráficos
Explora **relações entre variáveis** (tabelas de contingência, proporções, gráficos de barras/linhas) e boas práticas de visualização para comunicar padrões.  
(*Uso de `pd.crosstab`, proporções por linha/coluna, leitura de gráficos e comparação de grupos.*) :contentReference[oaicite:1]{index=1}

### 🔹 Atividade_Cap13 — Prática na limpeza e padronização
Ênfase em **padronização de categorias**, tratamento de **valores ausentes** e checagens de consistência antes de análises mais profundas.  
(*Normalização de campos, conferência de regras de negócio e preparação dos dados para etapas seguintes.*) :contentReference[oaicite:2]{index=2}

### 🔹 Atividade_Cap14 — Projeto TeleCON, Etapa 1 (Limpeza e lidar com dados ausentes de forma responsável)
Projeto aplicado com dados de **telecom/churn**: verificação de **regras de negócio** (ex.: coerência entre serviços), uso de **crosstabs** e **imputação guiada por evidência** para colunas como `PhoneService`, evitando viés.  
(*Hipóteses, máscaras condicionais, análises de consistência e efeito de decisões de imputação.*) :contentReference[oaicite:3]{index=3}

### 🔹 Atividade_Cap15 — Projeto TeleCON, Etapa 2 (Análises univarias e bivariadas, lindando com outliers)
Aprofundamento da análise de **churn** com **quartis** (0–25–50–75–100%) e **faixas de tempo de cliente**, avaliando taxa de churn por segmentos e **estratificando** por potenciais confundidores (ex.: tipo de contrato).  
(*`pd.qcut` e `pd.cut`, churn por faixa, gráficos de barras empilhadas 100%, leitura de tendência e possível validação com regressão logística.*) :contentReference[oaicite:4]{index=4}

> Observação: os nomes das pastas seguem o padrão de capítulos/atividades do curso (ex.: `Atividade_Cap10`, `Atividade_Cap12`, `Atividade_Cap13`, `Atividade_Cap14`, `Atividade_Cap15`). :contentReference[oaicite:5]{index=5}

---

## O que você encontra nos notebooks

- **EDA clara e progressiva:** da visão geral aos recortes que respondem perguntas específicas.  
- **Visualizações objetivas:** gráficos que mostram proporções, distribuições e comparações entre grupos.  
- **Boas práticas de dados:** checagem de nulos, padronização de rótulos, máscaras condicionais e justificativas para imputação.  
- **Interpretação focada no negócio:** as leituras conectam os números a *insights* (ex.: segmentos com maior risco de churn).

---

## Observações úteis

- **Visualizações interativas (Plotly):** no preview do GitHub, gráficos interativos podem não aparecer.  
  Quando necessário, os notebooks exportam imagens estáticas para visualização direta.  
- **Ambiente:** qualquer ambiente com Jupyter e as bibliotecas citadas deve reproduzir as análises.

---

## Contato

Dúvidas, sugestões ou feedbacks são bem-vindos!  
Abra uma *issue* ou entre em contato diretamente pelo GitHub.

