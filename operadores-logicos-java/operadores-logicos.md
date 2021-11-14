# Operadores lógico em java

Esta sessão foi criada por uma particularidade encontrada no java que era particularmente desconhecida - Disjunção exclusiva.

Seguem, então, os operadores lógicos do java

## Conjunção

Verdadeira quando ambas expressões envolvidas são verdadeiras

| exp | operador | exp | resultado |
| :-: | :-: | :-: | :-: |
| true | && | true | true |
| true | && | false | false |
| false | && | true | false |
| false | && | false | false |

## Disjunção

Verdadeira quando uma das expressões é verdadeira

| exp | operador | exp | resultado |
| :-: | :-: | :-: | :-: |
| true | \|\| | true | true |
| true | \|\| | false | true |
| false | \|\| | true | true |
| false | \|\| | false | false |

## Disjunção exclusiva

Verdadeira quando as expressões são opostas

| exp | operador | exp | resultado |
| :-: | :-: | :-: | :-: |
| true | ^ | true | false |
| true | ^ | false | true |
| false | ^ | true | true |
| false | ^ | false | false |

## negação

Inverte o resultado da expressão

| operador | exp | resultado |
| :-: | :-: | :-: |
| ! | true | false |
| ! | false | true |

# Boas práticas em operadores lógicos

- Switch servem para valores exatos e if(s) para testar expressões booleanas
- Evite usar default em switch para casos genéricos
- Evite o efeito flecha em if(s) -- quando se aninha if(s) dentro de if(s)
