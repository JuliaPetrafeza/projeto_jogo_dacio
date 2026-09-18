# Bob the robber

## 1.Descrição do Sistema

O projeto consiste em um sistema que imita o jogo "Bob the robber", que será executado no CMD do computador. O sistema permite guiar o ladrão Bob a invadir um prédio, roubar o dinheiro e fugir até a saída. O desafio do usuário é se movimentar pelos andares, conectados por espaços em branco e limitados pelas paredes, roubar o dinheiro e chagar até a saída, mas sem que o seguraça o alcance. Durante o jogo, o usuário deve usar estratégias para fazer o percuso pelos caminhos possíveis, evitando o guarda e concluindo o objetivo. O cenário do programa e seus componentes serão representados por caracteres ASCII, o personagem Bob pode ser movimentado através das teclas direcionais e não haverá limite de tempo para o jogo.

## 2.Fluxo de utilização esperado para o sistema

1. Ao iniciar o programa, o usuário visualizará todos os andares de um prédio, é um visão simplificada, como se o e difício fosse cortado ao meio`

2. Sobre os componentes do mapa:
   - `As paredes, que serão representadas por "#"`
   - `O personagem Bob, representado pela letra "B"`
   - `O guarda, representado pela letra "G"`
   - `A saída, representada pela letra "S"`
   - `O dinheiro, representado por "$"`
   - `Haverá 2 adares e será posicionado um caractere representando o dinheiro dentro do mapa`

2. O usuário pode "descer" e "subir" atrvés das setas direcionais do teclado, assim mudando de andar, fugindo do guarda e completando o desafio

3. Um guarda se locomove de forma aleatória perseguindo o usuário

4. Se o guarda e o Bob se encontrarem o jogoo acaba, ou se o Bob chegar à saída com o dinheiro o jgo também acaba

5. Não é possivel atravessar as paredes, não existe um limite de tempo e só é possivel um movimento por vez

## 3.Fluxograma da lógica do sistema

![Fluxograma](https://drive.google.com/file/d/1aFcGseEMWyP4mLJdGP-KYJg86lIVWs_0/view?usp=sharing)

## 4.Estrutura de dados

```c
//estrutura da posição do jogador
struct Jogador {
    int x;
    int y;
    int possuiDinheiro;
}

//estrutura posição Guarda
struct Guarda {
    int x;
    int y;
}

//estrutura posição dinheiro
struct Dinheiro {
    int x;
    int y;
    int coletado;
}
