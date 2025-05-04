# python
Python é uma linguagem de programação poderosa e versátil, ideal para iniciantes e amplamente usada por profissionais. Vamos explorar seus conceitos fundamentais:

## 1. Variáveis e Tipos de Dados
Em Python, você não declara o tipo da variável explicitamente - o tipo é inferido automaticamente.

```python
# Tipos básicos
inteiro = 10             # int
flutuante = 10.5         # float
texto = "Olá, Python!"  # str
booleano = True          # bool (True ou False)

# Tipos complexos
lista = [1, 2, 3]        # list
tupla = (1, 2, 3)        # tuple (imutável)
dicionario = {"chave": "valor"}  # dict
conjunto = {1, 2, 3}     # set (elementos únicos)
```
## 2. Estruturas Condicionais (if, elif, else)
```python
idade = 18

if idade < 12:
    print("Criança")
elif idade < 18:
    print("Adolescente")
else:
    print("Adulto")
```
## 3. Loops (for e while)
### Loop for
```python
# Iterando sobre uma lista
frutas = ["maçã", "banana", "laranja"]
for fruta in frutas:
    print(fruta)

# Usando range()
for i in range(5):       # 0 a 4
    print(i)

for i in range(2, 6):    # 2 a 5
    print(i)

for i in range(0, 10, 2): # 0, 2, 4, 6, 8
    print(i)
```
### Loop while
```python
contador = 0
while contador < 5:
    print(contador)
    contador += 1
```
## 4. Funções
```python
# Função básica
def saudacao(nome):
    return f"Olá, {nome}!"

# Chamando a função
print(saudacao("Maria"))

# Função com parâmetros padrão
def potencia(base, expoente=2):
    return base ** expoente

print(potencia(3))    # 9 (3^2)
print(potencia(3, 3)) # 27 (3^3)

# Função com número variável de argumentos
def soma(*numeros):
    total = 0
    for num in numeros:
        total += num
    return total

print(soma(1, 2, 3, 4))  # 10
```
## 5. Listas e Operações Comuns
```python
numeros = [1, 2, 3, 4, 5]

# Acessando elementos
primeiro = numeros[0]      # 1
ultimo = numeros[-1]       # 5

# Fatiamento (slicing)
parte = numeros[1:4]       # [2, 3, 4]

# Métodos úteis
numeros.append(6)          # [1, 2, 3, 4, 5, 6]
numeros.insert(0, 0)       # [0, 1, 2, 3, 4, 5, 6]
numeros.remove(3)          # Remove o valor 3
valor = numeros.pop()      # Remove e retorna o último (6)
numeros.sort()             # Ordena a lista
numeros.reverse()          # Inverte a ordem
```
## 6. Dicionários
```python
pessoa = {
    "nome": "João",
    "idade": 30,
    "cidade": "São Paulo"
}

# Acessando valores
print(pessoa["nome"])      # João
print(pessoa.get("idade")) # 30

# Adicionando/alterando
pessoa["email"] = "joao@exemplo.com"
pessoa["idade"] = 31

# Métodos úteis
chaves = pessoa.keys()     # Retorna as chaves
valores = pessoa.values()  # Retorna os valores
itens = pessoa.items()     # Retorna pares (chave, valor)
```
## 7. Manipulação de Strings
```python
texto = "Python é incrível"

# Métodos úteis
maiusculo = texto.upper()      # "PYTHON É INCRÍVEL"
minusculo = texto.lower()      # "python é incrível"
dividido = texto.split()       # ["Python", "é", "incrível"]
substituido = texto.replace("incrível", "poderoso")

# Formatação
nome = "Ana"
idade = 25
mensagem = f"{nome} tem {idade} anos"  # f-string (Python 3.6+)
```
## 8. Tratamento de Exceções
```python
try:
    resultado = 10 / 0
except ZeroDivisionError:
    print("Não é possível dividir por zero!")
except Exception as e:
    print(f"Ocorreu um erro: {e}")
else:
    print("Tudo ocorreu bem!")
finally:
    print("Este bloco sempre é executado")
```
## 9. Trabalhando com Arquivos
```python
# Escrevendo em um arquivo
with open("arquivo.txt", "w") as arquivo:
    arquivo.write("Olá, Python!\n")

# Lendo de um arquivo
with open("arquivo.txt", "r") as arquivo:
    conteudo = arquivo.read()
    print(conteudo)
```
## 10. Módulos e Bibliotecas
Python vem com uma ampla biblioteca padrão e permite instalar bibliotecas adicionais.

### Importando módulos
```python
# Importando todo o módulo
import math
print(math.sqrt(16))  # 4.0

# Importando funções específicas
from random import randint
print(randint(1, 10))  # Número aleatório entre 1 e 10

# Importando com alias
import numpy as np
```
Bibliotecas populares:
- NumPy: Computação científica
- Pandas: Manipulação de dados
- Matplotlib: Visualização de dados
- Requests: Requisições HTTP
- Django/Flask: Desenvolvimento web

## 11. Programação Orientada a Objetos
```python
class Pessoa:
    # Método construtor
    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade
    
    # Método de instância
    def apresentar(self):
        return f"Meu nome é {self.nome} e tenho {self.idade} anos."

# Criando objeto
p1 = Pessoa("Carlos", 40)
print(p1.apresentar())
```
## 12. Expressões Lambda
Funções anônimas de uma linha:

```python
dobro = lambda x: x * 2
print(dobro(5))  # 10

# Usando com map()
numeros = [1, 2, 3, 4]
quadrados = list(map(lambda x: x**2, numeros))
print(quadrados)  # [1, 4, 9, 16]
```
## 13. List Comprehensions
Forma concisa de criar listas:

```python
# Lista de quadrados
quadrados = [x**2 for x in range(10)]
print(quadrados)  # [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

# Com condição
pares = [x for x in range(20) if x % 2 == 0]
print(pares)  # [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
```
## 14. Geradores
Produzem valores sob demanda, economizando memória:

```python
def gerador_pares(max):
    n = 0
    while n < max:
        yield n
        n += 2

for num in gerador_pares(10):
    print(num)  # 0, 2, 4, 6, 8
```
## 15. Decoradores
Modificam o comportamento de funções:

```python
def meu_decorador(funcao):
    def wrapper():
        print("Antes da função")
        funcao()
        print("Depois da função")
    return wrapper

@meu_decorador
def diga_ola():
    print("Olá!")

diga_ola()
# Saída:
# Antes da função
# Olá!
# Depois da função
```
Este guia cobre os conceitos fundamentais do Python. Para se aprofundar, recomendo:

1. Praticar regularmente com pequenos projetos
2.Explorar a documentação oficial do Python
3.Experimentar bibliotecas populares para áreas de seu interesse
4.Participar de comunidades Python para tirar dúvidas
