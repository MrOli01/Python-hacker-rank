## Python exercicies level easy

### >> 1. Say "Hello, World!" Imprima para stdout.Hello, World!

````python 
print("Hello, World!")
````

### >> 2. O código incluido lerá um inteiro, do STDIN.n. Sem usar nenhum método de sequeência de strings, tente imprimir o seguinte: 123...n

````python
if __name__ == '__main__':
    n = int(input())
    for i in range(1,n+1):
        print(i,end='')
````

### >> 3. Imprima a lista em ordem lexicográfica crescente.



````python 
if __name__ == '__main__':
    x = int(input())
    y = int(input())
    z = int(input())
    n = int(input())
    
    print(list([i,j,k] for i in range(x+1) for j in range(y+1) for k in range(z+1)  if i+j+k !=n))
````
### >> 4. Você recebe o nome e sobrenome de uma pessoa em duas linhas diferentes. Sua tarefa é lê-los e imprimir o seguinte:

````python 
def print_full_name(a, b):
     print("Hello {} {}! You just delved into python.".format(a,b))
````

### >> 5. O código fornecido lê dois inteiros e, de STDIN. Adicione lógica para imprimir duas linhas. A primeira linha deve conter o resultado da divisão de inteiros, // . A segunda linha deve conter o resultado da divisão de flutuação, / . Não é necessário arredondamento ou formatação.

Exemplo: a = 3 b = 5 

````python 
if __name__ == '__main__':
    a = int(input())
    b = int(input())
    int_result = int(a/b)
    float_result = a/b
    print(int_result)
    print(float_result)
````

### >>. 6. Dada uma inteiro, e inteiros separados pelo espaço como entrada, crie uma tupla, desses inteiros. Em seguida, calcular e imprimir o resultado 

````python  
if __name__ == '__main__':
    n = int(input())
    integer_list = map(int, input().split())
    t = tuple(integer_list)
    print(hash(t))
````

### >> 7. Dada a pontuação dos participantes para o seu Dia de Esportes Universitários, você é obrigado a encontrar a pontuação do vice-campeonato. Você tem pontuação. Guarde-os em uma lista e encontre a pontuação do segundo colocado. 

````python
if __name__ == '__main__':
    n = int(raw_input())
    arr = map(int, raw_input().split())
    print(sorted(set(arr))[-2])
````

### >> 8. O código fornecido lê e inteiro, da STDIN. Para todos os inteiros não negativos ni < n print i ao cubo exemple = n = 3 A lista de inteiros não negativos que são menores que n = 3 é [0,1,2]. Imprima o quadrado de cada numero em uma linha separada.

````python
if __name__ == '__main__':
    n = int(input())
    print(*[num**2 for num in range(n)], sep='\n')
````

### >> 9.  Fulano é o dono de uma loja de sapatos. A loja dele tem o número de sapatos.
Ele tem uma lista contendo o tamanho de cada sapato que tem em sua loja.
Há um número de clientes que estão dispostos a pagar XnX quantidade de dinheiro apenas se eles recebem o sapato de seu tamanho desejado.

Sua tarefa é calcular quanto dinheiro Fulano auferido. 

````python 
import collections # Nos ajuda a trabalhar com tuplas, dicionarios e listas

numSapatos = int(input())
sapatos = collections.Counter(map(int, input().split()))  # collections.counter serve para fazer contagem de objetos
numCusto = int(input())

income = 0

for i in range(numCusto):
    size, price = map(int, input().split())
    if sapatos[size]: 
        income += price
        sapatos[size] -= 1

print(income)
````

### >> 10. Dado os nomes e notas de cada aluno de uma classe de alunos, armazene-os em uma lista aninhada e imprima os nomes de qualquer aluno com a segunda menor nota N

````python
if __name__ == '__main__':
    students = []
    for _ in range(int(input())):
        name = input()
        score = float(input())
        students.append([name,score]) 
    x = 99999
    for i in range(len(students)):
        if x > float(students[i][1]):
            x = float(students[i][1])
    y = 999999
    for i in range(len(students)):
        if float(students[i][1]) > float(x) and y > float(students[i][1]):
            y = float(students[i][1])
    runner = []
    for i in range(len(students)):
        if float(students[i][1]) == float(y):
            runner.append(students[i][0])
    runner = sorted(runner)

    for i in range(len(runner)):
        print(runner[i])
        
````

### >> 11. Converta todas as letras minúsculas em letras maiúsculas e vice-versa. Entrada da amostra: HackerRank.com presents "Pythonist 2". Saída da amostra: hACKERrANK.COM PRESENTS "pYTHONIST 2". 

