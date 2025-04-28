# Análise de Vendas da Alura Store

---

## Introdução
Eu sou **Arley Ribeiro**, Analista de Dados, e este relatório avalia o desempenho de quatro lojas do Sr. João, de 2020 a 2023, para recomendar qual deve ser vendida. A análise considera cinco métricas:

- *Faturamento total*
- *Vendas por categoria de produto*
- *Média de avaliações dos clientes*
- *Produtos mais e menos vendidos*
- *Custo médio de frete*

A análise foi realizada em Python, usando **Jupyter Notebook** e bibliotecas como `pandas`, `matplotlib`, `seaborn` e `tabulate`.

## Propósito da Análise
O objetivo é identificar a loja com menor desempenho e recomendar sua venda, analisando:
- **Faturamento**: Receita por loja, estado e tipo de pagamento.
- **Vendas por categoria**: Distribuição e faturamento por categoria.
- **Avaliações**: Satisfação média dos clientes.
- **Produtos mais/menos vendidos**: Padrões de demanda.
- **Custos de frete**: Impacto logístico.

## Estrutura do Projeto

- `Challenge_AluraStoreBr.ipynb`: Notebook com código, cálculos, tabelas e gráficos.
- `README.md`: Este documento, com detalhes do projeto e instruções.

---

## Metodologia

### Importação dos Dados
- Dados carregados de URLs públicas via `pandas.read_csv()`.
- Adicionada coluna "Loja" para identificar registros.
- Primeiras cinco linhas de cada loja exibidas com `tabulate`.

### Exploração e Análise
- **Faturamento**: Calculado por loja, estado e tipo de pagamento.
- **Vendas por categoria**: Distribuição e faturamento por categoria.
- **Avaliações**: Média das avaliações dos clientes.
- **Produtos mais/menos vendidos**: Identificação por loja e estado.
- **Frete**: Custo médio por loja e estado.

### Visualização
- Gráficos com `matplotlib` e `seaborn` (barras, boxplots).
- Tabelas formatadas com `tabulate`.

### Ferramentas Utilizadas
- `pandas`: Manipulação de dados.
- `matplotlib`/`seaborn`: Visualização.
- `tabulate`: Formatação de tabelas.
- `Jupyter Notebook`: Ambiente interativo.

---

## Resultados

### 1. Importação dos Dados
Os dados foram organizados a partir de CSVs no GitHub, com estrutura consistente entre lojas.

### 2. Análise do Faturamento
Faturamento total por loja **(2020–2023)**:

| Loja      | Faturamento (R$) |
|-----------|------------------|
| Loja 1    | 1.616.347,09     |
| Loja 2    | 1.567.773,22     |
| Loja 3    | 1.542.047,69     |
| **Loja 4**|**1.458.253,46**  |

**Por Estado (Loja 4)**:

| Local da Compra | Faturamento (R$) |
|-----------------|------------------|
| SP              | 588.862,89       |
| RJ              | 179.151,26       |
| MG              | 174.715,71       |
| ...             | ...              |
| **Total Loja 4**| **1.458.253,46** |

**Por Tipo de Pagamento** (todas as lojas):

| Tipo de Pagamento   | Faturamento (R$) |
|---------------------|------------------|
| Cartão de Crédito   | 4.537.242,96     |
| Boleto              | 1.236.563,66     |
| Cupom               | 331.304,44       |
| Cartão de Débito    | 79.310,39        |

**Insight**: A Loja 4 tem o menor faturamento, com desempenho inferior em estados-chave: SP, RJ e MG. O cartão de crédito predomina, mas não diferencia a Loja 4.

### 3. Vendas por Categoria
Distribuição de vendas e faturamento por categoria (Loja 4):

| Categoria                | Vendas | Faturamento (R$) | Porcentagem (%) |
|--------------------------|--------|------------------|-----------------|
| Móveis                   | 480    | 270.352,16       | 20.36           |
| Eletrônicos              | 451    | 575.071,18       | 19.13           |
| Brinquedos               | 338    | 28.498,67        | 14.33           |
| Esporte e Lazer          | 277    | 46.825,77        | 11.75           |
| Eletrodomésticos         | 254    | 397.710,75       | 10.77           |
| Utilidades Domésticas    | 201    | 21.237,76        | 8.52            |
| Livros                   | 187    | 13.148,81        | 7.93            |
| Instrumentos Musicais    | 170    | 105.408,35       | 7.21            |
| **Total**                | **2358**| **1.458.253,46** | **100.00**     |

