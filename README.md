update 1
o que foi feito: 1. o robo interage com coletaveis, há uma função looping chamada processaTudo, que em uma parte verifica se o personagem interagido com o robô é mortal. Se sim ele é deletado

o que falta ser feito: definir os impactos da explosão da bomba, definir o teletransporte, definir o tiro do robbo e a colisão,
criar o level design baseado no original


update 12/05

funções separadas na função processaTudo pra reduzir o código (em ControleDeJogo)

robô agora muda os sprites conforme o input (método keypressed em Tela)

adicionado sinalizadores de direção do robô (método direction em Personagem)

problemas:
tamanho dos sprites do robbo estão diferentes.

update 13/05

foi corrigido alguns sprites do robbo, porem apenas para o fundo preto

definido que o tiro do robô sai uma posição a sua frente de acordo com a sua direção. (na função key pressed em Tela)

foi criada uma função que verifica se a posição inicial do tiro é viável, isso é, se o tiro não estará dentro de uma parede. (função posicaoinicialbala em ControleDeJogo) (não foi definido sobre as bombas)

foi criada uma função que define as colisões do tiro com os objetos (função ColisaoBala em ControleDeJogo) (foi definido apenas a colisão com as paredes, onde a bala é apagada do cenário)


proximo objetivo, definir as explosões das bombas e fazer o robô empurrar paredes amarelas
