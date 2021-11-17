# Estruturas de dados em java

## Notas

- Atribuições, em java, são por cópia de valor, sempre
- Com tipo primitivo, copiamos o valor em memória
- Com objetos, copiamos o valor da referência de memória, sem duplicar o objeto

```java 
MyObject obj1 = new MyObject(1);
MyObject obj2 = obj1;

System.out.println("Obj1: " + obj1.toString());
System.out.println("Obj2: " + obj2.toString());
System.out.println("------------");
obj2.setI(2);
System.out.println("Obj1: " + obj1.toString());
System.out.println("Obj2: " + obj2.toString());

// SAIDA
// Obj1: 1
// Obj2: 1
//--------
// Obj1: 2
// Obj2: 2
```

## Conceito de nó e encadeamento

Quando criamos um objeto ou armazenamos um dado, criamos uma estrutura, que pode ser chamada de nó, que vai receber o dado e permitir que ele seja encontrado e manipulado

### LIFO (last in, first out)

Esta estrutura é chamada de pilha, pois os novos elementos são empilhados sobre o anterior e deverá ser o primeiro a sair -- ser consumido.

#### **Manipulação da pilha**

Para manipular a pilha criamos três métodos principais

 - pilha.top()
   - Retorna o último elemento da pilha -- no caso o elemento do topo -- sem retirá-lo da pilha
   - A referência -- ponteiro -- continua apontando para o objeto que está no topo
   - Este método pode ser chamado quando o objeto é criado a fim de permitir que seja manipulado
 - pilha.pop()
   - Este método retorna o último elemento da pilha a fim de que seja manipulado, porém o retira da pilha[^comparativo01]
   - Neste caso a referência passa a apontar para o objeto anterior ao retirado.
 - pilha.push()
   - Adiciona um elemento ao topo da pilha. Este elemento apontará para o objeto anterior e nossa referência base apontará para o novo objeto
 - pilha.isEmpty()
   - Verifica se a referência aponta para null, caso esteja, a pilha está vazia.

A implementação da pilha pode ser vista neste [link](https://github.com/aphenrique/estrutura-de-dados)



[^comparativo01]: Um observação é que este conceito aparentemente não funciona desta maneira  na navegação do flutter. Quando é chamado o método pop() a página sai da pilha e deixa de existir, sem permitir ser manipulada -- carece de conferência