````python 
def swap_case(s):
    return s.swapcase()
if __name__ == '__main__':
    s = input()
    result = swap_case(s)
    print(result)
 ````
 
 ````python
 txt = "HackerRank.com presents "Pythonist 2".
 x = txt.swapcase()

print(x)

````
 
 ### >> 12.  Divida a linha em um delimitador (espacial) e junte-se usando um hífen. " "-
 
 ````python
 def split_and_join(line):
  line = line.split(" ")
  line = "-".join(line)
  return line
````

### >> 13. Neste desafio, o usuário entra em uma string e um substring. Você tem que imprimir o número de vezes que o substramento ocorre na sequência dada. A travessia das cordas ocorrerá da esquerda para a direita, não da direita para a esquerda.

````python
def count_substring(string, sub_string):
    counter = 0 
    for i, letters in enumerate(string):
        if sub_string in string[i: i + len(sub_string)]:
            counter += 1
            
    return counter  
````
### >> 14. Leia uma determinada sequência, altere o caractere em um determinado índice e, em seguida, imprima a sequência modificada.

````python
def mutate_string(string, position, character):
    return string[:position]+character+string[position+1:]
    

if __name__ == '__main__':

````
### >>  15.  ![image](https://user-images.githubusercontent.com/95362045/175352295-211c00d8-3682-40a1-bfa8-5f6bcdf4eb8a.png)

````python
import math
import os
import random
import re
import sys


if __name__ == '__main__':
    n = int(input().strip())

    if n%2 != 0:
        print("Weird")
    else:
        if n>=2 and n<=5:
            print("Not Weird")
        elif n>=6 and n<=20:
            print("Weird")
        else:
            print("Not Weird")
            
````

### >> 16. O código fornecido lê dois inteiros do STDIN e . Adicione código para imprimir três linhas onde: 

1.	A primeira linha contém a soma dos dois números. ab
2.	A segunda linha contém a diferença dos dois números (primeiro - segundo).
3.	A terceira linha contém o produto dos dois números.

````python
a = int(input())
b = int(input())

print('{0} \n{1} \n{2}'.format((a + b), (a - b), (a * b)))

````

### >> 17.  O código fornecido será lido em um dicionário contendo pares de nomes de chave/valor:[marcas] para uma lista de alunos. Imprima a média da matriz de notas para o nome do aluno fornecido, mostrando 2 lugares após o decimal.

````python
if __name__ == '__main__':
    n = int(input())
    student_marks = {}
    for _ in range(n):
        name, *line = input().split()
        scores = list(map(float, line))
        student_marks[name] = scores
    query_name = input()

    if query_name in student_marks:
        x = ((float(student_marks[query_name][0]) + float(student_marks[query_name][1]) + float(student_marks[query_name][2])) / 3)
    
    print('%.2f' % x)
    
````

### >> 18.  Sua tarefa é descobrir se a sequência contém: caracteres alfanuméricos, caracteres alfabéticos, dígitos, caracteres minúsculas e maiústicos

````python

if __name__ == '__main__':
   s = input ()
   print(any(a.isalnum() for a in s))
   print(any(a.isalpha() for a in s))
   print(any(a.isdigit() for a in s))
   print(any(a.islower() for a in s))
   print(any(a.isupper() for a in s))
   
````

### >> 19.  Sua tarefa é envolver a sequência em um parágrafo de largura. 
Descrição da função
Complete a função de envoltório no editor abaixo.
o wrap tem os seguintes parâmetros:
•	corda de corda: uma corda longa
•	int max_width: a largura para embrulhar
Retorna
•	string: uma única sequência com caracteres newline ('\n') onde as quebras devem ser

````python

import textwrap
def wrap(string, max_width):
    wrapper = textwrap.TextWrapper(width=max_width) 
    dedented_text = textwrap.dedent(text=string) 
    result = wrapper.fill(text=dedented_text) 
    return result

if __name__ == '__main__':

````

### >> 20.  Você recebe um código parcial que é usado para gerar o logotipo hackerRank de espessura variável.
Sua tarefa é substituir o em branco () por rjust, ljust ou centro.______

````python

#Replace all ______ with rjust, ljust or center. 

thickness = int(input()) #This must be an odd number
c = 'H'

#Top Cone
for i in range(thickness):
    print((c*i).rjust(thickness-1)+c+(c*i).ljust(thickness-1))

#Top Pillars
for i in range(thickness+1):
    print((c*thickness).center(thickness*2)+(c*thickness).center(thickness*6))

