# Introdução à Análise Assintótica de Algoritmos

## 🎯 Objetivos
- Compreender o que é análise assintótica.
- Saber como medir a eficiência de um algoritmo.
- Aprender as principais notações: O (Ômega, Teta).
- Aplicar esses conceitos para comparar algoritmos na prática.

## 🧠 Comentário Inicial
Imagine que você vai a dois mercados. Em um, a fila demora 5 minutos para cada cliente. No outro, 1 minuto. Em qual mercado você escolheria ir, se a fila tiver 100 pessoas? Esse é o tipo de decisão que a análise assintótica nos ajuda a tomar, mas com algoritmos. Ela nos permite prever **como o tempo de execução ou uso de memória cresce** à medida que o tamanho dos dados aumenta.

---

## 📘 Conceito Fundamental

A **análise assintótica** estuda o **comportamento de um algoritmo quando a entrada tende ao infinito**. Ela nos dá uma forma de **comparar algoritmos independentemente do hardware** usado, focando no **crescimento da complexidade**.

### 🧪 Definição simples:
> “É uma forma de expressar o tempo ou espaço consumido por um algoritmo em função do tamanho da entrada (n), ignorando constantes e fatores de menor ordem.”

---

## 🎲 Analogia Visual

Imagine que você está enchendo baldes com areia. A velocidade com que o balde enche (a eficiência) depende do tamanho da pá (algoritmo). Se uma pá pega 1kg por vez e outra 10kg, a segunda é muito mais eficiente conforme a pilha de areia aumenta.

---

## 📊 Representação Visual

| Tamanho da Entrada (n) | Algoritmo A (O(n)) | Algoritmo B (O(n²)) |
|------------------------|-------------------|---------------------|
| 1                      | 1                 | 1                   |
| 10                     | 10                | 100                 |
| 100                    | 100               | 10.000              |
| 1000                   | 1000              | 1.000.000           |

🔍 Podemos ver que para entradas pequenas, a diferença parece irrelevante. Mas com o crescimento da entrada, **algoritmos com menor ordem de complexidade se destacam**.

---

## 🔧 Exemplo em Código (Java)

```java
    // Exemplo 1: Complexidade O(n)
    void imprimirNomes(String[] nomes) {
        for (String nome : nomes) {
            System.out.println(nome);
        }
    }
    
    // Exemplo 2: Complexidade O(n^2)
    void compararTodosComTodos(String[] nomes) {
        for (int i = 0; i < nomes.length; i++) {
            for (int j = 0; j < nomes.length; j++) {
                System.out.println(nomes[i] + " vs " + nomes[j]);
            }
        }
    }
```


🧾 Comentários:
	•	O primeiro algoritmo cresce linearmente: 1 ação por elemento.
	•	O segundo cresce quadraticamente: para cada elemento, compara com todos os outros.

⸻

🧪 Exercícios Práticos
	1.	Complete o código abaixo para calcular a soma de uma lista (complexidade O(n)):
```java
    int soma(int[] valores) {
        int total = 0;
        for (int i = 0; i < valores.length; i++) {
            // ????
        }
        return total;
    }
    
    	2.	Qual será o número de impressões do método compararTodosComTodos se nomes.length == 3?
    	3.	Corrija a análise de complexidade:
    
    for (int i = 0; i < n; i += 2) { 
        System.out.println(i); 
    }
```
❌ Complexidade O(n²)
✅ ???

	4.	Um algoritmo que executa 3 loops aninhados de tamanho n tem complexidade:
	•	( ) O(n)
	•	( ) O(n²)
	•	( ) O(n³)
	•	( ) O(log n)

⸻

🧪 Quiz de Múltipla Escolha
```
    1.	[Fácil] O que mede a análise assintótica?
	•	(A) O tempo de execução exato.
	•	(B) A quantidade de memória usada por um computador.
	•	(C) O crescimento do custo de tempo ou espaço de um algoritmo com a entrada.
	•	(D) O número de linhas de código.

    2.	[Fácil] Qual notação representa o pior caso?
	•	(A) Θ(n)
	•	(B) O(n)
	•	(C) Ω(n)
	•	(D) π(n)

    3.	[Médio] Se um algoritmo possui duas operações O(n) e O(n²), qual a complexidade final?
	•	(A) O(2n)
	•	(B) O(n²)
	•	(C) O(n + log n)
	•	(D) O(n)

    4.	[Médio] Qual algoritmo é mais eficiente para entradas grandes?
	•	(A) O(n²)
	•	(B) O(n log n)
	•	(C) O(2ⁿ)
	•	(D) O(n³)

    5.	[Avançado] Um algoritmo tem complexidade O(n) no melhor caso, O(n²) no pior caso e Θ(n log n) no caso médio. Isso indica:
	•	(A) Sempre é lento.
	•	(B) Só importa o pior caso.
	•	(C) Seu comportamento depende do tipo de entrada.
	•	(D) O tempo sempre cresce de forma linear.
```

⸻

✅ Gabarito
<details>
<summary>Mostrar respostas</summary>
    
	1.	(C) — Medimos como o tempo/memória cresce com n.
	2.	(B) — O(n) é a notação de pior caso.
	3.	(B) — O(n²) domina, pois cresce mais rápido.
	4.	(B) — O(n log n) é mais eficiente que os demais.
	5.	(C) — O desempenho varia com o tipo de entrada.
 
</details>


### 📌 Conclusão

A análise assintótica é uma das ferramentas mais poderosas para quem quer projetar software eficiente. Saber escolher um algoritmo mais rápido pode fazer toda a diferença em aplicações que lidam com grandes volumes de dados, como sistemas bancários, motores de busca ou jogos online.
