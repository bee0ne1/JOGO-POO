update 1 (v1)
o que foi feito: 1. o robo interage com coletaveis, há uma função looping chamada processaTudo, que em uma parte verifica se o personagem interagido com o robô é mortal. Se sim ele é deletado

o que falta ser feito: definir os impactos da explosão da bomba, definir o teletransporte, definir o tiro do robbo e a colisão,
criar o level design baseado no original


*UPDATE 12/05 (v2)*

funções separadas na função processaTudo pra reduzir o código (em ControleDeJogo)

robô agora muda os sprites conforme o input (método keypressed em Tela)

adicionado sinalizadores de direção do robô (método direction em Personagem)

problemas:
tamanho dos sprites do robbo estão diferentes.

*UPDATE 13/05 (v3)*

foi corrigido alguns sprites do robbo, porem apenas para o fundo preto

definido que o tiro do robô sai uma posição a sua frente de acordo com a sua direção. (na função key pressed em Tela)

foi criada uma função que verifica se a posição inicial do tiro é viável, isso é, se o tiro não estará dentro de uma parede. (função posicaoinicialbala em ControleDeJogo) (não foi definido sobre as bombas)

foi criada uma função que define as colisões do tiro com os objetos (função ColisaoBala em ControleDeJogo) (foi definido apenas a colisão com as paredes, onde a bala é apagada do cenário)


proximo objetivo, definir as explosões das bombas e fazer o robô empurrar paredes amarelas


*UPDATE 14/05 (v5)*

extensão no método ehPosicaoValida, que agora contém uma parte dedicada
às paredes amarelas que são empurráveis pelo robô (em ControleDeJogo)

criação de métodos que verificam se ha um personagem ao redor de um personagem especifico em ControleDeJogo

criação do método morte: agora o robô pode morrer, e dependendo da quantidade de vidas a fase em questão é resetada ou ele volta para a fase 1.

criação do método explosão: agora objetos mortais e intransponíveis ao redor da bomba, quando atirada, morrem (inclusive o proprio robô)

no método de tecla space foi adicionado uma verificação para que o player não pressione o botão consecutivamente e o vetor faseAtual contenha mais de uma bullet.

código + organizado

próximos objetivos: fazer a animação de explosão e o teleporte



*UPDATE 15/05 (v6)*

agora os personagens possuem uma animação de morte. (métodos morte e morteHeroi em ControleDeJogo)
para isso foi uma adicionado um atributo boolean "morrendo" na classe Personagem, que quando se encontra true,
o personagem deve se tornar imóvel, assim realiza a animação de morte. 

foi definido a explosão da bomba, que verifica se há espaços vazios ao seu redor, que terão a animação de explosão
ou se há objetos destrutíveis que irão morrer

próximos objetivos: definir o teletransporte, definir o lançachamas e terminar a fase1

*UPDATE 16/05 (v7)*

agora o robô pode se teleportar, ele realiza uma animação
pra isso foi criado dois novos status na classe Heroi: teleporteInicio
e teleporteFim. 

foi concertado uma parte do código em que evita a repetição de códigos por frame, os métodos que necessitavam apenas do robô foram tirados do laço for na ProcessaTudo, agora esses códigos são rodados uma vez por frame
O JOGO RODA A 60 FPS ENTÃO O MÉTODO PROCESSATUDO ESTÁ SENDO RODADO 60 VEZES POR SEGUNDO

próximos objetivos: definir o lança-chamas e terminar a fase1

*UPDATE 19/05 (v8)*
agora há lança chamas, o código também está mais organizado. 
O lança chamas possui um arraylist que contém os fogos, 
e agora as bombas possuem um arraylist que contém as explosões. 
além de deixar o código melhor, isso conecta esses elementos que antes
ficavam jogados no arraylist da fase, e precisavam fazer mais verificações para encontrá-los

proximos objetivos: implementar as fases e os inimigos.

*UPDATE 20/05 (v9)*
primeira fase concluida, algumas alterações no código
agora o lança chamas possui todas as direções (antes só para baixo)
foi adicionada uma fase teste para testar as mecanicas do jogo

*UPDATE 21/05 v10*
segunda fase concluida, agora o jogo possui perseguidores fantasmas
seria bom implementar vidas para o jogador coletar

v10.2
agora o jogo possui vidas espalhadas nas fases, e o usuario pode escolher o tempo de ativacao dos lança chamas

*UPDATE 21/05 v11*
terceira fase concluida, novo inimigo arrow que anda ao redor das paredes
agora o botão c reseta a fase, mas gasta uma vida.

*UPDATE 22/05 v12*
quarta fase concluida

v12.2
MUDANÇA GERAL NO CÓDIGO, AGORA AS CLASSES DOS PERSONAGENS POSSUEM MÉTODOS, QUE ANTES TODOS ESTAVAM NA CLASSE CONTROLE DE JOGO.

*UPDATE 23/05 v13*
fase final concluida, falta fazer a fase dos créditos e o save+load do jogo

