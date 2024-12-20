# Cartão de Crédito - Sistema de Controle de Compras

Este projeto em Java implementa um sistema simples para gerenciar compras realizadas com um cartão de crédito, controlando o saldo disponível, listando as compras realizadas e classificando-as por valor.

## Funcionalidades
- Registrar compras, verificando se o saldo é suficiente.
- Exibir uma lista de compras realizadas, ordenadas pelo valor.
- Exibir o saldo restante do cartão de crédito.

## Estrutura do Projeto
O projeto possui as seguintes classes:

### 1. `CartaoDeCredito`
Classe que representa o cartão de crédito. Contém:
- Atributos:
  - `limite`: Limite total do cartão.
  - `saldo`: Saldo disponível.
  - `compras`: Lista de compras realizadas.
- Métodos:
  - `lancaCompra(Compra compra)`: Registra uma compra, descontando o valor do saldo caso haja limite suficiente.
  - Getters para `limite`, `saldo` e `compras`.

### 2. `Compra`
Classe que representa uma compra. Contém:
- Atributos:
  - `descricao`: Descrição da compra.
  - `valor`: Valor da compra.
- Métodos:
  - `toString()`: Representação textual de uma compra.
  - `compareTo(Compra outraCompra)`: Compara duas compras pelo valor.

### 3. `Main`
Classe principal que implementa a interação com o usuário via console.
- Solicita o limite inicial do cartão.
- Permite registrar compras até que o saldo acabe ou o usuário decida sair.
- Lista as compras realizadas ordenadas por valor.
- Exibe o saldo final do cartão.

## Como Executar
1. Certifique-se de ter o [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-jdk-downloads.html) instalado.
2. Compile as classes:
   ```bash
   javac CartaoDeCredito.java Compra.java Main.java
   ```
3. Execute a classe `Main`:
   ```bash
   java Main
   ```
4. Siga as instruções exibidas no console para registrar compras e visualizar o saldo.

## Exemplo de Uso
```plaintext
Digite o limite do cartão:
500.0
Digite a descrição da compra:
Supermercado
Digite o valor da compra:
150.0
Compra realizada!
Digite 0 para sair ou 1 para continuar
1
Digite a descrição da compra:
Farmácia
Digite o valor da compra:
50.0
Compra realizada!
Digite 0 para sair ou 1 para continuar
0
***********************
COMPRAS REALIZADAS:

Farmácia - 50.0
Supermercado - 150.0

***********************

Saldo do cartão: 300.0
```

## Melhorias Futuras
- Adicionar suporte para persistência de dados.
- Implementar interface gráfica (GUI).
- Permitir remoção ou edição de compras registradas.





