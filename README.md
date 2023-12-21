# Pacote de operações de uma ArvoreBinaria 

Um simples pacote com operações de um Binary Tree

## Instalação

Para instalar execute:

```
python setup.py install
```

## Uso

Exemplo de uso do módulo `ArvoreBinaria`:

### Importando a biblioteca
```py
from arvorebinaria import  ArvoreBinaria, construir_arvore
```


###  Exemplo 1: Criando um nó de cada vez

```py
arvore = ArvoreBinaria(4)
arvore.filha_esquerda = ArvoreBinaria(10)
arvore.filha_direita = ArvoreBinaria(3)
arvore.filha_esquerda.filha_esquerda = ArvoreBinaria(5)
arvore.filha_esquerda.filha_direita = ArvoreBinaria(1)


print("Arvore 1 na forma de Array:")
lista_1 = arvore.to_array()
print(lista_1)
print()

# Método para transformar a árvore em um heap.
# No pacote temos também a função heapify, que transforma uma subarvore em heap
arvore.buildmaxheap()

# convertendo a arvore1 na representação de array.
lista_2 = arvore.to_array()
print("Arvore 1 (heap) na forma de Array:")
print(lista_2) 
print()
#  Imprimindo uma representação gráfica da árvore 1 na tela com uma mensagem especial (:.
arvore.print_tree()

print()
print()
```

### Exemplo 2: Transformando uma lista numa arvore e em seguida, num heap


```py
print("Arvore 2 na forma de Array:")
array_exemplo = [4, 2, 7, 1, 3, 6, 9]

# Transformando a lista de valores numa arvore
arvore2 = construir_arvore(array_exemplo)

# convertendo a arvore2 na representação de array.

lista_3 = arvore2.to_array()
print(lista_3)
print()
print("Arvore 2 (heap) na forma de Array :")


# Transformando a arvore2 num heap
arvore2.buildmaxheap()

lista_4 =arvore2.to_array()
print(lista_4)

print()
arvore2.print_tree()
```

