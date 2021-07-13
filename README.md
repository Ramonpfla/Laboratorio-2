# Laboratorio-2

  Para o exercício 10 a lógica geral utilizada para realizar a multiplicação é formada por 3 passos:
  
  1- Faz um shift para a direita no multiplicador.
  2- Soma o multiplicando com o produto se a flag C estiver setada.
  3- Faz um shift para a esquerda no multiplicando.
  
  As únicas verificações necessária para o código funcionar foram um BCS para ver se após o shift a direita o Carry está setado ou não e um CBZ para verificar se o multiplicador é diferente de 0. Além de utilizar as funções BL para chamar a sub-rotina e BX para sair dela.
  
  Para o exercício 11, para não modificar os registradores que foram usados como auxiliares foi feito um Push dos valores iniciais antes de modifica-los. Após isso, verifica-se se o valor carregado em R0 não é 0, caso seja, ele retorna 1 para o R0 (0!=1) e encerra o programa. Próximo passo é fazer o loop para realizar as multiplicações sucessivas até ele chegar em 2, quando é realizada a ultima multiplicação. Durante as varias multiplicações, verifica-se se o numero não ultrapassa 32 bits, fazendo o numero atual x 2 (que é a menor multiplicação de todos os fatoriais), se ele não estourar, a conta segue, se ele estourar, R0 retorna -1 e o programa é encerrado. Se nada acontecer ele segue a multiplicação até o final e por fim mostra o valor do fatorial em R0 e retorna os auxiliares para os valores iniciais.
