# Jogo-da-adivinha-o-02-
## Jogo de Adivinhação 2  
## Este é um simples jogo de adivinhação em Python, onde o jogador tenta adivinhar um número secreto. O objetivo é adivinhar o número correto dentro de um número limitado de tentativas.
### Como jogar

1. Ao iniciar o jogo, você será recebido com uma mensagem de boas-vindas.
2. Você tem 3 tentativas para adivinhar o número secreto.
3. Em cada tentativa, você deve digitar um número.
4. O jogo informará se o seu palpite é maior ou menor do que o número secreto.
5. Se você acertar o número secreto, uma mensagem de parabéns será exibida.
6. O jogo termina após 3 tentativas ou quando você adivinhar o número correto.

### Estrutura do código

O código está estruturado da seguinte forma:

- Definição do número secreto e do número total de tentativas.
- Loop que itera pelo número de tentativas.
- Leitura do palpite do jogador e comparação com o número secreto.
- Exibição de mensagens indicando se o palpite está correto, maior ou menor que o número secreto.
- Finalização do jogo com uma mensagem de encerramento.

### Exemplo de execução

```
*********************************
Bem vindo ao jogo de Adivinhação!
*********************************
Tentativa 1 de 3
Digite o seu número: 30
Você digitou  30
O seu chute foi menor do que o número secreto!
Tentativa 2 de 3
Digite o seu número: 50
Você digitou  50
O seu chute foi maior do que o número secreto!
Tentativa 3 de 3
Digite o seu número: 42
Você digitou  42
Parabéns! Você acertou!
Fim do jogo
```

### Como executar

Para executar o jogo, basta rodar o script em um ambiente Python. Você pode fazer isso salvando o código em um arquivo, por exemplo `adivinhacao.py`, e executando o comando:

```sh
python adivinhacao.py
```

### Requisitos

- Python 3.x

### Código

```python
print("*********************************")
print("Bem vindo ao jogo de Adivinhação!")
print("*********************************")
numero_secreto = 42
total_de_tentativas = 3
rodada = 1

while (rodada <= total_de_tentativas):
    print("Tentativa {} de {}".format(rodada, total_de_tentativas))

    chute_str = input("Digite o seu número: ")
    print("Você digitou " , chute_str)
    chute = int(chute_str)

    acertou = chute == numero_secreto
    maior = chute > numero_secreto
    menor = chute < numero_secreto

    if(acertou):
        print("Parabéns! Você acertou!")
    else:
        if(maior):
            print("O seu chute foi maior do que o número secreto!")
        elif(menor):
            print("O seu chute foi menor do que o número secreto!")

    rodada = rodada + 1

print("Fim do jogo")

 Isto é apenas o começo de uma jornada de sucesso apenas demonstrando o ué venho aprendendo . 
