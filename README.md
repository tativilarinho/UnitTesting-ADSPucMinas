# Análise e Desenvolvimento de Sisitema - PUC Minas
#Disciplina Qualidade de Software e Testes 
#Módulo: Testes de Unidade 

Este documento descreve a suíte de testes unitários para o módulo `greeting.js`. Os testes foram escritos para garantir que a função responsável por dar as boas-vindas aos alunos funcione corretamente e trate entradas inválidas de forma segura.

## 🛠️ Tecnologias Utilizadas

* **JavaScript** (Node.js)
* **Framework de Testes:** Jest

## 🎯 Objetivo dos Testes

A suíte de testes, nomeada como **"Saudação"**, verifica o comportamento da função `greet()` importada do arquivo `./greeting.js`. Ela garante que a função retorne a mensagem correta quando recebe dados válidos e dispare erros em cenários de dados ausentes.

## 🧪 Casos de Teste Abordados

A suíte cobre os seguintes cenários:

1.  **Saudação com nome válido (Caminho Feliz):**
    * **Descrição:** Verifica se a função retorna a string de boas-vindas formatada corretamente quando um nome é fornecido.
    * **Entrada Exemplo:** `'Tati'`
    * **Retorno Esperado:** `'Olá Tati, seja bem vindo ao curso de Desenvolvimento WEB'`

2.  **Tratamento de string vazia:**
    * **Descrição:** Garante que a função não aceite strings vazias como nome.
    * **Entrada:** `''`
    * **Comportamento Esperado:** Lançar uma exceção (`throw`).

3.  **Tratamento de valores indefinidos (Undefined):**
    * **Descrição:** Garante que a função não quebre silenciosamente caso seja chamada sem nenhum argumento.
    * **Entrada:** `()` *(nenhum parâmetro)*
    * **Comportamento Esperado:** Lançar uma exceção (`throw`).

## 🚀 Como Executar

Certifique-se de ter as dependências instaladas (`npm install`). Para rodar este teste especificamente, utilize o comando:

```bash
npx jest greeting.spec.js
