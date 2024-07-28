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

#Codigo 
import random

print("*********************************")
print("Bem vindo ao jogo de Adivinhação!")
print("*********************************")

numero_secreto = random.randrange(1, 101)
total_de_tentativas = 0
pontos = 1000

print("Qual o nível de dificuldade?")
print("(1) Fácil (2) Médio (3) Difícil")

nivel = int(input("Defina o nível: "))

if(nivel == 1):
    total_de_tentativas = 20
elif(nivel == 2):
    total_de_tentativas = 10
else:
    total_de_tentativas = 5

for rodada in range(1, total_de_tentativas + 1):
    print("Tentativa {} de {}".format(rodada, total_de_tentativas))

    chute_str = input("Digite um número entre 1 e 100: ")
    print("Você digitou ", chute_str)
    chute = int(chute_str)

    if(chute < 1 or chute > 100):
        print("Você deve digitar um número entre 1 e 100!")
        continue

    acertou = chute == numero_secreto
    maior = chute > numero_secreto
    menor = chute < numero_secreto

    if(acertou):
        print("Você acertou e fez {} pontos!".format(pontos))
        break
    else:
        pontos_perdidos = abs(numero_secreto - chute)
        pontos = pontos - pontos_perdidos
        if(maior):
            print("O seu chute foi maior que o número secreto")
            if (rodada == total_de_tentativas):
                print("O número secreto era {}. Você fez {}".format(
                    numero_secreto, pontos))
        elif(menor):
            print("Você errou! O seu chute foi menor do que o número secreto.")
            if (rodada == total_de_tentativas):
                print("O número secreto era {}. Você fez {}".format(
                    numero_secreto, pontos))

print("Fim do jogo")

 Isto é apenas o começo de uma jornada de sucesso apenas demonstrando o qué venho aprendendo .
