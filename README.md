# Challenge project - Create a rock, paper, scissors game with GitHub Copilot

**Meta de tempo:** 30 minutos

**Resumo:** Demonstre sua capacidade de analisar, criar e usar diferentes métodos para desenvolver um minijogo de console em Python com GitHub Codespaces e GitHub Copilot.

> Este é um módulo de **_projeto de desafio_** em que você realizará um projeto de ponta a ponta com base em uma especificação. Este módulo tem como objetivo ser um teste das suas habilidades: há poucas diretrizes e nenhuma instrução passo a passo.

## Objetivos de aprendizagem:
Neste módulo, você demonstrará sua capacidade de:
- Experimentar o GitHub Codespaces como ambiente de desenvolvimento
- Desenvolver rotinas de entrada e saída de dados em um aplicativo de console em Python
- Usar o GitHub Copilot como assistente

## Pré-requisitos:
- Aplicar instruções de iteração usando entradas de dados
- Processar dados
- Formatar a saída de dados
- Noções básicas sobre métodos em Python

# Introdução

Criar um mini-jogo pode ajudar você a praticar suas habilidades de programação e aprimorar sua capacidade de criar aplicativos de console em Python. 

Neste módulo, você desenvolverá o clássico minijogo de pedra, papel e tesoura, com a ajuda de GitHub Codespaces e GitHub Copilot. Ou seja, você não precisará se preocupar com a configuração do ambiente de desenvolvimento e poderá se concentrar em desenvolver o aplicativo e contar com um assistente de código.

O jogo pedra, papel e tesoura é um jogo de mão em que cada jogador escolhe uma das três ferramentas. Do ponto de vista programação, esse é um belo exercício para praticar decisões condicionais, iterações e utilização de módulos de Python.

O vencedor do jogo é determinado por um conjunto de regras simples:    
- Pedra vence a tesoura
- Tesoura vence o papel
- Papel vence a pedra

Ao final deste módulo, você criará um aplicativo jogável de mini-jogo!

## Preparar-se para o desafio

Você deverá user o GitHub Codespaces para desenvolver o aplicativo de mini-jogo. O GitHub Codespaces é um ambiente de desenvolvimento hospedado que permite que você crie rapidamente um ambiente de desenvolvimento completo para o seu projeto. Você pode usar o Codespaces para desenvolver aplicativos de console em Python sem precisar instalar o Python ou qualquer outra ferramenta no seu computador local.

1. Para começar, você precisará de uma conta no GitHub. Se você não tiver uma conta, crie uma gratuitamente em [github.com](https://github.com/).

2. Habilite o serviço do [GitHub Codespaces](https://docs.github.com/en/codespaces) em sua conta do GitHub. O Codespaces oferece 60 horas de uso gratuita por mês. [Estudantes podem obter acesso gratuito ao GitHub Copilot](https://aka.ms/copilot-estudantes)

3. Você deverá fazer uma cópia do repositório modelo para o seu GitHub. Para isso, você deverá acessar o [repositório](https://github.com/cyz/challenge-project-python-game) e fazer um `Fork`. Ao finalizar o fork do repositório, você terá uma cópia do repositório modelo em sua conta do GitHub. Você usará esse repositório para desenvolver o aplicativo de mini-jogo.

4. Na página do repositório que foi criado, clique no botão `Code` e, na aba Codespaces, clique em `Create codespace on main`. Em alguns instantes, o Codespaces criará um ambiente de desenvolvimento para você.

5. Quando o Codespaces terminar de criar o ambiente de desenvolvimento, você verá uma janela do VS Code no navegador. Você pode usar o VS Code no navegador para desenvolver o aplicativo de mini-jogo.

## Exercício 1 - Adicionar a extensão do GitHub Copilot

Seu objetivo é desenvolver um aplicativo de minijogo de console em Python, utilizando o GitHub Copilot.

### Especificação 
Neste exercício de desafio, você deverá atualizar o arquivo de JSON existente na pasta `devcontainer/devcontainer.json` para adicionar a extensão do GitHub Copilot.

- O Codespaces identifica as extensão que devem ser instaladas pelo `id` da marketplace do Visual Studio Code.
- A identificação da extensão do GitHub Copilot é `GitHub.copilot`.

### Verificar seu trabalho

1. Acesse o seu Codespaces e abra o arquivo `app.py` no VS Code.
2. Comece a digital o digitar o comentário:
    
    ```python
    # escreva 'olá mundo' na tela
    ```
3. O GitHub Copilot deverá completar o código para você. O resultado deverá ser semelhante ao seguinte:

    ```python
    # escreva 'olá mundo' na tela
    print('olá mundo')
    ```
4. Execute o aplicativo com o comando `python app.py` no terminal e verifique se o resultado é semelhante ao seguinte:

    ```bash
    olá mundo
    ```

Depois de validar os resultados deste exercício, prossiga para o próximo exercício deste desafio.

## Exercício 2 - Criar a lógica do jogo

Com o Codespaces configurado e o GitHub Copilot instalado, seu objetivo é desenvolver 
o minijogo de console em Python. Você precisará criar a lógica do jogo seguindo as especificações e usar o GitHub Copilot para ajudar a criar os métodos.

### Especificação 
Neste exercício de desafio, você deverá definir os elementos que serão usados no minijogo, criar a estrutura de repetição para permitir que o usuário jogue várias vezes, criar a lógica de decisão para determinar o vencedor e exibir o resultado.

#### Regras do jogo

O jogo pedra, papel e terousa possui três regras simples:
- Pedra ganha da tesoura (quebrando-a)
- Tesoura ganha do papel (cortando-o)
- Papel ganha da pedra (embrulhando-a)

#### Interação com o jogador

O console será usado para interagir com o jogador. O jogador poderá escolher uma das três opções: `pedra`, `papel` ou `tesoura`. O jogador também poderá escolher se deseja jogar novamente ou não, ser avisado caso digite uma opção inválida e saber a sua pontuação no final do jogo.

#### Definições para o jogo

- Importe o módulo random para utilizar a função `choice`, que fará o papel do nosso adversário
- Crie uma lista chamada `options` com as opções do jogo: `pedra`, `papel` e `tesoura`
- Crie as variáveis:
    - `rounds_played` para armazenar a quantidade de rodadas
    - `score`   para armazenar vitórias do jogador
- Utilize o `while` para criar uma estrutura de repetição que permita que o usuário jogue várias vezes
- Crie uma variável chamada `random_choice` para armazenar a opção do jogador adversário, utilizando a função `choice` do módulo `random`

#### Validação da entrada do usuário
- A cada rodada, o jogador deverá digitar uma das opções da lista e ser informado se ganhou, perdeu ou empatou com o adversário
- O minijogo deverá tratar as entradas do usuário, colocando-as em caixa baixa e informar se a opção é inválida
- Ao final de cada rodada, o jogador deverá responder se deseja jogar novamente ou não

### Verificar seu trabalho

1. Execute o minijogo no console com o comando `python app.py`
2. No prompt, digite uma das opções do jogo: `pedra`, `papel` ou `tesoura`
3. O minijogo deverá informar se o jogador ganhou, perdeu ou empatou com o adversário
4. Escolha continuar jogando
5. No prompt, digite `screen`
5. O minijogo deverá informar se a opção digitada pelo jogador é inválida
6. Repita os passos 2 e 4 para jogar algumas rodadas e escolha não continuar jogando
7. Verifique se o minijogo é encerrado e se ele irá exibir a sua pontuação, informando quantidade de vitórias e rodadas

Parabéns se você se saiu bem neste desafio!