**Insight**: Móveis e eletrônicos lideram, mas a Loja 4 não se destaca.

### 4. Média de Avaliação
Média das avaliações dos clientes (escala 0–5):

| Loja   | Avaliação Média |
|--------|-----------------|
| Loja 1 | 3.98            |
| Loja 2 | 4.04            |
| Loja 3 | 4.05            |
| Loja 4 | 4.00            |

**Insight**: A Loja 4 tem avaliação satisfatória.

### 5. Produtos Mais e Menos Vendidos: Loja 4

| Destaque       | Produto                     | Vendas | Faturamento (R$) | Porcentagem (%) |
|----------------|-----------------------------|--------|------------------|-----------------|
| Mais Vendido   | Cama box                    | 62     | 46.264,11        | 25.4            |
| Menos Vendido  | Guitarra                    | 33     | 36.232,51        | 24.8            |

**Por Estado (São Paulo)**:

| Local | Destaque       | Produto                     | Vendas | Faturamento (R$) | Porcentagem (%) |
|-------|----------------|-----------------------------|--------|------------------|-----------------|
| SP    | Mais Vendido   | Carrinho controle remoto    | 104    | 10.387,06        | 32.3            |
| SP    | Menos Vendido  | Headset                     | 57     | 11.150,45        | 53.8            |

**Insight**: A Loja 4 não se destaca.

### 6. Frete Médio
Custo médio de frete por loja:

| Loja   | Frete Médio (R$) |
|--------|------------------|
| Loja 1 | 34,69            |
| Loja 2 | 33,62            |
| Loja 3 | 33,07            |
| Loja 4 | 31,28            |

**Por Estado (Loja 4)**:

| Local da Compra | Frete Médio (R$) | Frete Mínimo (R$) | Frete Máximo (R$) | Total de Vendas |
|-----------------|------------------|-------------------|-------------------|-----------------|
| RO              | 59,67            | 9,38              | 110,57            | 4               |
| MA              | 45,66            | 0,00              | 184,78            | 19              |
| PA              | 44,96            | 0,00              | 170,90            | 17              |
| ...             | ...              | ...               | ...               | ...             |
| **Média Loja 4**| **31,28**        | -                 | -                 | **2358**        |

**Insight**: A Loja 4 tem o menor frete médio, mas isso não compensa o baixo faturamento.

---

## Recomendação Final
Recomendo a **venda da Loja 4** em **janeiro de 2024**, após os picos sazonais de novembro e dezembro (estimativa de faturamento: R$218.738,02). **Justificativa**:
- Menor faturamento (R$1.458.253,46).
- Avaliações satisfatórias, mas não excepcionais.
- Eficiência em frete não compensa a baixa receita.

A venda pós-pico sazonal maximiza o valor percebido, destacando a capacidade de receita e categorias principais (móveis e eletrônicos).

---

## Instruções para Executar o Projeto

### Pré-requisitos
- Python 3.8+
- Jupyter Notebook
- Bibliotecas: `pandas`, `matplotlib`, `seaborn`, `tabulate`

### Passos
1. Clone o repositório:
   ```bash
   git clone https://github.com/ribeiroarley/challenge-alura-store.git
   cd challenge-alura-store
   ```

2. Crie e ative o ambiente virtual:
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/Mac
   venv\Scripts\activate     # Windows
   ```

3. Instale as dependências:
   ```bash
   pip install pandas matplotlib seaborn tabulate jupyter
   ```

4. Execute o Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

5. Abra e execute `Challenge_AluraStoreBr.ipynb`.

**Notas**:
- Dados são carregados automaticamente das URLs.
- Gráficos são salvos como PNGs.
- Tabelas são exibidas no notebook.

## Desenvolvido por 💼
**Arley Ribeiro da Silva Xavier**



## Agradecimentos
Agradeço à **Oracle Next Education (ONE)** e à **Alura** pelo desafio e oportunidade de aprendizado.