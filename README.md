# Tabela Hash com Encadeamento usando Fila de Prioridade

Atividade desenvolvida para a disciplina de Resolução de Problemas Estruturados na Computação.

Implementação em Java de uma **tabela hash** com **100 posições** que recebe **1000 números aleatórios**. Quando há colisão, os valores da mesma posição são guardados em uma **lista encadeada ordenada em ordem crescente** (fila de prioridade).

## Requisitos da atividade

- Inserir 1000 elementos em uma matriz de 100 posições
- Em caso de colisão, usar uma lista encadeada na posição
- Gerar os números com `Random`, usando **seed = 1090**
- Usar números aleatórios no intervalo de **0 a 100 000**
- Ao final, mostrar:
  - a maior lista encadeada
  - quantas listas encadeadas foram geradas
  - quantas posições ficaram vazias
  - os três últimos valores inseridos em listas encadeadas
- **Restrição:** não usar comandos prontos da API do Java. Só são permitidos `if`, `else`, `for`, `while` e `Random`

## Estrutura

| Classe                | Função                                           |
| --------------------- | ------------------------------------------------ |
| `FilaDePrioridade`    | Lista encadeada com inserção ordenada crescente  |
| `FilaDePrioridade.No` | Nó da lista (`dado` + `proximo`)                 |
| `TabelaHash`          | Classe principal: inserção, análise e resultados |

### Métodos da `FilaDePrioridade`

| Método                | Descrição                                                             |
| --------------------- | --------------------------------------------------------------------- |
| `insereOrdenado(int)` | Insere o valor na posição certa da ordem crescente (aceita repetidos) |
| `removeElemento(int)` | Remove um valor da lista (não é usado na atividade)                   |
| `exibeLista()`        | Imprime os elementos da lista                                         |

## Como executar

```bash
javac TabelaHash.java
java TabelaHash
```

## Formato de saída esperada

```
Maior lista encadeada (posição X, N elementos):
Lista: v1 v2 v3 ...
Listas encadeadas geradas: N
Posições vazias: N
Três últimos valores inseridos em listas encadeadas:
  v1
  v2
  v3
```

> Como a seed é fixa (1090), o resultado é igual em toda execução.
