# 📘 Assignment: Automated Testing with pytest

## 🎯 Objective

Aprenda a escrever e executar testes automatizados em Python com `pytest`. Você vai verificar resultados esperados, testar casos de borda e usar falhas para encontrar erros no código.

## 📝 Tasks

### 🛠️ Configure o pytest e teste uma função

#### Description

Crie `calculadora.py` com uma função `somar(a, b)` e `test_calculadora.py` com testes para ela. Instale o `pytest` com `python -m pip install pytest` e execute os testes com `python -m pytest`.

#### Requirements

O programa concluído deve:

- Definir `somar(a, b)` em `calculadora.py`.
- Incluir pelo menos três testes em `test_calculadora.py`, cobrindo soma de números positivos, negativos e zero.
- Fazer todos os testes passarem ao executar `python -m pytest`.

### 🛠️ Teste erros e casos de borda

#### Description

Adicione a função `dividir(a, b)` e escreva testes para uma divisão comum e para a tentativa de dividir por zero. Use `pytest.raises` para verificar a exceção.

#### Requirements

O programa concluído deve:

- Definir `dividir(a, b)` em `calculadora.py`.
- Retornar o resultado correto para uma divisão comum.
- Gerar `ZeroDivisionError` quando o divisor for zero e verificar esse comportamento em um teste.

### 🛠️ Verifique limites e rode a suíte completa

#### Description

Adicione `nota_aprovada(nota)`, que retorna `True` para notas a partir de 60 e `False` para notas menores. Teste os valores imediatamente abaixo, no limite e acima dele; corrija a função se algum teste revelar um erro.

#### Requirements

O programa concluído deve:

- Definir `nota_aprovada(nota)` em `calculadora.py`.
- Testar as notas 59, 60 e 61, incluindo a regra de que 60 é suficiente para aprovação.
- Executar `python -m pytest` e deixar todos os testes passando.
