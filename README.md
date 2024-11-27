Aqui está uma handbook básica sobre **paradigmas de programação** com explicações e exemplos de código para os paradigmas mais comuns:

---

### **1. Paradigma Imperativo**
O paradigma imperativo foca em *como* resolver um problema, especificando uma sequência de instruções que o computador deve seguir.

**Exemplo em Python:**
```python
# Calcular a soma dos números de 1 a 10
soma = 0
for i in range(1, 11):
    soma += i
print(soma)
```

---

### **2. Paradigma Funcional**
O paradigma funcional trata a computação como a avaliação de funções matemáticas, evitando o uso de estados mutáveis.

**Exemplo em Python:**
```python
# Calcular a soma dos números de 1 a 10
from functools import reduce

soma = reduce(lambda x, y: x + y, range(1, 11))
print(soma)
```

---

### **3. Paradigma Orientado a Objetos**
Esse paradigma organiza o código em objetos que possuem atributos (dados) e métodos (comportamentos).

**Exemplo em Python:**
```python
# Classe que representa uma Conta Bancária
class ContaBancaria:
    def __init__(self, saldo=0):
        self.saldo = saldo

    def depositar(self, valor):
        self.saldo += valor

    def sacar(self, valor):
        if valor <= self.saldo:
            self.saldo -= valor
        else:
            print("Saldo insuficiente!")

# Criando uma conta e operando nela
conta = ContaBancaria()
conta.depositar(100)
conta.sacar(30)
print(conta.saldo)
```

---

### **4. Paradigma Declarativo**
O paradigma declarativo foca em *o que fazer*, deixando para o sistema decidir *como fazer*.

**Exemplo em SQL:**
```sql
-- Selecionar todos os clientes de uma tabela cujo saldo é maior que 1000
SELECT * FROM clientes WHERE saldo > 1000;
```

**Exemplo em Python (list comprehension):**
```python
# Filtrar números pares de uma lista
numeros = range(1, 11)
pares = [n for n in numeros if n % 2 == 0]
print(pares)
```

---

### **5. Paradigma Lógico**
Nesse paradigma, você define fatos e regras, e o sistema resolve o problema com base na lógica.

**Exemplo em Prolog:**
```prolog
% Fatos
pai(joao, maria).
pai(joao, jose).

% Regra
irmao(X, Y) :- pai(P, X), pai(P, Y), X \= Y.

% Consultar
% ?- irmao(maria, jose).
% true.
```

---

### **6. Paradigma Event-Driven (Baseado em Eventos)**
Esse paradigma é baseado na execução de código em resposta a eventos, como cliques ou mensagens.

**Exemplo em JavaScript:**
```javascript
// Evento de clique em um botão
document.getElementById("meuBotao").addEventListener("click", function() {
    alert("Botão clicado!");
});
```

---

### **7. Paradigma Concorrente**
Permite a execução de várias partes de um programa simultaneamente.

**Exemplo em Python (usando threading):**
```python
import threading

def tarefa(nome):
    print(f"Iniciando tarefa: {nome}")

# Criando threads
t1 = threading.Thread(target=tarefa, args=("Tarefa 1",))
t2 = threading.Thread(target=tarefa, args=("Tarefa 2",))

t1.start()
t2.start()

t1.join()
t2.join()
```

---

### **Resumo**
| Paradigma             | Foco Principal                                  | Exemplo Simples                  |
|-----------------------|------------------------------------------------|----------------------------------|
| Imperativo            | Sequência de instruções                        | `for` loops                     |
| Funcional             | Funções imutáveis e puras                      | `map`, `reduce`, etc.           |
| Orientado a Objetos   | Objetos com atributos e métodos                 | Classes e objetos               |
| Declarativo           | Descrever o problema, não como resolvê-lo       | SQL, list comprehensions        |
| Lógico                | Fatos e regras                                 | Prolog                          |
| Event-Driven          | Responder a eventos                            | Listeners em JavaScript         |
| Concorrente           | Executar múltiplas tarefas simultaneamente     | Multithreading                  |

Se quiser explorar mais algum desses paradigmas, é só avisar! 😊