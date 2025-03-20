# Estrutura de Dados

Uma **estrutura de dados** é uma forma de organizar, armazenar e manipular dados de maneira eficiente. Ela define a forma como os dados são armazenados na memória e as operações que podem ser realizadas sobre esses dados. O objetivo principal de usar estruturas de dados é otimizar o uso de recursos, como memória e tempo de processamento, e facilitar a implementação de algoritmos eficientes.

# Tipos de Estruturas de Dados

Existem várias estruturas de dados, que podem ser agrupadas em duas categorias principais: **estruturas lineares** e **estruturas não lineares**.

# 1. Estruturas Lineares

Essas estruturas armazenam dados de forma sequencial, onde o acesso aos dados segue uma ordem específica. Os exemplos mais comuns são:

# **Array (Vetor)**: 

Um array (ou vetor) é uma estrutura de dados que armazena uma coleção de elementos do mesmo tipo em uma sequência ordenada, esse elementos são armazenados em posições contíguas na memória. O acesso aos elementos de um array é feito por meio de índices, que geralmente começam em 0.
  - **Exemplo**: Lista de números `[1, 2, 3, 4]`.

Os arrays são ideais quando você precisa de acesso rápido e eficiente a dados do mesmo tipo, especialmente quando a quantidade de elementos é conhecida e constante. No entanto, se você precisar de flexibilidade para redimensionar ou trabalhar com dados de tipos diferentes, outras estruturas de dados, como listas ou dicionários, podem ser mais adequadas.

> Imagine que você tem uma **prateleira de livros** com vários espaços numerados de **0** até **N-1**. Cada espaço pode conter apenas um livro, e você pode pegar qualquer um deles instantaneamente ao saber sua posição.
> 
> No entanto, essa prateleira tem um tamanho fixo, o que significa que, se precisar adicionar mais livros e já estiver cheia, será necessário trocar por uma maior e reorganizar tudo. Além disso, remover ou inserir um livro no meio da prateleira pode ser trabalhoso, pois será preciso deslocar os outros livros para ajustar o espaço.
> 
> Apesar dessas limitações, a grande vantagem desse sistema é o acesso rápido e direto a qualquer livro, sem precisar procurá-lo um por um. 


### Vantagens dos Arrays ✅

- Todos os elementos do array são do mesmo tipo.
- Acesso rápido aos elementos, com tempo constante `(O(1))` usando índices.
- Uso otimizado de memória, com dados organizados de forma contígua.
- Arrays são fáceis de entender e implementar.

### Desvantagens dos Arrays ❌

- **Tamanho fixo**: O tamanho do array é determinado no momento da criação e não pode ser alterado dinamicamente (em algumas linguagens, como C e Java).
- **Redimensionamento ineficiente**: Para mudar o tamanho de um array, é necessário criar um novo e copiar os dados, o que pode ser custoso em tempo e memória.
- **Desperdício de memória**: Arrays grandes podem desperdiçar espaço, enquanto arrays pequenos exigem criação de novos arrays maiores se mais elementos forem necessários.
- **Inserção e remoção ineficientes**: Inserir ou remover elementos exige deslocamento de outros elementos, o que pode resultar em alto custo de tempo `(O(n))`.


## Exemplo de Código em Python:

Em Python, arrays podem ser representados usando **listas**.

```python
# Criando um array (lista) de números inteiros
numeros = [10, 20, 30, 40, 50]

# Acessando o primeiro elemento (índice 0)
print(numeros[0])  # Saída: 10

# Acessando o terceiro elemento (índice 2)
print(numeros[2])  # Saída: 30

# Modificando um elemento no índice 4
numeros[4] = 100
print(numeros)  # Saída: [10, 20, 30, 40, 100]

# Adicionando um novo elemento ao final do array
numeros.append(60)
print(numeros)  # Saída: [10, 20, 30, 40, 100, 60]

# Removendo o elemento no índice 2
numeros.pop(2)
print(numeros)  # Saída: [10, 20, 40, 100, 60]
```

# **Lista (List)** 
Uma Lista (List) em programação é uma estrutura de dados que pode armazenar vários elementos, como números, strings ou até mesmo outras listas. Diferente de um **array** fixo, a lista pode crescer e diminuir dinamicamente, permitindo a inserção ou remoção de elementos em qualquer posição.

  - **Exemplo**: Lista de compras (pode adicionar e remover itens facilmente).

```python
# Criando uma lista de frutas
frutas = ["Maçã", "Banana", "Laranja", "Uva"]

# Exibindo a lista completa
print("Lista de frutas:", frutas)

# Acessando elementos por índice
print("Primeira fruta:", frutas[0])  # Maçã
print("Última fruta:", frutas[-1])   # Uva

# Adicionando elementos à lista
frutas.append("Manga")  # Adiciona no final
print("Após adicionar Manga:", frutas)

# Inserindo elemento em uma posição específica
frutas.insert(2, "Morango")  # Insere "Morango" na posição 2
print("Após inserir Morango na posição 2:", frutas)

# Removendo um item da lista
frutas.remove("Banana")  # Remove a primeira ocorrência de "Banana"
print("Após remover Banana:", frutas)

# Removendo o último item da lista
ultima_fruta = frutas.pop()
print(f"Última fruta removida: {ultima_fruta}")
print("Lista após remoção do último item:", frutas)

# Ordenando a lista
frutas.sort()
print("Lista ordenada:", frutas)

# Tamanho da lista
print("Número total de frutas:", len(frutas))
```


# **Fila (Queue)** 
Funciona no modelo **FIFO** (First In, First Out), ou seja, o primeiro elemento a entrar é o primeiro a sair. Usada em processos onde a ordem de chegada precisa ser respeitada, como em uma fila de atendimento.

  - **Exemplo**: Fila de impressão de documentos.

