# Demonstracao-variancia
**Resumo:** Uma simples demonstração da variância da amostra estatística em Python.

# Já se questionou por que na fórmula da variância da amostra nós dividimos por "_n_-1" ?

---

Pois é, eu também tinha essa dúvida, como não conseguimos encontrar essa demonstração de forma muito tangível, pois quase sempre são abstrações, vim demonstrar do porquê fazemos esse cálculo.
<br>
<br>
<br>

# **Fórmula da variância da população**

$$ \sigma^2 = \frac{1}{N} \sum_{i=1}^{N} (x_i - \mu)^2 $$

Essa fórmula é essencial na estatística, com ela obtemos uma possibilidade de interpretar nossos dados muito melhor.

**Note** que a nossa somatória é dividida por N, que representa o total de indivíduos naquela população.

---

# **Fórmula da variância da amostra (não enviesada)**

$$ 
s^2 = \frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})^2
$$

Essa é a fórmula que naturalmente usamos e que a maioria dos algoritmos usam para calcular a variância amostral, onde temos a nossa somatória dividida por "*n*-1". E a razão desse "*n*-1" que vou demonstrar aqui nesse python notebook.

---

#### Quando não dividimos por "*n*-1", ou seja, dividimos somente por n, então temos uma variância amostral enviesada. Resumidamente, nossa variância amostral enviesada não se aproxima das medidas da nossa população quando tendemos nossos dados ao infinito.

---

# **Fórmula da variância da amostra (enviesada)**

$$
s^2 = \frac{1}{n} \sum_{i=1}^{n} (x_i - \bar{x})^2
$$

---
 Cabe ressaltar que quando obtemos um conjunto de dados pequeno, a variância amostral enviesada se aproxima mais da variância populacional, entretanto, na medida que aumentamos nosso conjunto de dados, a variância amostral não enviesada se aproxima muito mais da variância populacional e esse comportamento tende a aumentar quanto maior for o conjunto de dados.
 
Agora que já introduzi o que pretendo demonstrar nesse repositório, acompanhe-me até o script e vamos ver graficamente como isso é **verdadeiro.**
