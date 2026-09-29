Etapa 1 — Introdução
Após assistir ao vídeo e estudar o material disponibilizado, responda às questões abaixo.
1. O que é uma Máquina de Turing?
modelo matemático e abstrato de computação, criado pelo matemático Alan Turing
2. Quais são os principais componentes de uma Máquina de Turing?
Fita, Cabeçote de leitura e escrita, Estados, Alfabeto, Função de transição, Estado inicial, Estados de
aceitação e rejeição
3. Qual é a importância das Máquinas de Turing para a computação?
As máquinas de turing são importantes porque servem como um modelo teórico para representar o
funcionamento de computadores e algoritmos. Elas ajudam a entender quais problemas podem ou não
ser resolvidos por meio de um processo computacional e porque permitem estudar o que pode ser
calculado, como pode ser calculado e quais são os limites dos computadores.
4. Qual é a relação entre Máquina de Turing e algoritmo?
A máquina de turing e o algoritmo estão relacionados porque uma máquina de turing pode ser utilizada
para representar e executar um algoritmo, um algoritmo descreve o que deve ser feito, enquanto a
máquina de turing fornece um modelo de como esses passos podem ser executados de forma
sistemática, isso permite estudar se um problema pode ser resolvido computacionalmente.
Etapa 2 — Simulação
Utilize um software ou simulador de Máquina de Turing indicado pelo professor.
Crie uma máquina capaz de reconhecer palavras da forma:
0n1n
Exemplos aceitos
01
0011
000111
00001111
Exemplos rejeitados
0
1
001
011
00111
Desafio: A máquina deverá verificar se existe a mesma quantidade de símbolos 0 e 1, seguindo a
lógica de funcionamento de uma Máquina de Turing.
Etapa 3 — Registro da simulação
Após executar a máquina, registre:
A palavra utilizada como entrada.
Os estados percorridos.
O resultado da execução: ACEITA ou REJEITA.
Uma captura de tela da simulação.
Realize pelo menos 3 testes:
2 entradas que devem ser aceitas.
1 entrada que deve ser rejeitada.
Registro dos testes
Teste Entrada Resultado esperado Resultado obtido Estados percorridos
1
Ex.: 0011
ACEITA
Aceita
q0 fi q1 fi q2 fi q0 fi q1 fi q2 fi q3 fi q
2
Ex.: 000111
ACEITA
Aceita
q0 fi q1 fi q2 fi q0 fi q1 fi q2 fi q0 fi q1 fi q2 fi q3 fi q
3
Ex.: 00111
REJEITA
Rejeita
q0 fi q1 fi q2 fi q0 fi q1 fi q2 fi q0 fi q1 fi q2 fi q
Descrição da Máquina de Turing criada:
A Máquina de Turing foi criada para reconhecer palavras pertencentes à linguagem:
$$ L = \{0^n1^n \mid n \geq 1\} $$
A máquina verifica se a palavra possui uma quantidade igual de símbolos 0 e 1, mantendo também a
ordem: primeiro aparecem todos os 0s e depois todos os 1s.
Para realizar essa verificação, a máquina procura o primeiro 0 ainda não processado, marca esse
símbolo como X e percorre a fita para a direita em busca do primeiro 1 ainda não processado. Quando
encontra o 1, marca-o como Y e retorna para o início da palavra para procurar o próximo 0.
Esse processo continua até que todos os 0s tenham sido marcados. Ao final, se todos os 1s também
estiverem marcados, a máquina entra no estado de ACEITA. Caso exista algum 0 sem um 1
correspondente, algum 1 sem um 0 correspondente ou a ordem dos símbolos esteja incorreta, a
máquina entra no estado de REJEITA.
Etapa 4 — Reflexão sobre os limites computacionais
Uma Máquina de Turing consegue resolver qualquer problema? Explique com suas palavras por que
existem problemas que não podem ser resolvidos por algoritmos.
Existem problemas que são considerados indecidíveis, ou seja, não existe nenhum algoritmo capaz de
fornecer uma resposta correta para todas as possíveis entradas, isso acontece porque existem
problemas que não é possível criar uma sequência de passos que sempre termine e produza uma
resposta correta, as máquinas de turing representam os limites do que pode ser calculado por
algoritmos. Portanto, existem problemas que não podem ser resolvidos por nenhum algoritmo, mesmo
utilizando uma Máquina de Turing.
Questão final
Problema para reflexão:
Imagine que você recebeu um problema computacional muito complexo. Como saber se ele é apenas
difícil de resolver ou se, na verdade, não existe nenhum algoritmo capaz de resolvê-lo para todos os
casos?
Explique utilizando os conceitos estudados sobre Máquinas de Turing, computabilidade e limites
computacionais.
Um problema pode ser difícil, mas ainda assim possuir um algoritmo que consegue resolvê-lo. Nesse
caso, uma Máquina de Turing consegue executar o algoritmo e produzir uma resposta, embora possa
levar muito tempo ou exigir muitos recursos. Esses problemas estão relacionados à complexidade
computacional.
Por outro lado, existem problemas não computáveis ou indecidíveis, para os quais não existe nenhum
algoritmo capaz de fornecer uma resposta correta para todos os casos. Nesse caso, não importa
quanto tempo ou memória estejam disponíveis: o problema está além dos limites da computação. Um
exemplo clássico é o Problema da Parada, que demonstra que não é possível criar um algoritmo geral
capaz de determinar se qualquer programa irá parar ou executar indefinidamente.
Assim, utilizando os conceitos de Máquina de Turing e computabilidade, podemos pensar da seguinte
forma:
Problema computável - existe uma Máquina de Turing que consegue resolvê-lo.
Problema difícil - existe um algoritmo, mas sua execução pode exigir muito tempo ou recursos.
Problema indecidível - não existe uma Máquina de Turing/algoritmo que resolva corretamente todos os
casos.
A lógica da máquina é:
q0: procura um 0 ainda não marcado.
q1: procura um 1 correspondente ao 0.
q2: retorna para o início da fita.
qAceita: todos os 0s possuem um 1 correspondente.
qRejeita: encontrou uma quantidade diferente de símbolos ou ordem inválida.
X: marca um 0 já utilizado.
Y: marca um 1 já utilizado.
B: representa o espaço em branco da fita.
2. Teste 1 — Entrada 01
Entrada
01
Simulação
A máquina encontra o 0, marca como X e procura um 1.
01
q0: encontra 0 fi marca X e vai para a direita.
X1
q1: encontra 1 fi marca Y e retorna para a esquerda.
XY
q2: retorna ao início da palavra.
XY
q0: não existem mais 0s. A máquina verifica que também não existem 1s sem correspondência.
XY
Resultado:
ACEITA
Estados percorridos:
q0 fi q1 fi q2 fi q0 fi qAceita
3. Teste 2 — Entrada 0011
Entrada
0011
A máquina precisa encontrar dois 0s e dois 1s.
Simulação
Primeiro 0:
0011
fl
X011
O primeiro 0 foi marcado como X.
Agora procura o primeiro 1:
X011
fl
X0Y1
O primeiro 1 foi marcado como Y.
A máquina retorna ao início e procura outro 0:
X0Y1
fl
XXY1
Agora procura outro 1:
XXY1
fl
XXYY
Todos os símbolos foram correspondidos.
Resultado:
ACEITA
Estados percorridos:
q0 fi q1 fi q2 fi q0 fi q1 fi q2 fi q0 fi qAceita
4. Teste 3 — Entrada 00111
Entrada
00111
Aqui temos:
2 zeros
3 uns
Portanto, a palavra deve ser rejeitada.
Simulação
Primeiro 0:
00111
fl
X0111
Primeiro 1:
X0111
fl
X0Y11
A máquina retorna e encontra o segundo 0:
X0Y11
fl
XXY11
Agora encontra o segundo 1:
XXY11
fl
XXYY1
Neste momento, os dois 0s já foram correspondidos, mas ainda existe um 1 sem correspondência:
XXYY1
›
1 sobrando
Portanto, a máquina entra no estado de rejeição.
Resultado:
REJEITA
Estados percorridos:
q0 fi q1 fi q2 fi q0 fi q1 fi q2 fi q0 fi qRejeita
5. Tabela dos três testes
Você pode colocar esta tabela diretamente no trabalho:
Teste Entrada Resultado esperado Resultado obtido Estados percorridos
1 01 ACEITA ACEITA q0 fi q1 fi q2 fi q0 fi qAceita
2 0011 ACEITA ACEITA q0 fi q1 fi q2 fi q0 fi q1 fi q2 fi q0 fi qAceita
3 00111 REJEITA REJEITA q0 fi q1 fi q2 fi q0 fi q1 fi q2 fi q0 fi qRejeita
6. Evidências da simulação
No trabalho, você pode colocar as capturas de tela desta forma:
Evidência — Teste 1
Entrada: 01
Resultado: ACEITA
[INSIRA AQUI A CAPTURA DE TELA DO SIMULADOR MOSTRANDO A MÁQUINA ACEITANDO 01]
Evidência — Teste 2
Entrada: 0011
Resultado: ACEITA
[INSIRA AQUI A CAPTURA DE TELA DO SIMULADOR MOSTRANDO A MÁQUINA ACEITANDO
0011]
Evidência — Teste 3
Entrada: 00111
Resultado: REJEITA
[INSIRA AQUI A CAPTURA DE TELA DO SIMULADOR MOSTRANDO A MÁQUINA REJEITANDO
00111]
Conclusão dos testes
Os três testes demonstram o funcionamento da Máquina de Turing. As entradas 01 e 0011 foram
aceitas, pois possuem a mesma quantidade de 0s e 1s, mantendo a ordem 0n1n. A entrada 00111 foi
rejeitada, pois possui dois 0s e três 1s. Dessa forma, a máquina reconhece corretamente palavras
pertencentes à linguagem L = {0n1n | n ‡ 1}.
Importante: as partes de "captura de tela" precisam ser feitas no simulador que o professor indicou. Se
for JFLAP, eu também posso montar para você a tabela completa de transições (estado atual, símbolo
lido, símbolo escrito, movimento e próximo estado) para você simplesmente reproduzir a máquina n
