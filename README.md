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

