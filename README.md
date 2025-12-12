# Relatórios de Otimização (Excel Solver)

## Visão Geral
Este repositório contém um conjunto de dados exportados em formato CSV, derivados de folhas de cálculo do Microsoft Excel. Os ficheiros documentam a resolução de problemas de Programação Linear utilizando o algoritmo **Simplex** através da ferramenta Solver.

Os ficheiros estão organizados por exercício e divididos em três tipos principais de relatórios de análise pós-otimização.

## Estrutura dos Ficheiros
Os ficheiros estão agrupados em 5 exercícios principais:

### 📁 Exercício 1: Produção de Posters
Focado num problema de planeamento de produção com restrições de impressão, corte e dobra.
* **Variáveis de Decisão:** Quantidade de Pósteres A, B, C e D.
* **Objetivo:** Maximizar o lucro (`z`).
* **Restrições:** Capacidade de horas nas máquinas (Impressão, Corte, Dobra) e encomendas mínimas.

### 📁 Exercício 2: Análise de Sensibilidade Estendida & Dualidade
Este é o exercício mais complexo em termos de volume de dados, contendo múltiplas iterações de relatórios (numerados de 1 a 16).
* **Contexto:** Parece envolver múltiplos cenários ou alterações incrementais nos parâmetros do Solver.
* **Dualidade:** Contém referências a uma folha `[ExDual.xlsx]`, indicando que o exercício aborda a transformação de problemas Primais em Duais.
* **Conteúdo:** Várias execuções do Solver, provavelmente para demonstrar como a solução ótima e os preços sombra variam com a alteração das restrições (Lado Direito - R.H.) ou dos coeficientes da função objetivo.

### 📁 Exercício 3: Fábrica de Carteiras
Problema clássico de mix de produção.
* **Variáveis de Decisão:** Carteiras Femininas (`Fem`) e Masculinas (`Masc`).
* **Restrições:** Processos de fabrico incluindo Corte, Costura, Acabamento e Empacotamento.
* **Objetivo:** Maximizar o lucro total.

### 📁 Exercício 4: Fábrica de Relógios
Problema de alocação de recursos humanos/tempo.
* **Variáveis de Decisão:** Relógios de Pedestal e Relógios de Parede.
* **Restrições:** Disponibilidade de horas de trabalho de pessoas específicas (Davi, Lia, Lídia).
* **Objetivo:** Maximizar o lucro (`z`).

### 📁 Exercício 5: Formulação Matemática
Um exercício focado na estrutura matemática e variáveis de folga.
* **Variáveis:** Genéricas ($x_1, x_2, x_3$).
* **Detalhes:** Os relatórios referem-se a "Variáveis de Folga", sugerindo um foco pedagógico na forma como o Simplex lida com desigualdades convertidas em igualdades.

---

## Legenda dos Tipos de Relatório

Cada exercício gera três tipos de ficheiros CSV, essenciais para a interpretação dos resultados:

1.  **Relatório de Respostas (`Relatório de Respostas X.csv`)**
    * Apresenta o valor final da **Função Objetivo**.
    * Lista os valores finais das **Variáveis de Decisão**.
    * Mostra o estado das restrições (se foram satisfeitas, vinculativas ou se existe folga).

2.  **Relatório de Sensibilidade (`Relatório de Sensibilidade X.csv`)**
    * Fundamental para a análise económica.
    * **Células Variáveis:** Mostra o *Custo Reduzido* e os limites permitidos para aumentar ou reduzir os coeficientes da função objetivo sem alterar a base ótima.
    * **Restrições:** Apresenta o **Preço Sombra** (Shadow Price), que indica quanto o valor da função objetivo melhoraria se a restrição fosse relaxada em uma unidade.

3.  **Relatório de Limites (`Relatório de Limites X.csv`)**
    * Mostra os limites inferior e superior que as variáveis podem assumir, mantendo as restrições satisfeitas, e o respetivo impacto no valor objetivo.

4.  **Planilha (`Planilha1.csv`)**
    * Contém a tabela original com os dados brutos do problema (coeficientes, restrições e matriz técnica) antes ou depois da resolução.

---

## Notas Técnicas
* **Motor do Solver:** LP Simplex.
* **Origem:** Microsoft Excel 16.0.
* **Formato:** CSV (Comma Separated Values), codificação compatível com Excel.