> O primeiro documento enviado para a impressora será o primeiro a ser impresso, enquanto novos documentos entram no final da fila. A impressora processa os documentos na ordem de chegada.


```python=
# Criando uma fila vazia
fila = []

# Adicionando elementos à fila (Enqueue)
fila.append("Documento 1")
fila.append("Documento 2")
fila.append("Documento 3")

print("Fila inicial:", fila)

# Removendo o primeiro elemento da fila (Dequeue)
primeiro = fila.pop(0)  # Remove o primeiro elemento
print("Documento impresso:", primeiro)
print("Fila após impressão:", fila)
```

# **Pilha (Stack)**
Funciona no modelo **LIFO** (Last In, First Out), ou seja, o último elemento a entrar é o primeiro a sair. É usada em situações como chamadas de funções recursivas(chama a si mesma).

  - **Exemplo**: Imagine uma pilha de livros: o último livro colocado no topo da pilha é o primeiro a ser retirado. Para pegar um livro no meio, é necessário remover os que estão acima primeiro.

```python=
# Criando uma pilha vazia
pilha_de_livros = []

# Adicionando livros à pilha (Push)
pilha_de_livros.append("Livro A")
pilha_de_livros.append("Livro B")
pilha_de_livros.append("Livro C")

print("Pilha de livros:", pilha_de_livros)

# Removendo o último livro da pilha (Pop)
livro_removido = pilha_de_livros.pop()
print(f"Livro removido: {livro_removido}")
print("Pilha após remover o topo:", pilha_de_livros)
```

# 2. Estruturas Não Lineares

Essas estruturas não organizam os dados de maneira sequencial, permitindo relações mais complexas entre os elementos. Exemplos incluem:

## **Árvore (Tree)**
Organiza os dados em uma hierarquia, onde o nó raiz é o primeiro nó da árvore, e todos os outros nós são organizado para ter um nó pai para vários filhos. Cada elemento é chamado de nó, e os nós estão ligados por arestas. As árvores são úteis para representar hierarquias e são usadas em sistemas de arquivos, como o próprio sistema de arquivos de um computador.

- **Nós**: São os elementos da árvore (como vértices em um grafo). Cada nó pode armazenar informações.

- **Arestas**: São as conexões entre os nós (como as ligações entre vértices em um grafo). Elas indicam a relação hierárquica entre os nós, ou seja, como eles estão conectados.

  - **Exemplo**: Árvore genealógica.


```python=

           [Fruta]
           /    \
     [Citrus]   [Não Citrus]
       /   \        /    \
 [Laranja] [Limão]  [Maçã]  [Pera]

```

- **Nós**: "Fruta", "Citrus", "Não Citrus", "Laranja", "Limão", "Maçã", "Pera" são todos nós.
- **Arestas**: As linhas que conectam os nós indicam as arestas. Por exemplo, a aresta entre o nó "Fruta" e "Citrus" indica que "Citrus" é uma categoria de frutas.

> **Características das Árvores:**
> - **Nó Raiz:** O nó principal, de onde todas as outras conexões (nós filhos) se ramificam.
> - **Nó Pai:** Cada nó, exceto a raiz, tem um nó pai.
> - **Nó Filho:** Um nó que está abaixo de outro na hierarquia.
> - **Folhas:** Os nós que não têm filhos, ou seja, os nós mais baixos da árvore.
> - **Altura da Árvore:** O número máximo de arestas de um nó raiz até uma folha.

> **Exemplos de Árvores na Computação:**
> - **Árvore Binária:** Cada nó pode ter no máximo dois filhos.
> - **Árvore de Busca Binária:** Estrutura de árvore usada para armazenar dados de forma ordenada.
> - **Árvore de Decisão:** Usada em aprendizado de máquina para tomar decisões baseadas em um conjunto de regras.


## **Grafo (Graph)**
Um *grafo* é uma estrutura de dados que organiza informações em nós (também chamados de vértices) e arestas (também chamadas de ligações ou arcos) entre esses nós. Ele é usado para representar relacionamentos ou conexões entre objetos, e as conexões podem ser direcionadas (quando a ligação tem uma direção) ou não direcionadas (quando a ligação é bidirecional).
  - **Exemplo**: Mapa de estradas entre cidades.

## **Tabela de Hash (Hash Table)**: 
Usa uma função de hash para mapear dados para um índice em uma tabela. É ideal para buscas rápidas, pois permite acessar dados em tempo constante (O(1)) em muitas implementações.
  - **Exemplo**: Armazenar palavras em um dicionário para busca rápida.

# Resumo das Estruturas de Dados

| Tipo de Estrutura   | Características                                      | Exemplos                              |
|---------------------|------------------------------------------------------|---------------------------------------|
| **Arrays**          | Tamanho fixo, acesso rápido por índice               | Lista de números, matriz             |
| **Listas**          | Tamanho dinâmico, inserção/remover flexível          | Lista de compras, lista de tarefas   |
| **Pilhas**          | Acesso **LIFO** (Last In, First Out)                 | Histórico de navegação, chamadas de funções |
| **Filas**           | Acesso **FIFO** (First In, First Out)               | Fila de impressão, filas de processos |
| **Árvores**         | Dados hierárquicos, cada nó pode ter filhos          | Árvore genealógica, estrutura de diretórios |
| **Grafos**          | Dados conectados por arestas, pode ter ciclos        | Mapa de ruas, redes sociais          |
| **Tabelas de Hash** | Acesso rápido através de chave de hash               | Dicionário, cache de dados           |





