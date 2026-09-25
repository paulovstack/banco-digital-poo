[README.md](https://github.com/user-attachments/files/32522589/README.md)
# DevBank

Sistema bancário simples em Python, simulando as operações de um aplicativo de banco digital: o usuário faz seu cadastro e pode realizar depósitos e saques a partir do saldo disponível em conta.

## Funcionalidades

- Cadastro inicial do titular da conta
- Consulta de saldo
- Depósito de valores
- Saque de valores (com verificação de saldo suficiente)
- Menu interativo via terminal, com feedback visual (mensagens coloridas e simulação de carregamento)

## Conceitos praticados

Esse projeto foi minha forma de praticar Programação Orientada a Objetos (POO) em Python, principalmente:

- **Herança**: a classe `Conta` herda de `Depositar` e `Sacar`, que por sua vez herdam de `ContaBancaria` — isso evita repetir código, já que cada classe especializada só implementa o comportamento que é específico dela.
- **Encapsulamento**: os atributos da conta (`_titular`, `_saldo`) são protegidos (prefixo `_`), como forma de indicar que não devem ser alterados diretamente de fora da classe, e sim através dos métodos definidos (como `depositar` e `sacar`).
- Estruturas de controle (`while`, `if/elif/else`) para o menu e a lógica de cada operação.
- Formatação de saída no terminal, incluindo cores (ANSI escape codes) para melhorar a experiência do usuário.

## Como executar

```bash
python main.py
```

O programa vai pedir seu nome e CPF (simulado, não valida formato real), criar sua conta com saldo inicial zerado, e abrir o menu com as opções de depósito, saque e saída.

## Tecnologias

- Python 3
- Bibliotecas padrão: `time`, `os`

## Próximos passos

- Persistência de dados (salvar conta em arquivo, para não perder o saldo ao fechar o programa)
- Validação real de CPF
- Extrato de operações realizadas
