# Documentação | gqs-algoritmo-01-py
**Aluno:** Caio Ferreira Menezes<br>
**RA:** 4251923922

## Objetivo do Algoritmo
Este algoritmo é um verificador de Palíndromo e frase invertida, seu papel é remover todo caractere especial e letra maiúscula, além de verificar se a frase é a mesma quando invertida.
## Funcionamento
O código realiza o papel de validar se uma frase é um palíndromo, ou seja, se ela permanece igual quando lida de trás para frente. O processo acontece em três etapas, dentro da função `analisar`:

1. **Tratamento de valor nulo:** se a entrada for `None`, a função retorna `False` imediatamente, evitando erros no processamento seguinte.
2. **Limpeza da string:** utilizando a biblioteca `re` (expressões regulares), o comando `re.sub(r'[^a-zA-Z0-9]', '', entrada)` remove espaços, pontuação e qualquer caractere que não seja letra ou número. Em seguida, `.lower()` converte todo o texto para minúsculas, garantindo que a comparação não seja afetada por maiúsculas/minúsculas.
3. **Inversão e comparação:** a string limpa é invertida com fatiamento (`[::-1]`) e comparada com a versão original limpa. Se forem iguais, a frase é um palíndromo (`True`); caso contrário, não é (`False`).

## Como executar o código?
1. Certifique-se de ter o Python 3 instalado na máquina.
2. Salve o arquivo com a extensão `.py` (por exemplo, `palindromo.py`).
3. Abra o terminal na pasta onde o arquivo está localizado.
4. Execute o comando:
```bash
   python3 palindromo.py
```
5. O resultado dos testes será exibido diretamente no terminal.

Também é possível importar a função `analisar` em outro script Python e testá-la com frases próprias:
```python
from palindromo import analisar
print(analisar("Sua frase aqui"))
```

## Exemplo
Entrada:
```python
texto1 = "A sacada da casa de cadasa"
texto2 = "Socorram-me, subi no ônibus em Marrocos"
```

Saída:<br>

Teste 1: False<br>
Teste 2: True


- `texto1` não é um palíndromo, pois, após a limpeza (`asacadadacasadecadasa`), a string invertida não corresponde à original.
- `texto2` é um palíndromo clássico da língua portuguesa: ao remover pontuação, espaços e acentuação (que já não é letra ASCII e é descartada pela regex), a frase resultante (`socorrammesubinoonibusemmarrocos`) é idêntica à sua versão invertida.
