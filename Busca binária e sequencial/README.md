feat: adiciona comparativo de desempenho entre Busca Sequencial e Binária em Java
# 🔍 Comparativo de Algoritmos: Busca Sequencial vs Busca Binária

Este projeto em Java foi desenvolvido como Atividade Prática Supervisionada (APS) para demonstrar, na prática, a diferença de desempenho e a complexidade de tempo entre dois algoritmos clássicos de busca: **Busca Sequencial ($O(n)$)** e **Busca Binária ($O(\log n)$)**.

## 🎯 Objetivo
Analisar o tempo de execução de ambos os algoritmos submetidos ao **pior caso possível** (buscar o último elemento de um array ordenado), escalando o volume de dados de 1.000 até 100 milhões de elementos.

## ⚙️ Como funciona
O programa realiza as seguintes etapas automatizadas:
1. **Geração de Dados:** Cria arrays preenchidos com números aleatórios.
2. **Ordenação:** Utiliza `Arrays.sort()` para ordenar os dados, pré-requisito para a Busca Binária.
3. **Métrica de Tempo:** Captura os microssegundos exatos de execução usando `System.nanoTime()`.
4. **Repetição e Média:** Executa 5 repetições para cada tamanho de array (N) para garantir uma média precisa, mitigando oscilações do processador/JVM.
5. **Relatório:** Imprime uma tabela no console comparando os tempos (em milissegundos) e exibindo a razão de lentidão entre a busca sequencial e a binária.

## 💻 Tecnologias e Conceitos Aplicados
- **Linguagem:** Java
- **Estruturas de Dados:** Manipulação de Arrays unidimensionais.
- **Análise de Complexidade (Big-O):** Validação prática de que a busca binária é ordens de magnitude superior para grandes volumes de dados.
- **Prevenção de Bugs:** Cálculo do índice central da busca binária formatado como `esquerda + (direita - esquerda) / 2` para evitar falhas de *Integer Overflow*.

## 🚀 Como Executar
1. Certifique-se de ter o [JDK](https://www.oracle.com/java/technologies/downloads/) instalado.
2. Compile o arquivo:
   ```bash
   javac Aps.java