#Middle Belt
for i in range((thickness+1)//2):
    print((c*thickness*5).center(thickness*6))    

#Bottom Pillars
for i in range(thickness+1):
    print((c*thickness).center(thickness*2)+(c*thickness).center(thickness*6))    

#Bottom Cone
for i in range(thickness):
    print(((c*(thickness-i-1)).rjust(thickness)+c+(c*(thickness-i-1)).ljust(thickness)).rjust(thickness*6))
    
````

### >> 21. Vincent trabalha em uma empresa de fabricação de tapetes. Um dia, ele projetou um novo tapete de porta com as seguintes especificações: 

O tamanho do tapete deve ser X. ( é um número natural ímpar, e é vezes .)
O design deve ter 'WELCOME' escrito no centro.
O padrão de design só deve ser usado , e caracteres.|.-

````python

n, m = map(int,input().split())
pattern = [('.|.'*(2*i + 1)).center(m, '-') for i in range(n//2)]
print('\n'.join(pattern + ['WELCOME'.center(m, '-')] + pattern[::-1]))

````

### >> 22.  Dado um inteiro, imprima os seguintes valores para cada inteiro

1.	Decimal
2.	Octal
3.	Hexadecimal (capitalized)
4.	Binary

````python 

def print_formatted(number):
    num = len(bin(number))-1
    for i in range(1,number+1):
        print("{0:{m}d}{0:{n}o}{0:{n}X}{0:{n}b}".format(i,m=num-1,n=num))
        
````

### >>  23. Você recebe um inteiro, . Sua tarefa é imprimir um rangoli de alfabeto de tamanho. (Rangoli é uma forma de arte folclórica indiana baseada na criação de padrões.)

````python 

def print_rangoli(size):
    alpha = "abcdefghijklmnopqrstuvwxyz"
    data = [alpha[i] for i in range(n)]
    items = list(range(n))
    items = items[:-1]+items[::-1]
    for i in items:
        temp = data[-(i+1):]
        row = temp[::-1]+temp[1:]
        print("-".join(row).center(n*4-3, "-"))

if __name__ == '__main__':

````
### >> 24. Você é solicitado a garantir que o primeiro e o sobrenome das pessoas comecem com uma letra maiúscula em seus passaportes. Por exemplo, deve ser capitalizado corretamente como .alison heckAlison Heck 
Alison heck  Alison Heck

````python

#!/bin/python3

import math
import os
import random
import re
import sys

# Complete the solve function below.
def solve(s):
    for x in s[:].split():
        s = s.replace(x, x.capitalize())
    return s
if __name__ == '__main__':

````

### >> 25. Você recebe duas listas e. Sua tarefa é calcular seu produto cartesiano abaxb

````python

from itertools import product

a = list(map(int, input().split()))
b = list(map(int, input().split()))

print(*product(a, b))

````
### >> 26. Você recebe uma corda. 
 Sua tarefa é imprimir todas as permutações possíveis do tamanho da corda em ordem lexicográfica.

````python

from itertools import permutations
s,n = input().split()
print(*[''.join(i) for i in permutations(sorted(s),int(n))],sep='\n')

````

### >> 26. (Introduction to sets) 

Agora, vamos usar nosso conhecimento de conjuntos e ajudar Mickey. 
Gabriel Williams é professora de botânica no District College. Um dia, ela pediu ao seu aluno Mickey para calcular a média de todas as plantas com alturas distintas em sua estufa.

Fórmula utilizada:

![image](https://user-images.githubusercontent.com/95362045/176011301-71cc347b-f499-4d2c-b884-2d5411ddd71d.png)

````python

def average(array):
    return sum(set(array))/len(set(array))
    
````

### >> 27. (Introduction to sets) -> symmetric difference 

Dado conjuntos de inteiros, e , imprima sua diferença simétrica na ordem ascendente. O termo diferença simétrica indica os valores que existem em ambos ou mas não existem em ambos.

Formato de entrada

 - A primeira linha de entrada contém um inteiro, . 
 - A segunda linha contém inteiros separados pelo espaço. 
 - A terceira linha contém um inteiro, . 
 - A quarta linha contém inteiros separados pelo espaço.

````python

a,b = [set(input().split()) for _ in range(4)][1::2]
print('\n'.join(sorted(a^b, key=int)))

````

### >> 28. Input() 

Você recebe um polinômial de um único indeterminado (ou variável),
Você também recebe os valores de e . Sua tarefa é verificar se . pxxkP(x) = k

````python 

ui = input().split()
x = int(ui[0])
print(eval(input()) == int(ui[1]))

````

### >> 30. Sets (Set.add())

Aplique seu conhecimento sobre a operação .add()para ajudar seu amigo Rupal. Rupal tem uma enorme coleção de selos do país. Ela decidiu contar o número total de selos de país distintos em sua coleção. Ela pediu sua ajuda. Você escolhe os selos um a um de uma pilha de selos do país. Encontre o número total de selos de país distintos.

````python

a = set()
[a.add(input()) for _ in range(int(input()))]
print(len(a))

````

### >> 31. Sets (Set.discard(), .remove() & .pop()

Você tem um conjunto não vazio, e você tem que executar comandos dados em linhas.

Os comandos serão pop, remover e descartar.

````python

num = int(input())
data = set(map(int, input().split()))
operations = int(input())

for x in range(operations):
  oper = input().split()
  if oper[0] == "remove":
    data.remove(int(oper[1]))
  elif oper[0] == "discard":
    data.discard(int(oper[1]))
  else:
    data.pop()
    
print(sum(data))

````

### >> 32. Sets (Set .union() Operation)

Os alunos do District College têm assinaturas para jornais ingleses e franceses. Alguns estudantes assinaram apenas o inglês, alguns assinaram apenas francêse alguns assinaram ambos os jornais. 

Você recebe dois conjuntos de números de estudantes. Um conjunto assinou o jornal inglês, e o outro é subscrito pelo jornal francês. O mesmo aluno pode estar em ambos os sets. Sua tarefa é encontrar o número total de alunos que assinaram pelo menos um jornal.

````python

n = int(input())
l = list(input().split())
m = int(input())
k = list(input().split())

s1 = set(l)
s2 = set(k)

print(len(s1.union(s2)))

````

### >> 33. Sets (Set.intersection() Operation)

Os alunos do District College têm assinaturas para jornais ingleses e franceses. Alguns estudantes assinaram apenas o inglês, alguns assinaram apenas o francês, e alguns assinaram ambos os jornais. 

Você recebe dois conjuntos de números de estudantes. Um conjunto assinou o jornal inglês, um conjunto assinou o jornal francês. Sua tarefa é encontrar o número total de alunos que se inscreveram em ambos os jornais.

````python

num1, st1, num2, st2 = (set(input().split()) for i in range(4))
print(len(st1.intersection(st2)))

````

### >> 34. Set .difference() Operation

Os alunos do District College têm uma assinatura para jornais ingleses e franceses. Alguns estudantes assinaram apenas o jornal inglês, alguns assinaram apenas o jornal francês, e alguns assinaram ambos os jornais.

Você recebe dois conjuntos de números de estudantes. Um conjunto assinou o jornal inglês e um conjunto assinou o jornal francês Sua tarefa é encontrar o número total de estudantes que assinaram apenas jornais ingleses.

````python

n1 = int(input())
set_1 = set(map(int,input().split()))
n2 = int(input())
set_2 = set(map(int,input().split()))
print(len(set_1-set_2))

````

### >> 35. Set Mutations 

Você recebe um conjunto e um número de outros conjuntos. Esses conjuntos devem realizar algumas operações específicas de mutação no set .

Sua tarefa é executar essas operações e imprimir a soma de elementos do conjunto .

````python

if __name__ == '__main__':
    (_, A) = (int(input()),set(map(int, input().split())))
    B = int(input())
    for _ in range(B):
        (command, newSet) = (input().split()[0],set(map(int, input().split())))
        getattr(A, command)(newSet)

    print (sum(A))
    
````

### >> 36. Set .symmetric_difference() Operation

Os alunos do District College têm assinaturas para jornais ingleses e franceses. Alguns estudantes assinaram apenas o inglês, alguns assinaram apenas o francês, e alguns assinaram ambos os jornais.

Você recebe dois conjuntos de números de estudantes. Um conjunto assinou o jornal inglês, e um conjunto assinou o jornal francês. Sua tarefa é encontrar o número total de estudantes que assinaram o jornal inglês ou francês, mas não ambos

```python

n1=input()
li1 = input().split()
s1 = set(li1)
n2=input()
li2 = input().split()
s2 = set(li2)
s1s2 = s1.symmetric_difference(s2)
print(len(s1s2))

````

### >> 37. HTML Parser - Part 1

Você recebe um trecho de código HTML de linhas.
Sua tarefa é imprimir tags de partida, etiquetas finais e tags vazias separadamente. 

Formatar seus resultados da seguinte forma:

![image](https://user-images.githubusercontent.com/95362045/177833900-39d377b8-9ee2-412e-bafb-637b1e6b5312.png)

````python from html.parser import HTMLParser
def read_int(): return int(input())
def read_int_words(): return map(int,input().split())
def pa(a):
    for ai in a:
        (k,v) = ai
        print("->",k.strip(),">",str(v).strip())
class MyHTMLParser(HTMLParser):
    def handle_starttag(self, tag, attrs):
        print("Start :", tag.strip())
        pa(attrs)
    def handle_endtag(self, tag): print("End   :",tag.strip())
    def handle_startendtag(self, tag, attrs):
        print("Empty :", tag.strip())
        pa(attrs)
n = int(input())
parser = MyHTMLParser()
for i in range(n): parser.feed(input())

````

### >> 38. Map and Lambda Function

![image](https://user-images.githubusercontent.com/95362045/177857419-2f913192-b34a-4811-9c3a-7e34b6bbb20a.png)

````python 
cube = lambda x: pow(x,3)# complete the lambda function 
def fibonacci(n):
    # return a list of fibonacci numbers
    lis = [0,1]
    for i in range(2,n):
        lis.append(lis[i-2] + lis[i-1])
    return(lis[0:n])
````

### >> 39.  Concatenar

Você recebe duas matrizes inteiros de tamanho X e X ( e são linhas, e é a coluna). Sua tarefa é concatenar as matrizes ao longo do eixo

![image](https://user-images.githubusercontent.com/95362045/177858398-80205ad5-7604-46c3-9f97-99ada0503687.png)

````python 

import numpy as np
a, b, c = map(int,input().split())
arrA = np.array([input().split() for _ in range(a)],int)
arrB = np.array([input().split() for _ in range(b)],int)
print(np.concatenate((arrA, arrB), axis = 0))

````

### >> 40. Errors and Exceptions

Você recebe dois valores A e B
Executar divisão de inteiros A e B e imprimir 

````python 


for i in range(int(input())):

    try:
        valor1,valor2=map(int,input().split())
        print(valor1//valor2)
    except Exception as e:
        print("Error Code:", e)
            
````

### >> 41. Errors and ExceptionsIncorrect Regex

Voce recebe uma string S, sua tarefa e descobrir se é um regex válido ou não

![image](https://user-images.githubusercontent.com/95362045/178010126-88d94631-3640-449d-8046-b5c94aa77ed7.png)

````python

import re
for _ in range(int(input())):
    ans = True
    try:
        reg = re.compile(input())
    except re.error:
        ans = False
    print(ans)
    
````

### >> 42. ItertoolsIterables and Iterators

![image](https://user-images.githubusercontent.com/95362045/178016601-a8a91dc7-6c88-4dc0-b060-24eee888f64e.png)


````python
from itertools import combinations

N = int(input())
L = input().split()
K = int(input())

C = list(combinations(L, K))
F = filter(lambda c: 'a' in c, C)
print("{0:.3}".format(len(list(F))/len(C)))

````

### >> 43. Built-InsZipped!

A Universidade Nacional realiza um exame de alunos em disciplinas.
Sua tarefa é calcular as pontuações médias de cada aluno.

````python

n, x = map(int, input().split()) 

sheet = []
for _ in range(x):
    sheet.append( map(float, input().split()) ) 

for i in zip(*sheet): 
    print( sum(i)/len(i) )
    
````

### >> 44. Built-InsPython Evaluation

Você recebe uma expressão em uma linha. Leia essa linha como uma variável de string, como var, e imprima o resultado usando eval(var).

````python

leo = input()
eval(leo)

````

### >> 45. Você recebe uma lista separada de inteiros. Se todos os inteiros são positivos, então você precisa verificar se algum inteiro é um inteiro palindômico.

````python

N,n = int(input()),input().split()
print(all([int(i)>0 for i in n]) and any([j == j[::-1] for j in n]))

````

### >> 46. Built-InsginortS

![image](https://user-images.githubusercontent.com/95362045/178313513-a4d513ff-12ee-4763-87e9-b2c795913c01.png)

````python

def f(c):
    code = 0
    if c.isupper():
        code = 10 ** 3
    elif c.isdigit():
        code = 10 ** 6
        if ord(c) % 2 == 0:
            code = 10 ** 9
    return code + ord(c)

print(*sorted(input(), key=lambda c: f(c)), sep='')

````

### >> 47. MathMod Divmod

![image](https://user-images.githubusercontent.com/95362045/178746213-699fc675-5002-4fee-a66c-a193302c024b.png)

````python
a = int(input())
b = int(input())

print(a//b)
print(a%b)
print(divmod(a,b))

````

### >> 48. Power - Mod Power

![image](https://user-images.githubusercontent.com/95362045/178750284-0a94c42e-4ad4-43fa-910e-dd49f598ec9d.png)

````python 

a = int(input())
b = int(input())
c = int(input())

print(pow(a,b))
print(pow(a,b,c))

````



