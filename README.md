# 📚 Análise Assintótica de Algoritmos

## 📌 O que é Análise Assintótica?

Análise assintótica é uma forma de estudar o desempenho de um algoritmo quando o tamanho da entrada (geralmente denotado como `n`) **cresce muito**, tendendo ao infinito.  
O objetivo é entender como o tempo ou o espaço de execução **cresce em relação ao tamanho da entrada**, **ignorando constantes e detalhes menores**.

---

## 🎯 Por que isso é útil?

Porque não queremos saber apenas se um algoritmo é rápido com 10 elementos, mas sim **como ele se comporta com 10 mil, 1 milhão ou 1 bilhão de elementos**.

---

## 🧠 Tipos de Análise

| Tipo         | Símbolo     | Significado                                                                 |
|--------------|-------------|-----------------------------------------------------------------------------|
| Melhor caso  | Ω (Ômega)   | Quando tudo dá certo, o algoritmo roda no menor tempo possível.             |
| Caso médio   | Θ (Theta)   | Média de tempo/uso esperado, considerando todos os cenários.                |
| Pior caso    | O (Ô grande)| Quando tudo dá errado, o algoritmo roda no maior tempo possível.            |

> O mais comum em entrevistas e estudos é o **pior caso (`O`)**.

---

## 💡 Exemplo prático: Buscar um número em uma lista

### Código:
```java
public boolean busca(int[] lista, int alvo) {
    for (int i = 0; i < lista.length; i++) {
        if (lista[i] == alvo) return true;
    }
    return false;
}
```

### Análise:
- **Tamanho da entrada**: `n = lista.length`
- **Melhor caso (Ω(1))**: o número está na primeira posição.
- **Pior caso (O(n))**: o número está na última posição ou nem está.
- **Caso médio (Θ(n))**: o número está em alguma posição aleatória.

---

## 📈 Tabelinha dos principais tempos assintóticos

| Notação    | Nome           | Exemplo típico                                   |
|------------|----------------|--------------------------------------------------|
| `O(1)`     | Constante      | Acesso direto a um array: `arr[3]`              |
| `O(log n)` | Logarítmico    | Busca binária                                    |
| `O(n)`     | Linear         | Percorrer um array                               |
| `O(n log n)` | Quase-linear | MergeSort, QuickSort                             |
| `O(n²)`    | Quadrático     | BubbleSort, algoritmos com dois loops aninhados |
| `O(2ⁿ)`    | Exponencial    | Problemas de força bruta como subconjuntos       |
| `O(n!)`    | Fatorial       | Permutação de todos os elementos                 |

---

## 🎓 Importante lembrar

- A análise assintótica **não mede tempo real**, mas **crescimento relativo**.
- **Desconsidera detalhes como tipo de hardware, linguagem de programação ou otimizações do compilador**.
- **Nos ajuda a comparar algoritmos** independentemente do ambiente de execução.

---

## 🧪 Quer testar seu conhecimento?

Posso montar um **quiz com perguntas de múltipla escolha** sobre análise assintótica.  
Você gostaria que eu criasse esse quiz agora?
