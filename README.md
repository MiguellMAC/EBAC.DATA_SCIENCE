# 📊 Portfólio de Projetos – Ciência de Dados (EBAC)

[![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)](https://www.python.org/)  
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)](https://jupyter.org/)  
[![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-yellow?logo=pandas&logoColor=white)](https://pandas.pydata.org/)  
[![Plotly](https://img.shields.io/badge/Plotly-Interactive%20Viz-brightgreen?logo=plotly)](https://plotly.com/python/)  
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-red?logo=scikit-learn)](https://scikit-learn.org/stable/)

---

## 👤 Sobre mim

Sou **Miguel Cardoso**, estudante de **Ciência de Dados** na **EBAC** e também em formação em **Engenharia de Software** na FIAP.  
Este repositório reúne meus projetos didáticos, desenvolvidos durante o curso, como forma de **aprender, praticar e documentar** minha evolução.  

Embora os projetos tenham caráter **educacional**, eles mostram de forma prática minhas habilidades em:  
- **Python para Data Science**  
- **EDA (Exploração de Dados)**  
- **Limpeza e preparação de dados**  
- **Visualizações estáticas e interativas**  
- **Modelagem Preditiva** (classificação e regressão)  
- **Storytelling com dados**
- **Estatística aplicada**

> ⚠️ Os dados e códigos aqui são **apenas para fins didáticos** e não devem ser utilizados em produção.

---

## 📂 Estrutura do Repositório

- Cada pasta segue o formato `Atividade_CapX`, onde **X é o número do capítulo/módulo**.  
- Dentro de cada pasta há um notebook (`.ipynb`) com análises, gráficos e conclusões.  
- Os projetos são independentes, mas seguem uma linha de progressão: de fundamentos até Machine Learning.
- Cada pasta contém o **notebook** do módulo e, quando aplicável, **arquivos de dados** usados na análise.
- Os projetos são **independentes entre si**, mas refletem a progressão natural do curso (do básico ao avançado).  
  *Ex.: atividades de churn de telecom são evoluídas de um módulo ao seguinte, aprofundando técnicas e interpretações.*

> Observação: os nomes das pastas seguem o padrão de capítulos/atividades do curso (ex.: `Atividade_Cap10`, `Atividade_Cap12`, `Atividade_Cap13`, `Atividade_Cap14`, `Atividade_Cap15`).


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

## 🔹 Capítulo 17 — **Classificação: Credit Score**

**Objetivo.** Prever a faixa de **Credit Score** (ex.: *Low / Average / High*).

**Principais passos**
- **Tratamento e padronização**
  - Conversão de colunas numéricas (p.ex. `Income`) para **float** (ajuste de `.` e `,`).
  - **Imputação de `Age`** considerando o padrão observado com `Income` (ex.: médias por agrupamento acima/abaixo da média geral).
  - Padronização de rótulos categóricos (maiúsculas/minúsculas, valores “No internet service”, etc.).
- **EDA**
  - Contagens, **crosstabs** entre `Credit Score` e categóricas (ex.: `Education`, `Home Ownership`, etc.).
  - Histogramas e boxplots para entender distribuição de `Income`/`Age` por faixa de score.
- **Preparação**
  - **One-Hot Encoding** para categóricas (ex.: `Education`).
  - **Target**: `Credit Score` codificado como classe (0/1/2).
  - **Split** treino/teste com **estratificação** pelo target (mantém as proporções das classes).
- **Modelagem & Avaliação**
  - Classificador base (sklearn) para multiclasse.
  - Métricas: **accuracy** e **matriz de confusão**; análise de erros por classe.
- **Conclusões**
  - As variáveis socioeconômicas (ex.: `Income`, `Education`) mostram poder discriminativo; **balanceamento/estratificação** é importante devido à distribuição das classes.
  - Próximos passos: testar modelos lineares e baseados em árvores, validação cruzada e ajuste de limiar por classe.

---

## 🔹 Capítulo 18 — **Regressão: Previsão de Aluguel**

Notebook: regressão **simples** (apenas `Metragem`) e **múltipla** (variáveis estruturais do imóvel).

**Objetivo.** Prever **`Valor_Aluguel`** a partir das características do imóvel.

**Pré-processamento e EDA**
- Criação auxiliar de **`preco_m2 = Valor_Aluguel / Metragem`** **somente** para diagnóstico de outliers (não entra no modelo).
- **Regra transparente de *cap*** (IQR):
  - Quando **`Valor_Aluguel > 5900`** **e** **`preco_m2 > 63`**, substituir por `Metragem × 63`.  
  - Registro da **flag** e do **valor original** para auditoria.
- Tratamento adicional:
  - `Valor_Condominio`: remoção/trimming por p-quantil (ex.: p99) para reduzir cauda extrema.
  - **Feature derivada:** `N_Espaco = N_Quartos + N_Banheiros + 2×N_Suites + N_Vagas`.
- Exploração visual:
  - **Scatter com trendline** (`Metragem × Valor_Aluguel`) e facetas/cores por `N_Quartos`.
  - Boxplots/histogramas para entender dispersões e caudas.

**Modelagem**
- **Regressão Linear Simples** (target vs `Metragem`)
  - Equação (exemplo observado): **ŷ = −321,92 + 36,23 × Metragem**.
  - Resultado típico após tratamento: **R² ≈ 0,57** (antes ≈ 0,52).  
  - Observação: heterocedasticidade (dispersão cresce com metragem) — anotar como limitação.
- **Regressão Linear Múltipla**
  - Variáveis candidatas: `Metragem`, `Valor_Condominio`, `N_Quartos`, `N_Banheiros`, `N_Suites`, `N_Vagas`, `N_Espaco`.
  - Avaliação com **R²**, **MAE** e **RMSE** no **conjunto de teste**.
  - Comparação com o modelo simples para evidenciar ganho de explicação.

**Principais conclusões**
- A **metragem** sozinha já explica parte relevante do preço, mas existe grande variação (padrão de construção, vagas, suítes e condomínio pesam bastante).  
- O **tratamento de outliers** guiado por IQR melhorou a estabilidade do modelo.  
- Próximos passos naturais: regressão com `log(Valor_Aluguel)`, regularização (Ridge/Lasso) e validação cruzada.

### 🔹 Atividade_Cap19 — Estatística Aplicada
Estudo sobre **testes de hipóteses** usando o exemplo de duas estratégias de ensino de matemática.  
Foram simuladas amostras de notas de alunos, com análise de **médias e variâncias**, definição de hipóteses (H0 e H1) e aplicação de um **teste Z unilateral**.  
O foco foi interpretar médias, consistência das amostras, p-valor e região crítica em um gráfico da distribuição normal, concluindo sobre a significância estatística entre as duas estratégias.

### 🔹 Atividade_Cap20 — Projeto Credit Score com Naive Bayes
Aplicação do algoritmo de **Naive Bayes** para prever a faixa de **Credit Score** (*High, Average, Low*), dando continuidade ao pré-processamento feito no Cap. 17.  
O modelo foi treinado e avaliado em bases de treino e teste, trazendo métricas de **acurácia**, **recall macro** e **matriz de confusão**.  
Na fase de treino, apresentou alto desempenho; já no teste, os resultados caíram um pouco, mas continuaram bons, mostrando capacidade de generalização.  
O exercício reforçou como o Naive Bayes combina probabilidades das variáveis (assumindo independência) para classificar clientes, além de evidenciar limitações quando as variáveis não são totalmente independentes.

### 🔹 Atividade_Cap21 — Projeto Credit Score com Árvore de Decisão
Aplicação do algoritmo de **Árvore de Decisão** para prever o *Credit Score* (High, Average, Low), em continuação ao pré-processamento do Cap. 17.  
O modelo completo, usando todas as variáveis, atingiu acurácia perfeita em treino e teste (1.0).  
Com apenas as duas principais variáveis (Income e Age), obteve acurácia de 0.95 no teste, ainda com desempenho excelente.  
Na comparação com o **Naive Bayes** (Cap. 20), a Árvore se mostrou mais adequada, já que conseguiu capturar melhor os limiares das variáveis e entregar métricas superiores.


---

---

## O que você encontra nos notebooks

- **EDA clara e progressiva:** da visão geral aos recortes que respondem perguntas específicas.  
- **Visualizações objetivas:** gráficos que mostram proporções, distribuições e comparações entre grupos.  
- **Boas práticas de dados:** checagem de nulos, padronização de rótulos, máscaras condicionais e justificativas para imputação.  
- **Interpretação focada no negócio:** as leituras conectam os números a *insights* (ex.: segmentos com maior risco de churn).
- **Modelos de Machine Learning** exemplos seriam Regressão linear e árvore de decisão
- **Estatística aplicada** Utilização de estratégias estátiscas avançadas para validação de hipóteses
**Verificação da capacidade do modelo** Métodos para verificar coisas como acurácia e recall do modelo visando descobrir sua capacidade de acerto


---

## Observações úteis

- **Visualizações interativas (Plotly):** no preview do GitHub, gráficos interativos podem não aparecer.  
  Quando necessário, os notebooks exportam imagens estáticas para visualização direta.  
- **Ambiente:** qualquer ambiente com Jupyter e as bibliotecas citadas deve reproduzir as análises.

---

## Contato

Dúvidas, sugestões ou feedbacks são bem-vindos!  
Abra uma *issue* ou entre em contato diretamente pelo GitHub.

