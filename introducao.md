# Aprenda Python: Básico, Intermediário e Avançado

Vou te guiar pelo aprendizado de Python em três níveis. Vamos começar!

## Nível Básico

### 1. Introdução ao Python
Python é uma linguagem de programação interpretada, de alto nível e multiparadigma.

### 2. Instalação
Baixe em [python.org](https://www.python.org/) ou use ambientes online como Replit, Colab.

### 3. Primeiros Passos

```python
# Comentários em Python
print("Olá, Mundo!")  # Saída: Olá, Mundo!
```

### 4. Variáveis e Tipos Básicos
```python
# Números
idade = 25             # inteiro
altura = 1.75          # float

# Texto
nome = "Maria"         # string
sobrenome = 'Silva'

# Booleanos
ativo = True           # ou False
```

### 5. Operadores
```python
# Aritméticos
5 + 3   # Soma
10 - 2  # Subtração
4 * 2   # Multiplicação
16 / 4  # Divisão
16 // 4 # Divisão inteira
2 ** 3  # Potência (8)

# Comparação
5 > 3   # True
5 == 5  # True
5 != 3  # True

# Lógicos
True and False  # False
True or False   # True
not True        # False
```

### 6. Estruturas Condicionais
```python
idade = 18

if idade < 12:
    print("Criança")
elif idade < 18:
    print("Adolescente")
else:
    print("Adulto")
```

### 7. Estruturas de Repetição
```python
# For loop
for i in range(5):  # 0 a 4
    print(i)

# While loop
contador = 0
while contador < 5:
    print(contador)
    contador += 1
```

## Nível Intermediário

### 1. Listas e Tuplas
```python
# Listas (mutáveis)
frutas = ["maçã", "banana", "laranja"]
frutas.append("uva")       # Adiciona item
frutas[1] = "morango"     # Altera item

# Tuplas (imutáveis)
coordenadas = (10.5, 20.3)
```

### 2. Dicionários
```python
pessoa = {
    "nome": "João",
    "idade": 30,
    "casado": False
}

print(pessoa["nome"])  # Acesso
pessoa["profissão"] = "Engenheiro"  # Adiciona
```

### 3. Funções
```python
def saudacao(nome):
    return f"Olá, {nome}!"

print(saudacao("Ana"))  # Olá, Ana!

# Parâmetros opcionais
def potencia(base, expoente=2):
    return base ** expoente

print(potencia(3))     # 9
print(potencia(3, 3))  # 27
```

### 4. Manipulação de Arquivos
```python
# Escrevendo
with open("arquivo.txt", "w") as f:
    f.write("Conteúdo do arquivo")

# Lendo
with open("arquivo.txt", "r") as f:
    conteudo = f.read()
    print(conteudo)
```

### 5. Tratamento de Exceções
```python
try:
    resultado = 10 / 0
except ZeroDivisionError:
    print("Divisão por zero!")
except Exception as e:
    print(f"Erro: {e}")
finally:
    print("Sempre executa")
```

### 6. List Comprehensions
```python
# Forma concisa de criar listas
quadrados = [x**2 for x in range(10)]
pares = [x for x in range(20) if x % 2 == 0]
```

## Nível Avançado

### 1. Programação Orientada a Objetos
```python
class Pessoa:
    # Construtor
    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade
    
    # Método
    def apresentar(self):
        print(f"Sou {self.nome} e tenho {self.idade} anos.")

# Herança
class Funcionario(Pessoa):
    def __init__(self, nome, idade, salario):
        super().__init__(nome, idade)
        self.salario = salario

    def aumentar_salario(self, percentual):
        self.salario *= (1 + percentual/100)
```

### 2. Decoradores
```python
def meu_decorador(funcao):
    def wrapper():
        print("Antes da função")
        funcao()
        print("Depois da função")
    return wrapper

@meu_decorador
def dizer_ola():
    print("Olá!")

dizer_ola()
```

### 3. Geradores
```python
def contador(maximo):
    n = 0
    while n < maximo:
        yield n  # Pausa a execução
        n += 1

for numero in contador(5):
    print(numero)
```

### 4. Módulos e Pacotes
```python
# Importando
import math
from datetime import datetime

# Criando módulos
# salvar como meu_modulo.py
def funcao_util():
    return "Função útil"

# Em outro arquivo:
# from meu_modulo import funcao_util
```

### 5. Trabalhando com APIs
```python
import requests

response = requests.get("https://api.github.com")
dados = response.json()
print(dados)
```

### 6. Threading e Multiprocessamento
```python
import threading

def tarefa():
    print("Executando tarefa")

thread = threading.Thread(target=tarefa)
thread.start()
```

### 7. Context Managers Personalizados
```python
class MeuContextManager:
    def __enter__(self):
        print("Entrando no contexto")
        return self
    
    def __exit__(self, exc_type, exc_val, exc_tb):
        print("Saindo do contexto")

with MeuContextManager() as cm:
    print("Dentro do contexto")
```

### 8. Metaprogramação
```python
# Criando classes dinamicamente
def criar_classe(nome):
    return type(nome, (), {})

MinhaClasse = criar_classe("MinhaClasse")
obj = MinhaClasse()
```

## Próximos Passos

1. **Projetos Práticos**: Comece a construir pequenos projetos
2. **Frameworks**: Explore Django (web), Flask (web), Pandas (dados)
3. **Testes**: Aprenda unittest ou pytest
4. **Padrões de Projeto**: Estude SOLID, Design Patterns
5. **Performance**: Aprenda sobre otimização de código

Quer que eu detalhe algum tópico específico ou tenha alguma dúvida sobre algum conceito?
