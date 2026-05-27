[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/KGJs7Wtk)

Durante os testes da classe Counter sem sincronização, observou-se que o valor final do contador frequentemente não era igual a zero, mesmo realizando a mesma quantidade de incrementos e decrementos. Isso ocorre devido à condição de corrida (race condition), onde múltiplas threads acessam e modificam simultaneamente a variável compartilhada c.

As operações c++ e c-- não são atômicas. Internamente, elas envolvem leitura, modificação e escrita do valor. Quando duas threads executam essas operações ao mesmo tempo, algumas atualizações podem ser perdidas, causando inconsistência nos dados em memória.

Na versão sincronizada, utilizando o modificador synchronized, apenas uma thread pode executar os métodos por vez. Isso garante exclusão mútua e preserva a consistência dos dados compartilhados.

Nos testes realizados, a versão sincronizada apresentou resultado final correto (zero) em todas as execuções, enquanto a versão sem sincronização apresentou valores inconsistentes em diferentes execuções.
