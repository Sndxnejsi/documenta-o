#  Estudos de Lógica de Programação com JavaScript

Este repositório contém uma coleção de exercícios e exemplos práticos para o aprendizado de JavaScript, cobrindo desde conceitos básicos de variáveis até manipulação de APIs e sistemas simples.

---

##  Índice de Arquivos

###  Condicionais (if, else, switch, ternário)

* **`condicional-1.js`**: Exemplo básico de estrutura condicional para verificar se uma pessoa é maior ou menor de idade.
* **`condicional-2.js`**: Demonstração de condicionais `if...else` e o uso do **Operador Ternário** para um código mais limpo.
* **`condicional-3.js`**: Uso de `if...else if` para múltiplas condições (classificação de notas escolares).
* **`condicional-4.js`**: Estrutura de repetição `switch` para identificar o estado correspondente a uma sigla (UF) da região sudeste.

###  Integração com API e Arquivos

* **`feriados.js`**: Script assíncrono que consome a [BrasilAPI](https://brasilapi.com.br/) para buscar feriados nacionais de um determinado ano e gera automaticamente um arquivo formatado em Markdown (`Feriados.md`).

###  Manipulação de Arrays e Listas

* **`idades.js`**: Algoritmo que filtra um grupo de pessoas entre maiores e menores de idade, calculando a soma das idades e listando os nomes separadamente.
* **`lista-alunos.js`**: Separa alunos em grupos de "Aprovados" e "Reprovados" com base em suas notas, exibindo a contagem final de cada grupo.
* **`lista-compras.js`**: Exemplo de como percorrer arrays utilizando laços `for` e o método `forEach`, exibindo itens numerados.
* **`objeto-1.js`**: Introdução a objetos literais em JavaScript, mostrando como estruturar dados de forma organizada (propriedades e valores).

###  Interatividade e Lógica

* **`ímpar-ou-par.js`**: Script interativo via terminal (utilizando `readline`) que recebe um número do usuário e informa se ele é Par ou Ímpar.
* **`jogo.js`**: Um jogo de "Adivinhe o Número". O programa gera um valor aleatório e dá dicas (Muito alto/Muito baixo) até que o usuário acerte, contando o número de tentativas.
* **`logica.js`**: Arquivo de referência geral contendo:
    * Declaração de variáveis (`const`, `let`, `var`).
    * Verificação de tipos de dados (`typeof`).
    * Funções para verificação de par/ímpar.
    * Laços de repetição aninhados para gerar uma **Tabuada completa**.

---

##  Tecnologias Utilizadas

- **JavaScript (Node.js)**
- **Módulo Readline**: Para interação via terminal.
- **Módulo FS (File System)**: Para gravação de arquivos locais.
- **Fetch API**: Para consumo de dados externos.

---

##  Como Executar

Certifique-se de ter o [Node.js](https://nodejs.org/) instalado. No terminal, execute:

```bash
node nome-do-arquivo.js