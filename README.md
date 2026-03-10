# 📊 Testes de Hipótese — Atividade FIAP

**Disciplina:** Estatística / Ciência de Dados  
**Professor:** Nemec  
**Data:** 09/03/2026  

---

## 📌 Descrição

Este repositório contém a resolução da atividade de **Testes de Hipótese** aplicados a datasets de diferentes domínios. Cada instância apresenta quatro questões (A, B, C, D) que exigem a escolha e execução do teste estatístico adequado, interpretação do p-value e cálculo de uma soma final como resposta.

A lógica de decisão é padronizada em todas as instâncias:

- Se **p < 0,05** → diferença significativa → retorna a estatística relevante do grupo vencedor (maior média, menor média, maior/menor mediana, conforme o contexto).
- Se **p ≥ 0,05** → sem diferença significativa → retorna a estatística geral (média ou mediana de todos os dados).

---

## 🗂️ Estrutura dos Datasets

Os datasets estão organizados em subpastas por instância:

```
Dados/
├── instancia_01_futebol/dataset.csv
├── instancia_02_futebol/dataset.csv
├── instancia_03_hospital/dataset.csv
├── instancia_04_ecommerce/dataset.csv
├── instancia_05_ecommerce/dataset.csv
├── instancia_06_ecommerce/dataset.csv
├── instancia_07_futebol/dataset.csv
├── instancia_08_manufatura/dataset.csv
├── instancia_09_futebol/dataset.csv
├── instancia_10_manufatura/dataset.csv
├── instancia_11_streaming/dataset.csv
├── instancia_12_futebol/dataset.csv
├── instancia_13_futebol/dataset.csv
...
└── instancia_24_ecommerce/dataset.csv
```

### Domínios e variáveis analisadas

| Domínio | Variáveis |
|---|---|
| **Futebol** | `finalizacoes`, `faltas`, `cartoes_amarelos`, `gols`, `posse_bola`, `rodada`, `time`, `tecnico` |
| **Hospital** | `sono_horas`, `dor_antes`, `dor_depois`, `recuperacao_dias`, `tratamento` |
| **E-commerce** | `conversao_antes_pct`, `conversao_depois_pct`, `satisfacao`, `ticket_medio`, `tempo_antes_min`, `tempo_depois_min`, `campanha`, `dispositivo` |
| **Manufatura** | `temperatura_antes`, `temperatura_depois`, `vibracao`, `defeitos`, `tempo_ciclo_s`, `maquina`, `turno` |
| **Streaming** | `avaliacao`, `churn_pct`, `minutos_antes`, `minutos_depois`, `interface`, `plano`, `cliques_home` |

---

## 🧪 Testes Estatísticos Utilizados

| Teste | Quando usar |
|---|---|
| **t-test independente (Student)** | Comparação de médias entre dois grupos independentes com variâncias homogêneas |
| **t-test de Welch** | Comparação de médias entre dois grupos independentes com variâncias diferentes (`equal_var=False`) |
| **t-test pareado** | Comparação de médias em medições antes/depois no mesmo grupo |
| **Mann-Whitney U** | Comparação não-paramétrica de medianas entre dois grupos independentes |
| **Wilcoxon signed-rank** | Comparação não-paramétrica pareada (antes vs. depois) |
| **Teste de Levene** | Verificação de homogeneidade de variâncias antes do t-test independente |

---

## ▶️ Como Executar

### Pré-requisitos

```bash
pip install pandas numpy scipy jupyter
```

### Rodando o notebook

1. Clone o repositório ou faça o download dos arquivos.
2. Ajuste os caminhos dos CSVs no notebook para o seu ambiente local:
   ```python
   # Exemplo — substitua pelo caminho correto na sua máquina
   df = pd.read_csv(r'Dados/instancia_01_futebol/dataset.csv')
   ```
3. Abra o notebook:
   ```bash
   jupyter notebook Testes_hipotese.ipynb
   ```
4. Execute todas as células em sequência (`Kernel > Restart & Run All`).

---

## 📋 Instâncias e Resultados

| Instância | Domínio | Soma Final |
|---|---|---|
| 01 | Futebol | 35.12 |
| 02 | Futebol | 70.21 |
| 03 | Hospital | 24.42 |
| 04 | E-commerce | 168.44 |
| 05 | E-commerce | 26.73 |
| 06 | E-commerce | 167.26 |
| 07 | Futebol | 36.59 |
| 08 | Manufatura | 215.22 |
| 09 | Futebol | 81.03 |
| 10 | Manufatura | 137.83 |
| 11 | Streaming | 164.91 |
| 12 | Futebol | 69.10 |
| 13 | Futebol | 34.69 |
| 14 | Futebol | 80.72 |
| 15 | E-commerce | 169.97 |
| 16 | E-commerce | 26.48 |
| 17 | Manufatura | 135.28 |
| 18 | Manufatura | 136.52 |
| 19 | Futebol | 70.64 |
| 20 | Manufatura | 173.84 |
| 21 | E-commerce | 164.29 |
| 22 | Manufatura | 215.56 |
| 23 | Streaming | 105.65 |
| 24 | E-commerce | 184.80 |

---

## 👥 Integrantes

| Nome | Instâncias |
|---|---|
| **Hacker** | 01 – 06 |
| **Kenzo** | 07 – 12 |
| **Guilherme** | 13 – 18 |
| **Anna** | 19 – 24 |

---

## 🛠️ Tecnologias

- Python 3.14
- [pandas](https://pandas.pydata.org/)
- [numpy](https://numpy.org/)
- [scipy.stats](https://docs.scipy.org/doc/scipy/reference/stats.html)
- Jupyter Notebook
