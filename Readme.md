# Análise de Vendas da Allure Store

## Introdução
Este projeto analisa dados de vendas de quatro lojas da Alura Store para ajudar o Senhor João a decidir qual loja vender e financiar um novo empreendimento.  
Utilizando Python no Jupyter Notebook, a análise avalia:

- Faturamento
- Vendas por categoria
- Avaliações de clientes
- Custos de frete
- Produtos mais e menos vendidos  

Tabelas e gráficos são gerados para apoiar a tomada de decisão.

---

## Propósito da Análise
O objetivo principal é identificar a loja com menor desempenho financeiro e recomendar sua venda. A análise contempla:

- **Faturamento** por loja, cidade e tipo de pagamento
- **Vendas e faturamento** por categoria de produto
- **Avaliação média** dos clientes
- **Custos de frete** por loja e estado
- **Produtos mais e menos vendidos** por loja e local de compra

---

## Estrutura do Projeto

O repositório contém:

- `Challenge_AluraStoreBr.ipynb`: Notebook com código de análise, importação de dados, cálculos, tabelas e gráficos.
- `README.md`: Este arquivo, com instruções e detalhes.
- Gráficos gerados:
  - `grafico_faturamento_total_loja.png`
  - `grafico_barras_faturamento_cidade.png`
  - `grafico_barras_faturamento_tipo_pagamento.png`
  - `grafico_barras_vendas_categoria.png`
  - `grafico_barras_avaliacao_compra.png`
  - `grafico_pizza_produtos_destaque.png`
  - `grafico_pizza_produtos_destaque_local_compra_cores_diferentes.png`

**Observação:**  
Os dados são carregados diretamente de URLs públicas, sem necessidade de arquivos locais.

---

## Dados

Cada loja possui registros de vendas:

- **Registros:** 2.359 por loja (exceto Loja 4 com 2.358 registros)
- **Colunas:**
  - Produto
  - Categoria do Produto
  - Preço
  - Frete
  - Data da Compra
  - Vendedor
  - Local da compra
  - Avaliação da compra
  - Tipo de pagamento
  - Quantidade de parcelas
  - Latitude e longitude

**Fontes de dados:**  
- Loja 1
- Loja 2
- Loja 3
- Loja 4

---

## Ferramentas Utilizadas

- **pandas:** Manipulação e tratamento dos dados
- **matplotlib**/**seaborn:** Criação de gráficos
- **tabulate:** Formatação de tabelas
- **Jupyter Notebook:** Ambiente interativo de desenvolvimento

**Etapas do notebook:**

- Importação de dados diretamente das URLs
- Concatenação dos dados (com inclusão da coluna "Loja")
- Cálculo de faturamento (`Preço + Frete`)
- Geração de tabelas e gráficos

---

## Resultados e Insights

### Faturamento
Loja  Faturamento (R$) 
Loja 1: R$1.616.347,09
Loja 2: R$1.567.773,22
Loja 3: R$1.542.047,69
**Loja 4** **1.458.253,46**

> **Insight:** Loja 4 tem o menor faturamento, sendo a principal candidata à venda.

---

### Avaliações

- Loja 1: 3.98
- Loja 2: 4.04
- Loja 3: 4.05
- Loja 4: 4


> **Insight:** Loja 4 possui boas avaliações, mas não compensa o faturamento inferior.

---

### Custos de Frete

- Frete Médio Loja 1: R$34,69
- Frete Médio Loja 2: R$33,62
- Frete Médio Loja 3: R$33,07
- Frete Médio Loja 4: R$31,28

> **Insight:** Loja 4 apresenta o menor custo de frete, mas o impacto no faturamento é limitado.

---

### Categorias de Produto
- Móveis e eletrônicos representam entre 19% e 21% do faturamento total.

> **Insight:** Categorias dominantes em todas as lojas.

---

### Estados
- **São Paulo**, **Rio de Janeiro**e **Minas Gerais** lideram o faturamento em todas as lojas.

> **Insight:** O mercado é concentrado em grandes centros urbanos.

---

## Gráficos Gerados

- Faturamento por loja
- Faturamento por cidade
- Faturamento por tipo de pagamento
- Vendas por categoria
- Avaliação média por loja
- Produtos mais e menos vendidos
- Produtos por local de compra

---

## Recomendação Final
Com base na análise, recomenda-se vender a **Loja 4**, que apresenta:

- Menor faturamento (R$1.458.253,46)
- Avaliações médias satisfatórias (4,00)
- Custos de frete competitivos (R$31,28)

No entanto, o desempenho financeiro é o mais fraco entre todas as lojas, cerca de 10% inferior à Loja 1.

---

## Instruções para Executar o Projeto

### Pré-requisitos:

- Python 3.8+
- Jupyter Notebook
- Bibliotecas instaladas: `pandas`, `matplotlib`, `seaborn`, `tabulate`

### Passos:

1. **Clone o Repositório:**
   ```bash
   git clone https://github.com/ribeiroarley/challenge-alura-store.git
   cd challenge-alura-store
   ```

2. **Crie e Ative o Ambiente Virtual:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/Mac
   venv\Scripts\activate     # Windows
   ```

3. **Instale as Dependências:**
   ```bash
   pip install pandas matplotlib seaborn tabulate jupyter
   ```

4. **Execute o Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```

5. **Abra e execute o arquivo:** `Challenge_AluraStoreBr.ipynb`

- Dados são carregados automaticamente de URLs públicas.
- Tabelas são exibidas e gráficos são salvos como PNGs.

---

## Desenvolvido por
**Arley Ribeiro da Silva Xavier**

---

## Agradecimentos
Agradeço à **Oracle Next Education (ONE)** e à **Alura** pela oportunidade e pelo desafio proposto.